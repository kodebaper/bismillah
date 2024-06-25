+++
title = 'SVG Path Icon for Hugo Static Website'
date = 2024-06-25T16:15:00+07:00
description = "in this article I will discuss blog optimization to improve the performance of faster blog access, I follow these tips from the results of a speed test on the Google speed test"
tags = [
    "tips&tricks",
    "programming",
    "static-website",
    "hugo-static",
]
categories = [
    "programming",
    "hugo-static",
    "bloging",
]
series = ["Themes Guide"]
aliases = ["static-website"]
image = "svgpath.jpg"
+++


### main topics
In this article I will discuss blog optimization to improve the performance of faster blog access, I follow these tips from the results of a speed test on the Google speed test, then I follow every optimization guide that must be done. One of them is here. I did an optimization that slowed down access to my blog due to the svg file that I used in the blog content.


Then how to overcome all this?
---


What I did was, I had to find a solution to using image files in the SVG format, which I apply a lot on blogs, which causes slow blogs, but it needs to be underlined that using SVG format files is actually much better than using JPG or PNG format.


to overcome this all I have a solution, ie***my-export*** the svg file that I used then***my-import*** that svg file uses SVG PATH CODE. The application that I use is the application*open sorece* named***GIMP (GNU Image Manipulation)*** to convert SVG formatted image files into path code.


### What's the result?
I found that the blog increased in performance when tested using it***Google Speed***. Then below I will explain how to use the application***GIMP*** to convert an SVG format image file to a file**PATH**


1. First, here I assume that everyone has installed the Gimp application on their respective laptops or computers.


2. Next, you open the SVG format file which will be imported into the file**SVG Path Code**


3. Once open, then select the menu***WINDOWS -> Docable Dialogs -> Path***


4. After the third step, look at the lower right corner next to the image there is a menu path like the image below.

`````
![import file svg to path file](/images/pathicon.png)
``````

5. Select on the section**+** which is at the bottom henceforth a menu will appear to change the file name, then replace the file name with what you want.


6. Then right-click on the layer in the path menu on the lower right, then select**Import Path**, then find the image file that was selected earlier.


7. After that, right-click again on the image that is in the path menu but in this step select it**Export Path**, then specify the location where you will save this file.


8. Finally open the file that was just in**Export** with your favorite text editor application.


9. You can use the result code**Export** that is to be included in articles or property features of your website or blog.


Hopefully this article is useful, happy learning!