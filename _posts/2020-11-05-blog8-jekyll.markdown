---
layout: post
title: "Using AWS CLI"
date: 2020-11-05 07:00:00 -0700
---

Hello everyone! For this week's blog post I will touch a little on AWS CLI. This week's Lab was about setting up an EC2 instance and running an Apache server on it and rendering a custom HTML page. I have to say I really enjoyed this lab. It surprised me because networking is not my area of interest. To be quite honest I find it a bit boring. My area of interest in the computer science realm is software development. Anyway, after completing this lab it was really surprising to me that I had actually set up an EC2 instance in the cloud and I connected to it via my local laptop through the command prompt. That amazed me. Now, I will get into how I interacted with my EC2 instance that is in the cloud via my local laptop using the AWS CLI.

===> What is AWS CLI?
I think it is important to first go over what is the Amazon Web Services Command Line Interface (AWS CLI). AWS CLI is a tool to manage your AWS services. By downloading the AWS CLI you can configure and control multiple services from your command line. The steps would look something like: \n
------------------------------------------------------------------------------------ \n
**Run command**: \n
`ssh -i "cit480.pem" ec2-user@ec0-0-000-000-00.us-east-2.compute.amazonaws.com` \n
**Explanation**: \n
-`cit480.pem` = your private key \n
-`ec2-user` = user in instance \n
-`@ec0-0-000-000-00.us-east-2.compute.amazonaws.com` = Your public IPV4 DNS \n
-You may be prompted some questions after running the above command so answer \n
 accordingly \n
------------------------------------------------------------------------------------ \n

------------------------------------------------------------------------------------ \n
**Run command**: \n
`sudo yum install aws cli` \n 
**Explanation**: \n
-Depending on your linux distro for your instance you would install the AWS CLI. The \n   
 above command works for a CentOS Linux distro instance \n
------------------------------------------------------------------------------------ \n

------------------------------------------------------------------------------------ \n
**Run command**: \n
`aws --version` \n
**Explanation**: \n
-This is to check that the AWS CLI was successfully installed \n
------------------------------------------------------------------------------------ \n

From here on out you can access all your AWS services. For Lab 4 we had to make some configurations to our S3 buckets. I did this by running the following command: \n
`aws s3api list-buckets --query "Buckets[].Name"` \n 
The following is the actual response I get from my instance: \n
{% highlight ruby %}
[
    "cit480"
]
{% endhighlight %}

With AWS CLI you can manage literally everything. Since I've only consumed EC2 + S3 services, those are the only commands I know. In a future blog post I will get into other services.

Hack on!

