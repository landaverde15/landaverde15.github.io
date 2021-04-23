---
layout: post
title: Generating a Jekyll site locally
date: 2021-04-23 10:10:00 -0700
---

For some reason when I went to visit my Jekyll site I noticed that it was completely messed up. I couldn't click into my blog posts and the styling was completely off. I tried to debug the issue with number 1 - making changes to `_config.yml`. That didn't do the trick so I decided to make sure everything was mapped correctly, like `/assets` directory. I thought maybe the .css file could not be located. That did not do the trick either. Finally I decided, what the heck, I'll just generate a new site.

The following steps are what I did to generate my new Jekyll site (did this in Windows environment).

1) Open up CMD

2) Depending where you want your project to live, go to that directory. In my case I made it live in my Desktop so I changed directory to desktop.

3) In the CMD I ran `jekyll new cit481blog`. The third argument of the command can be replaced with the name of your project.

4) Once the command runs successfully you should cd into that new created project. In this case I ran `cd cit481blog`. 

5) Once inside the project we should run it locally and make sure all is well. Run the following command to serve this project in http://localhost:4000. `bundle exec jekyll serve`.

6) If all goes well you should be able to open up your browser and visit http://localhost:4000 and see your site. Then after this you can go on to create posts and place them within the `_posts` directory and also you can go on to personalize your site via editing the _config.yml and so on and so forth.

Thank you!
