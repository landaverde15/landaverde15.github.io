---
layout: post
title: "Understanding Docker"
date: 2020-10-22 07:00:00 -0700
---

![docker img]({{site.url}}/assets/docker.png)

Before CIT480, I had only heard the word Docker but I were lying to you if I told you I knew what Docker was. The only thing I knew was that Docker had something to do with containers, which in reality I had no idea what containers were either.

After doing some research and having to get my hands dirty with Docker in this course here is what I have learned:

1) What docker is
2) What a container is
3) What a docker file is

I will quickly walk through each of these topics for those who still can't grasp the idea of what Docker is.

===> What is Docker?

To make this easy to understand I'm going to use an example. Let's say I have 3 GoLang applications that all use different versions of GoLang. Since I cannot have different versions of GoLang on my laptop then it is impossible to run all 3 applications. Literally I would need 3 machines all with the different GoLang versions to run those applications individually. Also I can purchase 3 different spaces on AWS to host these applications. This is where Docker comes in and solves this dilemma. Docker is kind of like a virtual machine. Where within my laptop I can run 3 virtual machines that each individually run my 3 GoLang projects. Instead, Docker has what they call containers.

===> What is a container?

Unlike Virtual Machines, containers do not run operating systems. A container inherits necessary files from the operating system of its host (my laptop) and share the kernel. The containers are all seperated but live within the same storage (my laptop). Each of the containers can run different images for instance: Ubuntu, CentOS, Debian, and more. Within each other containers I can create environments specific to only that container. Whatever I install in one container will not affect my other containers.

===> What is a docker file?

A Dockerfile is a document that contains all the commands to run to build an image for a container. For instance in the Dockerfile I would specify what Operating System I want, download PHP, download MySQL, and so on and so forth.

I hope this was helpful. To learn more about Docker you can [here][docker]. Hack on!

[docker]:https://docker-curriculum.com/




