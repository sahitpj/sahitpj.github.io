---
layout: post
title: The tar cheatsheet and how to never forget
comments: true
tags: [Tar, Cheatsheet]
---


tar, A GNU project which we happened to stumble upon atleast once, and it is never easy understanding the flags to use in order to compress or extract files, so in this short blog post, I am going to give you a list of basic tar functions and their flags and a good way of remembering them. I want to thank an anonymous dev.to user who came up with this idea 'cause honestly I think it is a nice way. So without further a do, lets dive in and Warning - PG 13 content ahead !

<h1 class="post-subheading">Extracting</h1>

extracting using tar is something we would end up doing using tar, and to do that we use the following code

```console
tar -xzvf name-of-archive.tar.gz
```
* -f allows you to mention path/file name
* -v means lot of processing is shown step by step
* -z tells tar to decompress the file using gzip
* -x extracts files 

How to remember it?


tar **X**tract **Z**he **V**ucking **F**ile filename.tar.gz


May not be the best way but does get the job done

<h1 class="post-subheading">Compressing</h1>

tar lets you compress files or a directory in a tar.gz file. The flags for compressing are quite similar to that of extracting.

```console
tar -czvf name-of-archive.tar.gz
```

* -f allows you to mention path/file name
* -v means lot of processing is shown step by step
* -z tells tar to compress the file using gzip
* -c create an archive 

How do you remember? This shouldn't be hard to figure out, once you know the first one


So the next time you ever see a tar.gz file, you won't have to worry about how to extract, 'cause you will have it, at the back of your head

Happy compressing and extracting !

Courtesy - dev.to


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