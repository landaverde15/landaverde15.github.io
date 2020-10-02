---
layout: post
title: "Using Chart.js"
date: 2020-10-02 07:00:00 -0700
---
![chart js site photo](/assets/chartjs.PNG)

Have you ever had a project/assignment/client job where you were required to dynamically display data using graphs? Well, in my early days of development (3 years ago lol), I would manually build basic graphs using HTML, CSS, and JavaScript. During my early days of development I had no experience with packages, NPM, Node, etc. After years of experience I have found an excellent tool to display data via charts, graphs, you name it.

===> Chart.js
To learn about Chart.js you can visit [here][chart js url]. Chart.js is a simple nice to use JavaScript tool that you can use to implement in your project. You can either install via npm or download the source and include in script tag in your html.

When you have successfully included Chart.js into your project with the method of your choice (NPM/ Script tag), you will need to create a canvas element in your html. Something like this:

{% highlight ruby %}
    <canvas id="blog4" width="400" height="400">
    <canvas>
{% endhighlight %}

Then in your javascript file is where you will need input the data manually or dynamically. That is the beauty of Chart.js that it is easily customizable. If your data changes via AJAX calls then the Chart.js catches the changes. For this blog post I will place the data manually. In your JavaScript you will create the Chart.js instance like this:

{% highlight ruby %}
    // -------------------------------------------------------------------------
    // Sample data showing visitors for all my blog posts for this CIT480 course
    // -------------------------------------------------------------------------

    var chartjs = document.getElementById("blog4").getContext("2d");
    var myChart = new Chart(chartjs, {
        type: 'bar',
        data: {
            labels: ['Blog 1', 'Blog 2', 'Blog 3', 'Blog 4'],
            datasets: [{
                label: '# of Visitors',
                data: [12, 19, 3, 5],
                backgroundColor: [
                    'rgba(255, 99, 132, 0.2)',
                    'rgba(54, 162, 235, 0.2)',
                    'rgba(255, 206, 86, 0.2)',
                    'rgba(75, 192, 192, 0.2)'
                ],
                borderColor: [
                    'rgba(255, 99, 132, 1)',
                    'rgba(54, 162, 235, 1)',
                    'rgba(255, 206, 86, 1)',
                    'rgba(75, 192, 192, 1)'
                ],
                borderWidth: 1
            }]
        },
        options: {
            scales: {
                yAxes: [{
                    ticks: {
                        beginAtZero: true
                    }
                }]
            }
        }
    });

{% endhighlight %}

The code is very clear and understandable. The developer needs to specify the labels, in this case I used each of my blog posts. Then, you have to specify the datasets. In this case I used number of visitors for my blog posts. Then you can go on and customize the coloring.

Below is a preview:
![chartjs html](/assets/charthtml.PNG)

Now, go on and hack on!



[chart js url]: https://www.chartjs.org/
