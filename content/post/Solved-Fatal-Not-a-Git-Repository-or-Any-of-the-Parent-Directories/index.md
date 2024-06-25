+++
title = 'Solved Fatal Not a Git Repository or Any of the Parent Directories'
date = 2024-06-25T16:29:12+07:00
description = "where in this case I experienced a problem where the template that I wanted to clone from the templates made by other people could not be installed via git to my blog"
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
    "solved",
]
series = ["Themes Guide"]
aliases = ["static-website"]
image = "errorgit.jpg"
+++

### main topics
For me, documenting every error encountered in every lesson is very important, I am a beginner learning to build a blog using the Hugo static site, therefore documenting every lesson by writing it in a blog post is a must for myself where this will be useful in the future.


This is the umpteenth documentation, where in this case I experienced a problem where the template that I wanted to clone from the templates made by other people could not be installed via git to my blog.
The following is the error message that is displayed when I run the command to install the template on my blog, this is the command to install the template that I want to install on my personal blog.


	git submodule add https://github.com/gyuha/hago.git hago


This is the error message that is displayed after executing the above command


	fatal: Not a git repository (or any of the parent directories): .git


Then how to fix this error? The following is a solution to overcome problems with error messages like the one above.


	git init


Then try, run the command line again above to try to reinstall the template, it should work. An issue that might be too trivial for a quick fix for someone familiar with git commands, but not for a newbie like me.


The following is an explanation of the **<u># git init</u>** command where this command is used to create a repository in a local file which will later have a **.git** folder. I hope this article is useful, happy learning!