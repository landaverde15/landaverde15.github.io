---
layout: post
title: "Need to know Yarn Commands"
date: 2020-10-09 07:00:00 -0700
---

Hello everyone! If you've read my previous 5 blog posts (0-4), you know that I'm a ReactJS developer, and from time to time I touch server side code at my job. If this is the first blog post you, it's ok. Now you know I'm a React developer and I honestly love the library (not a framework).

If you're new to React I will list a few important Yarn commands that will help you in your React development. 

===> `Yarn add (package)`

This is a really important command because it allows you to add packages to your project. Let's say you want to consume a nice tool like ChartJS that provides really cool Charts for your front end. You would need to run `yarn add chart.js` . Then you'd be able to use the ChartJS package within your React project.

===> `yarn` or `yarn install`

This is another really important command. This command can be ran with either `install` after the `yarn` or just the `yarn`. It still will understand. The reason this is important is because let's say that the React project I created has a bunch of packages that I imported into it like ChartJS, CalculatorJS, and so on and so forth. The list of packages for my React project gets really long. If I gave another developer access to my project they would just download the React project and run the `yarn` command. All the packages like ChartJS, and CalculatorJS, and so on would be downloaded for you to develop in your environment.

===> `yarn audit` 

This is a good command to run especially if you download projects online and don't know about the developer who published it. `yarn audit` will check all the packages installed into the project and check for security issues with those packages. If issues are found it will list it out.

===> `yarn autoclean`

This is another good command because it removes all the unnecessary crud within the installed packages in the project. Lets say ChartJS installed files that are not important into my React project, then `yarn autoclean` will remove these unneeded files.

===> Conclusion

The list of yarn commands is really expansive and each command is extremely helpful and can benefit your React development in many ways. If you would like to learn more commands you can do so [here][yarn commands]

Hope this was a helpful blog to the beginner React developers. Hack on!

[yarn commands]: https://classic.yarnpkg.com/en/docs/cli/