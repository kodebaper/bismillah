+++
title = 'How to Create an Alternative Article in Hugo Static Website'
date = 2024-06-26T10:07:19+07:00
description = "as a blogger who uses Hugo's static site as his blog engine, but this time I was faced with a different situation where writing articles on a blog using Hugo simply uses a text editor"
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
image = "articletips.png"
+++


### main topic
as a blogger who uses Hugo's static site as his blog engine, but this time I was faced with a different situation where writing articles on a blog using Hugo simply uses a text editor. I will update this article with a more complete discussion at a later time with other tips on how to write articles on Hugo, while the tips that I wrote at this time are still limited to the whole ones that I use in writing on my current blog.


To remind you again, previously all of our article files or writings on the Hugo blog would be stored in the directory <font size="4" color="red"><b>**content**</b></font> with the file order like this


       [Hugo blog]
                   ---> [content]
                             |
                        [blog/post]



The way to write articles on blogs that use hugo / create articles through a text editor is as follows:


### Include image files


I usually use this script when we want to include a picture in an article post


     <img src="/images/namagambar.png" align="center"> 


all we have to do is adjust the image files where we will call them later using this script, usually the template folder will be stored in the static folder then the images folder where the image assets are stored.


## Create a form script text


I call it like that, because to be honest I'm still having a hard time and I haven't found an article that discusses writing articles on Hugo. Okay, so we use this to make the writing in black form, usually in articles there are times when we want to write a script between the posts in the article, we need to make it different from normal writing.


to make it very easy, we simply advance the writing/script that we will enter into the black form by pressing the Tab key 2x then writing or pasting the writing.


## Mark text with rounded dots


For this one I usually use it to describe many sub-subheadings, for example I'm describing the types of the Debian linux operating system and its derivatives, so I will mention the Debian operating system by starting [ROUND POINT] before the name of the operating system, an example is as follows.


- Linux Ubuntu


- Linux Mint


- Kali Linux


- etc


Can you see the round dot before the word "Linux" ? well I mean like that. For bloggers
To make it very easy, we just need to give a sign **[-]** before the sentence we will give a round dot


## Makes the title underlined


In this function I will give tips on how to make a large underlined title in the article or subtitles in each post. For more details, for example like this, I embed sub-headings in each article.


## example subtitles 1 line
## example subtitles 2 lines


Like this, as for making it also simple, namely giving a sign **[##]** in any desired title. for more details see the picture below.


But if we don't want a line under the title, then we just need to remove one mark**#** before the title. Thus, for this article, I will end it here and in the future I will update other tips on how to write articles on blogs using Hugo ssg. Hopefully this article is useful, happy learning!