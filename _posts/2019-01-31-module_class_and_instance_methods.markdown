---
layout: post
title:      "Module Class and Instance Methods"
date:       2019-01-31 14:25:11 +0000
permalink:  module_class_and_instance_methods
---


When I  was first introduced to modules I was very exited because I new there had to be an easier way then writing the exact same methods in every class. Finally I had a way of passing the same methods to multiple classes without repeating my code in every class. Modules gave me the power to do so. 

The lessons on modules in the curriculum taught us that we can nest Class and instance methods within the same module which I really liked. When I got to my Music Library CLI and they had me create a module I got really confused on why they had me call my module like so Concerns::Findable. I found out that calling a module with concerns is common practice but my mind was boggled as to why. Then ofcourse the tests asked me to to put a couple class methods within this module so my classes could use them. So I wrapped them within a module ClassMethods within my Concerns::Findable because I thought this was neccessary so the class that I passed them to would know that it was a class method and not an instance method. I thought this was neccessary because class methods within a module don't need a self. in front of the method when defining it. So when I tried to extend my ClassMethods nested in my module my code was breaking because I couldnt add ClassMethods to my extend Concerns:Findable.  When I later found out that nesting them within a ClassMethods was unneccesary it was very troubling to me because I had no idea  how my classes diferenciated the methods between a class and an instance method without the self. .

I then had a aha moment when I realized that the word extend was doing that for me. It was telling my classes that the methods passed from Concerns::Findable were all Class methods. Had I did Include Concerns::Findable they would all be though to be instance methods by the classes. Then I realized  if you give a module two names like Concerns::Findable you can only have one type of method within it Class or Instance but not both. 



