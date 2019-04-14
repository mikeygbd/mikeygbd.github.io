---
layout: post
title:      "Omniauth and Devise."
date:       2019-04-14 16:02:26 +0000
permalink:  omniauth_and_devise
---


So I thought this project would be a breeze much like the sinatra project was for me but I was far from wrong. It took me a while to figure out what exactly devise was doing for me. I quickly realized that i needed to overide devise in many occasions. I first had to overide the redirects i was getting from devise to my welcome page by adding this code to my application controller: 
`   def after_sign_in_path_for(resource)
      "/users/show"
   end`
	 I also had to overide all of my destroy routes aswell in my routes.rb file.
	 
	 
	 Omniauth
	 
	 First off I wasn't able to see my omniauths working because I had to delete my browser history everytime I logged in using them. Also for some reason my console had it redirecting to my signup Page but on other consoles it works fine redirecting to the users show page. So not really sure what my console was doing differnetly. So i had to try to delete the whole file locally and just clone it down from git up.


