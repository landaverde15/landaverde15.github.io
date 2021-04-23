---
layout: post
title: "Performing fetch in ReactJS"
date: 2021-03-26 10:10:00 -0700
---

For blog 4 I've decided to explain on making an HTTP fetch call via ReactJS. How did I come up with this idea for this blog? Well originally I had planned to create out groups web application in GoLang, however, as I started developing the web app I approached several hurdles. Since I don't have experience with GoLang I decided to abandon that idea and create the web app in ReactJS which is the day to day language I use at work. To understand this blog it is expected to have atleast a beginner level knowledge on ReactJS.

The most common cases to make an HTTP request would be in your initial page load state of your application, so the data can be fetched and then displayed in the DOM. In React this would be performed inside the `componentDidMount()` function of the component. In earlier versions of React it could've also been done in the `componentWillMount()`, however that function is now heavily recommended NOT to use and will probably be deprecated.

Performing the fetch within `componentDidMount()` will look something like this. For purposes of this blog I will make a request to a sample candy store API:

{% highlight ruby %}
    componentDidMount() {
        fetch("http://candy.api.com/candies")
        .then(res => res.json())
        .then((result) => {
            console.log(result);
        });
    }
{% endhighlight %}

If this API were real and the fetch were successful we should expect something like the following:
{% highlight ruby %}
    ["snickers", "kitkat", "butterfingers", "jolly rancher"]
{% endhighlight %}

Simple as that we can make an HTTP request. Now you say what is the `then()` attached to the fetch function. `then()` is from the Promise API. It is used to deal with asynchronous tasks like in this case the API call. When the candy API responds, the `then()` allows developers to specify what to do right after the previous function has executed and completed. In the sample above we are console logging the result.

