---
layout: post
title: "What are package managers and their components?"
date: 2020-09-18 09:00:00 -0700
---
For Blog 2 I will write about package managers. The reason I decided to write and explain about package managers is because of a new project I was given this week at work. The requirements for the project specified that it had to be written in React JS. I lightly touched React JS about 2 years ago but it wasn't at a level where I can consider myself a React Developer. When I looked at the docs and created a simple React app 2 years ago I remember that the package manager was `Node Package Manager (NPM)`. This week when I started the project at work and generated a React template I noticed I kept getting some red text in the command prompt about using/installing `Yarn`, which is another package manager. 

====> What are Package Managers?
In simple terms, a package manager is a software tool that helps to prepare your local environment for development and imports specified external dependencies. 

====> What are dependencies?
Dependencies are pieces of code that are useful and are needed to perform another task in a programming project.

For instance, let's say you and I are JavaScript developers. One day being bored I developed a nice tool in JavaScript that calculates tax depending on state. I then uploaded my code to GitHub which is an online public repository. Now, let's say you're given a project to develop an accounting app. Instead of writing tax logic on your own, you import the code I uploaded onto GitHub and implement it into your project. Now you have 1 less component to worry about in your project.

====> What is Node Package Manager (NPM)/Yarn?
NPM is a package manager for NodeJS (Server side JavasScript). Yarn (Yet Another Resource Negotiator) is another package manager just like NPM. After doing research on Yarn and why it is recommended for React projects instead of NPM, I discovered many interesting things. Yarn was developed by Facebook and is now open-source. The reason that Yarn was developed was to fix performance and security concerns with NPM. **Note**, React is also developed and maintained by Facebook.
