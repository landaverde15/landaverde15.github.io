---
layout: post
title: "Arrow Functions in TypeScript"
date: 2020-09-09 10:10:00 -0700
---
For Blog 1 I have decided to share some information on Arrow functions in TypeScript and explain how to use them. Before continuing to read this blog post, it is assumed that you (the reader) are familiar with TypeScript. If you aren't, it is completely fine. I can quickly exlplain what TypeScript is.

===> What is TypeScript?
TypeScript is basically JavaScript but much better (or on steroids). What I mean by this is that TypeScript supports other JS libraries, understood through various browsers, and when compiled is simply plain JavaScript. So what difference is it from JavaScript? The syntax. The reason some developers prefer TypeScript is because of its compilation, strong static typing, OOP, and type definitions. **_To put it all plain and simple, developing in TypeScript helps the development process to avoid bugs_**.

===> What are Arrow Functions?
Arrow functions are like any other Javascript/TypeScript function but just syntactically different. I enjoy Arrow functions because it just makes the code look much nicer and cleaner. I will start by explaining a basic hello world regular function.
{% highlight ruby %}

var myFunction = function (greeting) {
    console.log(greeting);
}

myFunction("hello world!");

// ------------------------
    returns 
        hello world!
// ------------------------
{% endhighlight %}

For regular functions as desplayed above, a variable is declared called `myFunction`. This variable will be a function that takes in a parameter of greeting which essentially will be a string containing 'hello world!'.

Now let's take a look at arrow functions below:
{% highlight ruby %}

let myFunction = (greeting:string) => {
    console.log(greeting);
}

myFunction("hello world!");

// ------------------------
    returns 
        hello world!
// ------------------------
{% endhighlight %}

In creating an arrow function, we will approach it the same way. Creating a variable called `myFunction`, however we don't need to specify the term `function`. What is cool about arrow functions is that just by using the parenthesis and the arrow and curly brackets (`() => {}`), the browser will already understand it's a function. If you want to pass parameters to a function you would do so by providing it inside the parenthesis just as a regular function.

Try it out and see how fun and easy it is to use Arrow functions. I'm sure you will start implementing it in future development!