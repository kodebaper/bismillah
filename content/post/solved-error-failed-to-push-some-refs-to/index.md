+++
title = 'Solved Error Failed to Push Some Refs To'
date = 2024-06-25T21:59:19+07:00
description = "in this case, you just use this command below to solve the problem"
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
image = "gitrejected.jpg"
+++

### [SOLVED]

*error: failed to push some refs to*
! [Rejected] main -> main (fetch first) (blaaa…..blaaa... blaaa)

in this case, you just use this command below to solve the problem

$ git pull origin master -allow-unrelated-histories

and then you can try again to push your code .....

$ git push -u origin master

I hope this article is useful, happy learning!

