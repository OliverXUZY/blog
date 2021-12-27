---
layout: post
title: How to hold gh-pages for another repo other than your-username.github.io?
---



### github pages

I already created one github page (https://oliverxuzy.github.io) for personal website 2 years ago. That time I only have master branch for hosting website as well as active development. 

Throughout one of my projects in developing julia package, I know more about the branch. I would use a feature branch for development and push to origin(remote repo). Then create a merge request on origin end (github.com on web).

In this blog project(https://oliverxuzy.github.io/blog), I set another repo other than https://oliverxuzy.github.io as website. I would use one feature branch(gh-pages) for hosting website and master branch for active development. Two branch do not contain exact the same content, so I do not use git merge or so (a troubled experience).

Another thing frustrated me a lot is internal link. I tried to use internal link for not only posts but [collections](https://stackoverflow.com/questions/27099427/jekyll-filename-without-date). I googled and edited the `_config.yml` file. Since I use blog repo to host instead of original link, I would edit baseurl as well(see [this](https://github.com/barryclark/jekyll-now/blob/12cb8a2e97c3b63c4bc92d2a1ab050b35bf946b7/_config.yml#L46) for example).

I encounter one problem when I tried to link to page in tutorial [High Dimensional Statistics]({{ site.baseurl }}{% link _tutorials/highDimStat.md %}). I set `site.url` and `site.baseurl` accordingly, but I found decrepency between building by site locally and publishing onlie. I use localhost:4000, and locally it should be `{{site.url}}{{site.baseurl}}`. 

I still have this problem. I right now use `site.baseurl + link _tutorials/highDimStat.md`. Then it showed correctly in remote as `https://oliverxuzy.github.io/blog/tutorials/highDimStat/`. But locally, when I click it goes to `http://localhost:4000/blog/blog/tutorials/highDimStat/`. I need to eliminate `/blog` inside the link.

### Troubleshooting
Here are some problem bothered me much as I developed in an initial stage. I update here. I will periodically add posts in the future if I solve other problems.
1. why github pages not updating? [an old question](https://stackoverflow.com/questions/24713112/why-does-my-github-page-do-not-update-its-content/47955695#47955695)
First of all, remote server can take up to 10 minutes for updating, please be patient at first. If you do not see change for like 12 hours, you can check following options. Although updating time (build and deploy weibite time) is not long unless you have some warnings and failure actions. The program tried that action several times and give up, but this does not affect the final effect. You need __action__ tab in github to see the workflow.
 - __Clear up the cache of website__. Some times the browser just save the cookies and cache for simplicity. After you push new things in html/md to remote site successfully. The browser might just show the old content. One way to tell is switch a brower and see.
 - __See action in github__. This is specially to github pages. Action tab will show the entire build and deploy workflow once you push change to origin. But it does require `.yml` file. I used jekyll for by blog site, this is convenient.

