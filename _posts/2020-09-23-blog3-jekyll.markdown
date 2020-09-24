---
layout: post
title: "Tools I Use for React Development"
date: 2020-09-23 10:00:00 -0700
---
As mentioned in my previous blog post (blog 2), I mentioned about getting into React development since I was assigned a project at work which required it to be written in React. Within a couple weeks of getting into React development I have discovered some nice tools that help a lot. The tools I use are in the following:

===> Visual Studio Code (IDE)

I've always used Visual Studio Code as a text editor/IDE for all the development I do, but for React it is extremely nice because Visual Studio Code allows for thousands of plug ins. There have been talks of other IDE's dedicated to React like Reactide that are really great, however since I do full stack development and code in Java, I wouldn't like the idea of switching from Reactide to another IDE for Java. With the VS Code I can do all types of development.

===> React Developer Tools (Chrome Extension)

This extension was created by Facebook and to be honest it's a nice little tool to have. For the developers that like using the inspect feature for chrome, this extensions adds tabs for the HTML elements for your components/styling. The reason I like to use this tool is because it helps me to debug issues for individual components. You can download [here][react-chrome-ex]
![react chrome extension](/assets/ss1.PNG)

===> ES7 React/Redex/GraphQL... (VS Code Extension)

This nice to have extension for VS Code is very helpful. The reason I really enjoy this tool is because it allows for nice code snippets that help during development. In simple terms, it provides the option for short cuts when coding. For instance, typing the following prefix `imr→` will type out `import React from 'react'` automatically for you. This extension provides many prefix snippets to make your react development a breeze.
![react extension vscode](/assets/ss2.PNG)

===> npx create-react-app (NPM module)

This is a nice module/package because it helps to provide a nice already built React project for you to start your development. This saves you the time to set up babel/webpack which are external JavaScript tools for bundling up apps. Setting up babel/webpack on its own can be pretty stressful. And that's why I use create-react-app. To use this you need to have NPM version 5.2+ downloaded. Then you can run the following on your command prompt/terminal `npm install -g create-react-app`. Once it is done downloading you can start a react project by simply running `npx create-react-app nameOfApp`. You will be prompted some questions and have the option of answering them or simply pressing enter to skip them.

If you're new to React please use all of the helpful tools I stated above! =)

[react-chrome-ex]: https://chrome.google.com/webstore/detail/react-developer-tools/fmkadmapgofadopljbjfkapdkoienihi?hl=en


