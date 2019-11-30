---
layout: post
title:      "bottomTabNavigation"
date:       2019-11-30 23:37:59 +0000
permalink:  bottomtabnavigation
---


There are mutiple ways to design your bottom tab navigation. one of the easiest ways is to use navigation options on each screen like so and giving your tab a title like so:

![https://i.imgur.com/KZC2fmK.png](https://i.imgur.com/KZC2fmK.png)

And you can add an icon simply by importing from expo vector icons:

![https://i.imgur.com/zIe3rnW.png](https://i.imgur.com/zIe3rnW.png)

Then adding a tabBarIcon:

![https://i.imgur.com/4NiiIRKh.png](https://i.imgur.com/4NiiIRKh.png)

giving you the end result of something like this:

![https://i.imgur.com/HdVTDEwl.png](https://i.imgur.com/HdVTDEwl.png)

Now this method is nice but I prefer using createMaterialBottomTabNavigator from 'react-navigation-material-bottom-tabs' within App.js so that way you have all of your navigation within App.js instead of within each screen. First you would have to npm install, expo install or yarn add  'react-navigation-material-bottom-tabs'. then import it into App.js:


![https://i.imgur.com/eOOSZcG.png](https://i.imgur.com/eOOSZcG.png)

Then Wrap your navigation within a createMaterialBottomTabNavigator:

![https://i.imgur.com/WH0GW31.png](https://i.imgur.com/WH0GW31.png)

Insert your screen with its navigation options:

![https://i.imgur.com/iPdW5kKh.png](https://i.imgur.com/iPdW5kKh.png)

You can also add other otions like activeColor, InactiveColor and barStyle:

![https://i.imgur.com/IS7VqKMh.png](https://i.imgur.com/IS7VqKMh.png)

If you need to do a stack Navigator you simply have to make a constant and pass that constant in as the screen:

![https://i.imgur.com/eWIRF01h.png](https://i.imgur.com/eWIRF01h.png)

And then pass it in like so:

![https://i.imgur.com/Td3yumVh.png](https://i.imgur.com/Td3yumVh.png)

In conclusion I think that Material Bottom Tabs are way mor functional and easier to use.


