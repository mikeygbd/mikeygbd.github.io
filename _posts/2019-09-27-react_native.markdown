---
layout: post
title:      "React Native"
date:       2019-09-27 19:43:08 +0000
permalink:  react_native
---


I recently started learning React Native and the two are very similar and Native just has some differences that I very much like. My favorite thing I have learned so far is the useReducer hook and for some reason found this hook way easier to understand than creating different files for reducers as I would do in React. You simply have to import useReducer with react at the top like so:

![https://i.imgur.com/jsGPK7Ql.png](https://i.imgur.com/jsGPK7Ql.png)

Then create a const with state and dispatch set it to useReducer with 2 arguments your reducer and what you would like initial state to be like so:

![https://i.imgur.com/33WyWGwl.png](https://i.imgur.com/33WyWGwl.png)

Create your reducer function  with two arguements state and action and run a switch statement on your action types and either add some functionality by adding a ternary operator like I have done here:

![https://i.imgur.com/S2hzp7nh.png](https://i.imgur.com/S2hzp7nh.png)

 or simply use the spread operator to get the current state  and instead of destructively changing the state of red i set red to the current state of red and added the action.payload:
 
 ![https://i.imgur.com/u7t2RI2l.png](https://i.imgur.com/u7t2RI2l.png)
 
 and then simply apply it to your onChanges callback functions:
 
 ![https://i.imgur.com/2UxhQVCh.png](https://i.imgur.com/2UxhQVCh.png)
