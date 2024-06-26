+++
title = 'Git Push Rejected Non Fast Forward'
date = 2024-06-26T10:23:03+07:00
description = "a few days ago I had an error after doing a custom domain on the github page, where when I made changes to this blog and wanted to update the changes by pushing the results of the changes to the github repository but was rejected"
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
image = "gitpush.png"
+++


### main topic
a few days ago I had an error after doing a custom domain on the github page, where when I made changes to this blog and wanted to update the changes by pushing the results of the changes to the github repository but was rejected, more or less for the error message as below :
 
The git command for to push changes as follows
      
   # git push -u origin master    
 
At this step I got an error something like this :
 
   error: failed to push some refs to 'https://github.com/santricyber/santricyber.github.io.git'
   hint: Updates were rejected because the remote contains work that you do
   hint: don't have it locally. This is usually caused by another repository pushing
   hint: to the same ref. You may want to first integrate the remote changes
   hint: (eg, 'git pull ...') before pushing again.
   hint: See the 'Note about fast-forwards' in 'git push --help' for details.

### solved
A little explanation from what I read from Stackoverflow for this case, that the changes from the blog to be pushed to the github repository were rejected because there were indications that another repository was pushed to the previous repository, here maybe the reason I made changes to the `.toml` where I changed my domain was `https://santricyber.github.io` to `https://santricyber.com`. But there is no need to worry because here there is a short solution via the command below.
 
   git fetch origin master:tmp
   git rebase tmp
   git push origin HEAD:master
   git branch -D tmp
 
after this is entered it's time for us to test by making changes again to the blog, then as usual push again to the Github Page in the following way:
 
   hugo
   cd / public
   git add .
   git commit -m "push notes"
   git push -u origin master
 
then for this stage it should be able to run normally, so this article I hope this is useful!