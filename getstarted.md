---
layout: page
title: Build a Website 
subtitle: Just 3 steps
---

There's a very easy way to use this theme, and there's a hard way. For most people (including myself!), I suggest going the easy route. If you're an advanced user and want to tinker with the hard way (using ruby gems), then [skip the easy way](https://github.com/daattali/beautiful-jekyll#the-hard-way-using-ruby-gems) if you know what you're doing.

## The easy way (recommended!)

Getting started is *literally* as easy as 1-2-3

Scroll down to see the steps involved, but here is a 40-second video just as a reference as you work through the steps. If you don't already have a [GitHub account](https://github.com/join), you'll need to sign up.

<div class="gs-section-01" markdown="1">

![Installation steps](assets/img/install-steps.gif)
<ol>
<li>Fork this project</li>
Fork this project by clicking the <strong>Fork</strong> button at the top right corner of this page. Forking means that you now copied this entire project and all the files into your account.

<div>

<li>Rename the project to <code>yourusername.github.io</code></li>
  Click on <em>Settings</em> at the top (the cog icon) and on that page you'll have an option to rename the project (<i>Repository name</i>). This will create a website with the <strong>Beautiful Jekyll</strong> template that will be available at <code>https://<yourusername>.github.io</code> within a couple minutes (check out the <a href="https://beautifuljekyll.com/faq/#custom-domain">FAQ</a>) if you want to use a different project name). <bdi class="name">If after a few minutes your website is still not ready,</bdi> try making any edit to any file, just to force GitHub to re-build your site.

<li>Customize your website settings
Edit the <code>_config.yml</code> file to change any settings you want. To edit the file, click on it to view the file and then click on the pencil icon to edit it (watch the video tutorial above if you're confused). The settings in the file are self-explanatory and I added comments inside the file to help you understand what each setting does. Any line that begins with a hashtag (<code>#</code>) is a comment, and the other lines are actual settings.</li>


<br>

Note that in the video above I only edited one setting in the <code>_config.yml</code> file.
<br>
<em>You should actually go through the rest of the settings as well. Don't be lazy, go through all the settings!</em>   
<br>  
Congratulations! You have a website!   
  
After you save your changes to the `_config.yml` file (by clicking on *Commit changes* as the video tutorial shows), your website should be ready in a minute or two at `https://<yourusername>.github.io`. Every time you make a change to any file, your website will get rebuilt and should be updated in about a minute or so. Your website will be initialized with several sample blog posts and a couple other pages.
  
Note that this was the easy way to *create* your website, but it does come at a cost: when Beautiful Jekyll gains new features in the future, *updating* your website to include all the latest features is cumbersome. See the [FAQ](https://beautifuljekyll.com/faq/#updating) for help with upgrading in the future.

<style>

.gs-section-01 h3 { 
     color: blue }

.gs-section-01 p {
     font-size: 30px;
}

</style>
