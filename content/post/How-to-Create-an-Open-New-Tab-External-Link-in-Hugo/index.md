+++
title = 'How to Create an Open New Tab External Link in Hugo'
date = 2024-06-25T23:17:19+07:00
description = "Here's how to create external link by hugo, so it's easy when we open a link on one page"
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
image = "hugoexli.png"
+++

### main topic
Here's how to create*external link by hugo*, so it's easy when we open a link on one page then the link we open will open in a new tab in the browser. The question is is this important? for myself this is important in terms of how far we will know the quality of the content on our blog or website, whether users like it or not. Where do you do it from? namely through monitoring the Bounce Rate on*Google Analytic*, now the function is to make external links to be able to open in new tabs will lower the number*bounce rate* quality on *Google Analytic*


As for the way like this, create a file named`render-link.html` in your theme layouts folder. The order goes like this`layouts/_default/_markup/render-link.html`,


````
layouts
   └── _default  
       └── _markup
           └── render-link.html
````


Then for the contents of the file`render-link.html` itself is more or less like this:

``````
   <a href="{{ .Destination | safeURL }}"{{ with .Title}} title="{{ . }}"{{ end }}{{ if strings.HasPrefix .Destination "http" }} rel="noopener noreferrer" target="_blank"{{ end }}>{{ .Text }}</a>
   
```````


Now if you make an external link in the content, then if the link is in *click* it will open in a new tab. Hope it is useful!