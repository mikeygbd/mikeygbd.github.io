---
layout: post
title:      "Van Builder - Sinatra Portfolio Project"
date:       2019-03-15 15:39:15 +0000
permalink:  van_builder_-_sinatra_portfolio_project
---

![](https://i.imgur.com/XafoM5St.png)

**The Idea**

The Idea came to me because I was curently in the middle of buying and installing parts to my sprinter van to turn it into a camper van. I was getting a little overwhelmed with keeping track of all the parts I had currently purchased, how much I had already spent and what parts I still needed to purchase to bring my van to completion.  I thought that this might be a perfect use for this portfolio project. 



**Table Outline**

At first it was a little tough to figure out the outline of the tables and which tables needed to be created. At first I thought the user would have many parts and have many vans but then I thought to myself that a user in this case would rarely have more than one van unlesse the user is some bitcoin billionare. So then I realized I needed to delete the vans table and give all the van attributes directly to the user. This gave the ability for the user to create his van attributes directly during sign up. I then just needed three tables: users, parts, and wishlist_parts. The user would then have many parts and wishlist parts and both the parts tables would belong to a user.



**Scraping For Thumbnail Images**

I wanted the user to be able to see a thumnail picture of the exact part they were adding to their parts list. So what I did was a google image search with all the parts attributes and I noticed that there was two locations that a slug of the search was inserted. So I created  a new slug with all the parts attributes and created a url variable with the link and the gsub'd slug inserted in. I then passed that url to the scrape_part method in PartsScraper which then scrapes for the image in the block. I then did the same for the users van image.



**CSS**

I have to say that 85-90% of the time I had spent on this project was toward the css. I had to do so many minor tweaks here and there to make everything look the way it does. As soon as I thought one view was perfiect I would find something else that needed minor tweaking and I would get lost in this tweaking tunnel for hours. I will probably continue down this rabit hole further to do some additional tweaking after the project is submitted because everytime I look at the application I find something that can be improved. 



**Conclusion**
    
All and all I had a lot of fun creating this project. The more it became an actual web application that I could personally use the more stoked I got. When I was nearing completion I couldnt believe I learned to create it in such a sort time. All thanks to FlatIron Scool!

