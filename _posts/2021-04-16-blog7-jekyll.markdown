--- 
layout: post
title: "Using compenentDidMount and componentDidUpdate in ReactJS"
date: 2021-04-16 10:10:00 -0700
---

These are 2 functions that I have found important in my continuous learning in development in ReactJS. componentDidMount and componentDidUpdate. In the last blog post I spoke about state. To quickly summarize the last blog post - state are variables passed from parent components down to child components. Now this is very important because what if the parent receives new data and it needs to send it down to its child components. What is nice about ReactJS is that the Document Object Model (DOM) can be updated without refreshing the whole browser tab. So, how are these 2 functions important?

I'm going to explain their importance with a made up scenario. Let's say that in the initial load of our landing page, some data is fetched and then loaded onto the DOM. In this phase of the lifecycle we would use the componentDidMount() to load our data into the state of the component. Something like below:

{% highlight ruby %}

    componentDidMount() {
        console.log("Landing Page component has mounted");
        this.setState({
            data: this.props.fetchedData
        });
    }

{% endhighlight %}

As you can see above that as soon as our page loaded we are loading data into our state. Right when the component mounts onto the DOM we fetch the data. What if without refreshing the page, the data changes? How will the children components receive this updated data? We would then use componentDidUpdate(), something like below:

{% highlight ruby %}

    componentDidUpdate(previousProps, newProps) {
        if (previousProps != newProps) {
            this.setState({
                data: this.props.fetchedUpdatedData
            });
        }
    }

{% endhighlight %}

As you can see above componentDidUpdate() compares the old data with the new data. If the data has changed, then we want to load the new data into the components state.

