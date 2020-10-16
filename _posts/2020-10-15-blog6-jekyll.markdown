---
layout: post
title: "Understanding Ansible Playbook's"
date: 2020-10-15 07:00:00 -0700
---

For Lab 3 I need to create an Ansible Playbook that performs all the tasks done in Lab 1. To be quite honest, my realm of expertise is not automation or tools like this. I'm a Software Engineer and plan to grow down that path. Touching back on Ansible, I've never heard about such thing or understand at all. After doing some research I'm now more comfortable with Ansible. Below are some notes of my understanding on Ansible Playbook's.

===> What is an Ansible Playbook?

Playbooks are files where Ansible code is written. They have code that tells Ansible on what to execute. A playbook honestly reminds me of a docker file.

===> Where are playbooks used for?

They are used for servers. The purpose of them is commonly for management/configuration on servers. For example with a playbook I can specify all the packages needed to be download on the server.

===> Sample 'Hello World' Ansible Playbook

{% highlight ruby %}
---
- name: A sample 'Hello World' playbook
  hosts: web_server
  tasks:
    - name: create a file called '/tmp/helloworld.txt'
      copy:
        content: Hello World!
        dest: /tmp/helloworld.txt
{% endhighlight %}

After running this playbook successfully, you should be able to run the following command: `cat /tmp/helloworld.txt` and you should see:
{% highlight ruby %}
[root@sample /]# cat /tmp/helloworld.txt
Hello World!
{% endhighlight %}

Now, what do some of the keywords mean?
`- name:` basically is the name of the playbook (not the file).
`hosts:` is the hosts for the playbook.
`tasks:` all the tasks/commands to execute on the server

Hope this was helpful! Thank you and hack on! =)