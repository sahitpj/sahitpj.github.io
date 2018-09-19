---
layout: post
title: Package Modelling in Python
comments: true
---

We all develop python code - small or big, whether it is related to an Application or a package, the way in which the Python is written ultimately plays a major role in deciding it's usibilty. Thus assuming if I were to build a solution to a machine learning problem, however I cram my entire solution into one .py file. The good things are :

- I will have only 1 file to look at, for anything, be it an error or an enhancement

The bad things are :-

- I have to keep looking and edit the same file over and over again.
- If at all I am to scale this bigger datasets (makes sense in this context, but in general an important factor about any application is scalability), then how am I going to approach this?
- Even if I were to test iof this application is running or not, I would have to run the entire program which may require high power in order to check if basic functions are respoding correctly.

I hope the following points seem to give you a hint as to where I am going. Writing good code in python is a must, be it any domain you are working in, but writing code which takes time to edit, test and scale is a big NO, because then this product is restricted to the person who develops it. Simply put it's like having a doctor write a prescription to you compared with that which is printed. 

So with that in mind, let is understand how we can make an project we develop better simply by changing it's package structure. 

<h1 class="post-subheading"> Basic Python Project Structure </h1>

The overall structure of a Python package should look something like this 

```
project --- src
        --- tests
        --- dependency-list
        --- docs
        --- run_main.py
        --- run_tests.py
        --- setup.py
```

- The src is where the code resides
- The tests contains tests for each function in the program
- dependency list, contains the dependencies which the program requires
- docs
- the run_main.py should be able to execute the whole program
- the run_tests.py should be able to run tests with flags pertaining to any certain tests you would lile to run in particular


How does this help you may ask, well this :-

- introduces the notion of tests and separation of code from the main project
- running tests and and the main src can be done separately now and debugged too separately ( of course if this is to be a package we wouldn't have a run_main.py)


<h1 class="post-subheading"> Dependency List </h1>

The dependency list in python usually is named `requirements.txt`. And contains all dependent modules which the project requires. Unlike other languages, Python dependencies are far simpler to use and understand. 

Not so surprisingly there exists a python package `pipreqs` which automatically creates a project requirement file

```console
USER:~ username$  pip install pipreqs
USER:~ username$  pipreqs /path/to/project
```

Here is an example of one

```
numpy==1.13.1
matplotlib==2.0.2 
seaborn==0.8.1
```

<h1 class="post-subheading"> setup.py </h1>


The `setup.py` files helps install dependencies for the following project and if it is a package, helps install the package from pip

An example of a setup.py file is shown below, taken from flockos.

```python
import sys
from setuptools import setup, find_packages

NAME = "flockos"
VERSION = "1.2.0"

# To install the library, run the following
#
# python setup.py install
#
# prerequisite: setuptools
# http://pypi.python.org/pypi/setuptools

REQUIRES = ["requests", "six >= 1.10", "PyJWT"]

setup(
    name=NAME,
    version=VERSION,
    description="Flock API",
    author_email="",
    url="",
    keywords=["Flock API"],
    install_requires=REQUIRES,
    packages=find_packages(),
    include_package_data=True,
    long_description="""\
    Integrate your apps with flock using this API
    """
)
```

<h1 class="post-subheading">Docs</h1>

Keeping a docs folder in your project allowws github to generate a documentation website for the following project. These websites are generally static, although some people do still develop them the conventional way 

<h1 class="post-subheading">src</h1>

This include the main part of the program. This can be split into various sub-directories based pn functionality. Once again the idea is to separate code into various bins so that it is easier to understand and scale, so you could expect an src package of the following form

```
src --- utils
    --- core-functions
    --- error-handling
    --- (other-modules)
    --- __init__.py 
```


the `__init__.py` file here, helps define functions and objects which are to be exported. A project without this file would be able to export all of it's objects and functions, however it can allow all functions and objects to be accessed. Thus it becomes important to define what all modules are to be exported.

<h1 class="post-subheading">Summary</h1>

And thus in summary we have learnt what makes projects robust and how simply designing the way files appear and are written in a project makes a lot of difference. Package building architecture can be extended to other languages too such as Go, JavaScript where each file may have different names, however the basic outline remains the same. Hope this article helps you in building better scalable projects/packaged which can be debugged quickly and tested efficiently

Cheers!

<div id="disqus_thread"></div>
<script>

/**
*  RECOMMENDED CONFIGURATION VARIABLES: EDIT AND UNCOMMENT THE SECTION BELOW TO INSERT DYNAMIC VALUES FROM YOUR PLATFORM OR CMS.
*  LEARN WHY DEFINING THESE VARIABLES IS IMPORTANT: https://disqus.com/admin/universalcode/#configuration-variables*/
/*
var disqus_config = function () {
this.page.url = PAGE_URL;  // Replace PAGE_URL with your page's canonical URL variable
this.page.identifier = PAGE_IDENTIFIER; // Replace PAGE_IDENTIFIER with your page's unique identifier variable
};
*/
(function() { // DON'T EDIT BELOW THIS LINE
var d = document, s = d.createElement('script');
s.src = 'https://sahitpj-github-io.disqus.com/embed.js';
s.setAttribute('data-timestamp', +new Date());
(d.head || d.body).appendChild(s);
})();
</script>
<noscript>Please enable JavaScript to view the <a href="https://disqus.com/?ref_noscript">comments powered by Disqus.</a></noscript>