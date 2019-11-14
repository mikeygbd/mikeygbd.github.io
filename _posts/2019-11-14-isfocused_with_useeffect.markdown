---
layout: post
title:      "isFocused with useEffect"
date:       2019-11-14 13:43:50 +0000
permalink:  isfocused_with_useeffect
---


Lets say you want something to track a users location on a certain screen on your application but when the user navigates away you want to stop tracking. Usually because you do not want to drain the users battery by tracking their location when not on the map screen. react-navigation come with a neat function called withNavigationFocus which allows you to see if the screen is in focus or not. Here is how it is used. 
First you want to import withNavigationFocus within react-navigation on the map screen:

![https://i.imgur.com/UpW6XOsl.png](https://i.imgur.com/UpW6XOsl.png)

Then you want to wrap your screen down at your export in the withNavigationFocus function like so:

![https://i.imgur.com/kdSgi0Ul.png](https://i.imgur.com/kdSgi0Ul.png)

After doing so you want to destructure out the isFocused prop giving you a boolean of true or false when the screen is in focused:

![https://i.imgur.com/EvBGrvrl.png](https://i.imgur.com/EvBGrvrl.png)

Now you want to pass in isFocused into your location tracking in this case my useLocation hook as my first arguement:

![https://i.imgur.com/lTiB0Jbl.png](https://i.imgur.com/lTiB0Jbl.png)

Now add that arguement into my useLocation hook but I change the name from isFocus to something that makes a bit more sense like shouldTrack like so:

![https://i.imgur.com/iEAoduXl.png](https://i.imgur.com/iEAoduXl.png)

The useEffect can be used for multiple reasons one for running something once when the component just renders by just adding a second arguement of an empty array:

![https://i.imgur.com/w7Whgrbl.png](https://i.imgur.com/w7Whgrbl.png)

But you can also use useEffect to run some code everytime an element changes. In this case I added the shouldTrack to the array giving me the ability to rerun useEffect everytime shouldTrack changes its value:

![https://i.imgur.com/zuzcApsl.png](https://i.imgur.com/zuzcApsl.png)

Now I simply add my logic on what I want useEffect to do every time its run:

![https://i.imgur.com/GrpKyuDl.png](https://i.imgur.com/GrpKyuDl.png)

Thats how you track a user on one screen but when navigated away from that screen it stops tracking and saves the user some battery life. 






