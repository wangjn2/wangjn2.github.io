---
layout: post
title: 购买GoDaddy域名设置GitHub Pages
date: 2018-03-12
tags: [GoDaddy, Github Pages, DNS]
---

Congrats, you’ve finally created a personal website that you want your own custom domain name instead of using gh-pages to host it. The process of connecting your domain to your gh-pages is quite simple. However, choosing the perfect domain name is the tricky part. I was very tempted to buy a “.ninja” extension, but ended up settling with an “.io.” Additionally, I was stumped as to whether to go with a nickname or my full name. In the end, I chose, kirstenswanson.io.

Github provides, some docs to wire up your domain with your gh-pages, but I’m going to cover the set up in 7 simple steps.

First, the most difficult part…decide on a domain name and buy it on GoDaddy (fingers-crossed you get the domain name you want and someone else hasn’t already taken it)
On the home page of your account the “My Products” tab is selected on default, which makes it easy to click on the “Manage” button

3. Scroll down to the bottom of the page and click the “Manage DNS” button


4. Within the DNS management page you will need to make three changes

In the Type “A” row update the IP address to: 192.30.252.153
(this will point your custom domain to GitHub’s server)
In the CNAME row with Name “www” input your gh-pages website (username.github.io)
At the bottom click the “ADD” button and make another Type “A” row with a different IP address of: 192.30.252.154
(don’t worry when you leave the page it will alphabetize the types)

5. Go to your editor and in the repository of your website create a new file named “CNAME” in the root of your directory


6. In the “CNAME” file add your domain name purchased from GoDaddy

7. Add, commit, and push your changes to Github

You can confirm that your DNS is set-up correctly by using the dig command in your terminal with your custom domain. You should see that your “A” Types point to the IP addresses that you had specified in GoDaddy’s DNS management page, in other words you’re pointing your DNS to GitHub’s server. Below is an example of the dig command:



If you’re encountering any problems, this GitHub Troubleshooting Custom Domains documentation is a good reference.

And just like that, you now have your very own custom DNS! As a side note, it may take some time for your DNS configuration to update, but after that celebrate and share your website! 🎉

