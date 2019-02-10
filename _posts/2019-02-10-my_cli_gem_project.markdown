---
layout: post
title:      "My CLI Gem Project"
date:       2019-02-10 17:19:19 +0000
permalink:  my_cli_gem_project
---


So today I will be explaining my CLI gem and my thought process behind the build. First off I wanted to pick a website to scrape that I was interested in scraping. So I thought to myself wouldn't it be great to scrape all the snow reports of the different ski resorts and be able to display a report for each ski resort. So this then started a thousand ideas that were spinning in my head. 

It took me a couple of attempts to get the final product because I ran into one really big issue which was the main page I wanted to scrape from was Unscrapable! The reason being the table I wanted to scrape was initially blank and populated by a script. This then sent me spiraling on created one of two gems. I first thought iIwould just manually scrape each direct link to the actual snow report page. This was a lot of code and I got them gem working this way but this wasnt the way I wanted my finished project to look. So I then started just adding all the pages links to an array and itterating through that array to scrape all my reorts. All though I was still getting all the live info I needed and the CLI worked, this was still to messy for me and I didnt like it.

This took me to creating a whole other gem. So instead of scraping from all the different websites of snow reports. I went back to that unscrapable index page with the list of all the resorts. Instead of scraping the page I copied all all of the HTML and created a index.html file within my gem. I created a working gem that scraped all of my report attributes directly from the index.html but this wasnt live information. The only way this would show a current snow report for each of those resorts is if I manually changed that index.html file myself every day which I was definitley not interested in doing. 

So I then was sitting there with these two working gems trying to figure out which one was the better of the two to complete my project with. I kept getting frustrated because neither really were good enough for me. So I then had the aha! moment. I said to myself why dont I just take the two gems and combine them to create one great gem. I started thinking to myself how I would go about doing this. I realized I could use some of the information in the index.html to further get all the live attributes from each of the resorts live snow report page. So I scraped all the end of the links from the index.html attached them to the rest of the link and shoveled them onto an array of links. I then needed to go another link deeper to get to my snow report page that I wanted to scrape. So I scraped each of those pages and shoveled onto another array the links I wanted to give to my report objects.  I then created new report objects each with a link attribute for each link in that second array of links. I then scraped all report objects by there links and got there attributes. This then gave me the final product that I was satisfied with. I had a working gem where I didnt have to manually input all the links manually and I had live attributes that change on a daily basis.

If you would like to check out my gem click here: [My Gem - resort_report](https://github.com/mikeygbd/resort_report)

If you would like to see a short walkthrough of my gem click here: [My Gem - resort_report](https://www.youtube.com/watch?v=U_7OQO0neP0&feature=youtu.be)



