---
layout: post
title: "Downloading Go and writing a simple 'Hello World' program (Windows)"
date: 2020-09-02 17:38:00 -0700
categories: jekyll update
---
For Blog 0 I will be explaining on how to download Go (GoLang) on a Windows machine. But, before I dive in, I will quickly explain what Go is and where it came from. Go is a programming language that over the past 5 years has been on the rise amongst developers and corporate companies for its simplicity and high-level efficiency. Go is continuously developed and maintained by Google.

=> Now. I shall dive in on how to download Go in your Window's OS environment:

1) Visit [Go's Download Page][golang-download] and click on the Microsoft Windows option. This should launch an msi file ad if not, directly go into your downloads folder and run the Go .msi file.

2) After you follow the window prompt, it's good to confirm that it was successfully downloaded. Open up Command Prompt and run the following command `go version`. If all goes well, you should get a response of something along the lines of `go version go1.15.1 windows/amd64`

=> Now, I will dive in on how to write a simple "Hello World" program and running this program.

1) Create a folder in your Desktop directory called `GoSample`

2) Open up the `GoSample` older using a text editor of your choice

3) In the text editor create a file called `hello.go` in the `GoSample` directory.

4) Within that file type the following:
{% highlight ruby %}
package main

import "fmt"

func main() {
    fmt.Println("Hello World!")
}
{% endhighlight %}

5) Save the file. Open up the command prompt and run the following command `go run hello.go` . Some things to keep in mind is to run this command while inside the `GoSample` directory. You should get a response that looks like:
{% highlight ruby %}
PS C:\Users\Path\to\directory\: go run hello.go
Hello World!
{% endhighlight %}

In another blog post I will explain what each line in the code means.


[golang-download]: https://golang.org/dl/