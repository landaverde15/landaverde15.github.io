---
layout: post
title: "Tips on using State in ReactJS"
date: 2021-04-09 10:10:00 -0700
---

ReactJS is an extremely nice front end library (not a framework). What's is so cool about ReactJS is the customization of components and the use of state. So what is exactly is state?
State are variables that are managed by a component. Props in the other hand are variables passed in from a parent component to a child component. This is neat because a parent component can make a fetch to an external API and the child component can receive the props or data and populate the DOM with the data. So how does this look in React code?

{% highlight ruby %}

class Blog6ParentComponent extends React.component {

    constructor(props) {
        super(props);
        this.state = {
            sampleData = this.props.dataFromExternalParent
        }
    }

    render() {
        return(
            <Blog6ChildComponent data={this.state.sampleData}/>
        );
    }
}

{% endhighlight %}

As you can see in the code above, state is initialized within the constructor method. Then the value for the state variables are props (or in easier terms variables passed in from parent). Then when props get saved into the state, state data can be passed into child components as well. One important thing to note is that passing data in ReactJS has only 1 directions. From parents to children, and NOT children to parent. So if data gets updated in the child component and the child component wants to return the updated data to the parent it cannot do this. There are other forms of doing this which will be discussed in another blog.

