---
layout: post
title: What and Why Machine Learning Engineering
comments: true
tags: [Industry, Data, Archive, MLE]
---

Here I am blogging again after having done it during college and a lot of things seem different now. My last blog was in 2018 and right now I am 6 years in the future. I noticed that I tend to put a lot of paragraphs in my previous posts so I think I will stop doing that and they seem to be rather short so I think from now on, I will try to venture deep into my thought process.

Any who why machine learning engineering? A couple days ago at work I was trying to express my interest in this subject when one person's reply was - How are ML systems different? Don't they just simply consume input from a model, and this is where I think engineers really underestimate machine learning. Its actually a little ironic if you ask me. As a person involved in software I think we assume machine learning models to simply be software with intelligence and that they behave in the same way software works ie, 

1. they give us what we want when we ask for it, 
2. if something is not right we can simply change the code for it and most importantly 
3. the final output of this model can simply be used as input for our business logic. 

<br>
This could not be more away from the truth, the problems being :-

1. They may not give us what we want always
2. If its buggy there is a huge process involved in improving the model
3. We simply can't treat the model output as the final answer

<br>
I think we trust machine learning too much that its made us this way and I don't blame anyone for that, I am actually being the cynical one here because machine learning has come a long way, I mean as I am writing this post there exists GPT-4 - huge models which can talk and also reason like humans, models which can generated extremely real images and videos. But at the same time if you are going to really important tasks having million dollars at stake into the hands of machine learning models such as :-

1. Loan underwriting, fraud detection, terms of service violation
2. Translation of voice in real time, NSFW filtering of images/videos, fake news detection
3. hurricane/tornado forecasting, demand forecasting, pricing predictions
4. video recommendation, image search, text search

<br>
then I think its fine to be skeptical that your ML model may not always be good or right. And since obviosuly we don't have machine learning to tell if another machine learning model is doing well enough because then it becomes more complex, we need to fall back to engineering and be smart about how we implement systems which interact with ML models. Case in point, fraud detection has further human review steps, text search suggests similar search queries, product review summarisation has feedback mechanisms to see if the customer actually felt it useful or completely wrong and the list goes on, although what usually happens is that such instruments for feedback or cross checking come into place way before a system consumes from a machine learning model, however the notion that an intelligent part of the system which can go wrong is controlling this decision making is prevalant from the start. 

Now this is 1 side to the problem, the other side being - how can we make these systems better in terms of the model itself and in terms of software itself, similar to normal software engineering. And so here you have the 2 pieces of machine learning engineering and this niche is important I believe as the use of machine learning increases in systems. Its easy to see why you would also need to be aware behind the working of the model itself to better tackle these problems. 

Apart from this being an extremely interesting topic for me, another motivation I have for learning more about this is my notion that the Indian software community does not beleive this field is important to understand or does not operate that way. From personal experience I know most companies currently have their normal software team do the machine learning engg part as well, however often times its considered a normal engineering problem and not given separate attention such as the android/ios community or frontend as well. And so this is something I want to change, I personally want to explore ML engineering problems, parctises and challenges which we can come across while building software for India and hopefully be able to share insights and processes which I have experienced. 

My experience in Flipkart has personally opened me too this subject in terms of how important it is, whats happeneing in the current times, and whats lacking in terms of the indian tech space and so hopefully I would have inspired like minded people interested in ML Engineering to explore and contribute more to this area. If this is first blog post you have read about ML Engineering, I would like to say - buckle up because I have a lot on my mind which I would like to explore and deep dive into ML engineering and with the advent of LLMs and Image Gen models, I think the scope for ML engineering to solve extremely niche problems cannot get bigger than the opportunity that is currently developing in the tech space.

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
                            