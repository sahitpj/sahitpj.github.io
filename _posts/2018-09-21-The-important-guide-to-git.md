---
layout: post
title: The Important guide to git
comments: true
tags: [Git, Archive]
---

Version control, a key tool for developers and the one which we end up using - git. Although git happens to be failry simple and intuitive in basic things such as `pull` , `push` and `clone` , it however poses a challenge when you want to work with actual version control commands, such as reverting a commit, or updating your repository with the remote one - The main reason why there exits multiple applications which use visual version control, but if you are like me who enjoys working on the command line this post os for you!


<h1 class="post-subheading">Reverting a commit</h1>

Although reverting a commit, can be equivalent to undoing your changes on projects which are small, when it comes to bigger projects and packages, it becomes a tedious task. Thus reverting it important. 

The command for reverting a commit is

```console
git revert <commit id>
```

we can also use the reset command

```console
git reset --soft HEAD~n
git reset --hard HEAD~n
```

where n is the number of commits you want to revert back to 

The --soft keeps your present work while reverting, while --hard does not.
<br>
<h1 class="post-subheading">Creating a new branch</h1>

in order to do this, simply type the following 

```console
git checkout -b <new branch> <branch that the new branch will look like>
```

changing to a branch can be done simply by

```console
git checkout <branch>
```
<br>
<h1 class="post-subheading">Updating the remote or upstream</h1>

While contributing and opening pull request after pull requests, it becomes important to update your clone to the upstream - the original project repo. So in order to do so

```console
git remote add upstream github.com/ORIGINAL-USERNAME/REPO-YOU-FORKED-FROM.git
git fetch upstream
```

and finally updating it 

```console
git pull upstream master
```
<br>
<h1 class="post-subheading">Force Push</h1>

Force push can occur when remote is ahead in commits and you want push your repository. In this case git usually doesn't give you the permission to use, because it will ask you to pull first. I really don't happen to remember when I would actually want this to happen, but in case you do

```console
git push -f
```
<br>

Hope the following extra pointers have helped in making, using git far simpler

cheers!



<!-- <div id="disqus_thread"></div>
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
<noscript>Please enable JavaScript to view the <a href="https://disqus.com/?ref_noscript">comments powered by Disqus.</a></noscript> -->