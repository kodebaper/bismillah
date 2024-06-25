+++
title = 'Preparation Before Deployment Hugo Static Website to Github Page'
date = 2024-06-25T22:16:19+07:00
description = "The following are things that need to be prepared before making a custom domain for this Hugo Blog"
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
image = "hugotogithub.jpg"
+++

### main topic
The following are things that need to be prepared before making a custom domain for this Hugo Blog, where I am doing this change or custom domain using the services of Github Page, as for the preparation as follows.

### 1. **Setting up the domain**

Make sure you have bought a domain, yes, if you are using a paid domain. here I document my preparations before doing a custom domain on the github page using a paid domain, I bought the `.com` domain at
**Domainesia** , this will also affect the DNS Management settings which later we have to change where in this case I changed my default nameserver from **Domainesia** to the nameserver recommended by cloudflare because I also use cloudflare for DNS management .

### 2. **Read Documentation**

This is very important, yes, you need to understand before doing a custom domain, because at this stage we will make some changes that you may not understand properly, such as understanding DNS management, what is changing nameservers to direct your initial domain to a new domain, you might I don't really understand CNAME settings, or SSL activation.

I have included the documentation here to serve as a guide for you to learn, yes, you need to understand, the method I use for the sequence is more or less so that you understand the sequence,

[I bought a domain ---> after my domain was activated by Domainesia --> I used Cloudflare for DNS management then I ADD DOMAIN on Cloudlfare ---> I made a nameserver change from Cloudflare to my Domainesia Dashboard --- > then I custom domain on the github page of the main repository]`

more or less the order is like this, then I will describe in more detail the steps for custom domain on the github page for my hugo blog on another occasion.

Here's the documentation that you can read to be your guide.

First guide:
https://docs.github.com/en/github/working-with-github-pages/configuring-a-custom-domain-for-your-github-pages-site

Second guide:
https://docs.github.com/en/github/working-with-github-pages/managing-a-custom-domain-for-your-github-pages-site	

I think these two documentation modals are enough, because they are very detailed and complete as a guide for customizing your domain on the github page.


### 3. **Already registered an account on the CLoudflare service**

We recommend that you first create an account at Cloudflare, it's very easy to create because it only requires an email for the registration process and account activation later. Then you are here using the *free* service provided by Cloudflare like I did, but for paid packages if you want it is also available. This preparation is important to speed up the custom domain process because after the domain we bought is active then we can immediately register our domain on the Cloudflare service.

That's all for this article, I highly recommend this preparation to be fulfilled in order to facilitate our learning process to experiment with Hugo and GitHub Pages. Hopefully this article is useful, happy learning!