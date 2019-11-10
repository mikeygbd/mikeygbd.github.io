---
layout: post
title:      "Safe Area View"
date:       2019-11-10 18:00:00 +0000
permalink:  safe_area_view
---


A neat little fuction to react-navigation is SafeAreaView expecially in cases where you have no set header and don't want your screen to get pushed up behind the time and battery power of you phone. For example if your screen lookslike this:

![https://i.imgur.com/vK4SXepm.png](https://i.imgur.com/vK4SXepm.png)

SafeAreaView is very easy to use by just importing it from react-native  like so:

![https://i.imgur.com/YGAfAnXl.png](https://i.imgur.com/YGAfAnXl.png)


Then you will need to wrap your entire screen in SafeAreaView:

![https://i.imgur.com/B7MyOYBl.png](https://i.imgur.com/B7MyOYBl.png)

Then you will ad a prop called forceInset and set top to always:

![https://i.imgur.com/MXzHqhQl.png](https://i.imgur.com/MXzHqhQl.png)

This will take that pushed up screen and set it always into a safe area for the phone like so:

![https://i.imgur.com/ec8bQbDm.png](https://i.imgur.com/ec8bQbDm.png)

