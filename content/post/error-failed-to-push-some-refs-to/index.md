+++
title = 'Error Failed to Push Some Refs To'
date = 2024-06-26T11:27:01+07:00
description = "Some time ago I had encountered an error when I was about to post the latest article"
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
image = "gitrefs.jpg"
+++


### Main Topic
Some time ago I had encountered an error when I was about to post the latest article, as usual I updated articles on this blog because I was still using the services from the GitHub page and I had no intention of moving to use the services from *Netlifiy* or *Forestry* because I felt I was still convenient for doing everything, be it updating the latest articles, improving the blog or making changes by pushing it to GitHub.

Okay, without intending to get further out of the topic of discussion in this article, I will continue my discussion, actually the error that occurred I myself don't know what caused it, because before I had never made any changes or activities before encountering this error. As usual, every time I post the latest articles or make periodic updates to changes to the blog, I always push to the GitHub Page with these 5 commands.

	# hugo
	# cd public/
	# git add .
	# git commit -m "your-commit-order"
	# git push -u origin master

From the commands I entered 1 to 4 it went as usual, but as soon as I entered the push command 5.
		
	# git push -u origin master

I get an error message like this.

	error: failed to push some refs to 'https://github.com/kodebaper/kodebaper.github.io.git'
	hint : Updates were rejected because the tip of your current branch is behind
	hint : 'git pul ...') before pushing again.

The error message is more or less like the one above, what I always do every time I encounter an error is I will start reading the error messages given one by one. Because almost every time we use the Git service, we encounter problems, in my experience, error messages are definitely included, which will make it easier for us to trace errors so we can fix them. Another tip to make it easier for us to understand error messages is to try to learn English because understanding and being able to speak English will make it easier for us in all respects, moreover, in my opinion, most of the articles on the internet are available in English or for reading documentation.

### Error can be resolved with this command

Finally I got a solution to overcome the problem as above so we can push back to update to GitHub Page, this is the script

	# git pull --rebase

And just using this command and problem is solved, I can push back to git, good luck!