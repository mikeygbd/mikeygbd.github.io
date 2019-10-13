---
layout: post
title:      "React Native App Provider"
date:       2019-10-13 18:33:31 +0000
permalink:  react_native_app_provider
---


I recently learned how to use context instead of props and really like the concept of being able to bypass having to pass props from parent to child to grand child to great grand child and just make the context available from the App Provider. Yes it is a little more complex to set up then using props but can save you the headache when trying to pass props to a deeply nested child for instance If you wanted to make a blog. First you want to Import createAppContainer in your App.js file:

![https://i.imgur.com/KNBt889l.png](https://i.imgur.com/KNBt889l.png)

Then you want to create a constant called App and set it equal to createAppContainer and pass in the navigator:

![https://i.imgur.com/y9rPNu6l.png](https://i.imgur.com/y9rPNu6l.png)

Then you want to export a callback function and return the <App /> you just created:

![https://i.imgur.com/Oglq88Pl.png](https://i.imgur.com/Oglq88Pl.png)

After this you want to create a seperate folder for all your context files and add a file like BlogContext.js. You will want to import React so you can use the createContext function like so: 

![https://i.imgur.com/qHWjBggl.png![](http://)](https://i.imgur.com/qHWjBggl.png)

You'll Then want to create an exported Provider function with a destructured children prop and return the BlogContext.Provider wrapping the children prop. Then export default the BlogContext.


![https://i.imgur.com/Ab0HBKSh.png](https://i.imgur.com/Ab0HBKSh.png)

Then you want to return to App.js import and  wrap your <App /> being returned in your Provider function:

![https://i.imgur.com/gxwppFwl.png](https://i.imgur.com/gxwppFwl.png)
![https://i.imgur.com/X4JjCZKl.png](https://i.imgur.com/X4JjCZKl.png)

Now to test out your context you can simply pass in any prop for instance I passed in a value set equal to 5:

![https://i.imgur.com/jOSy74bh.png](https://i.imgur.com/jOSy74bh.png)

To use this context you can just import useContext in with react in a nested child:

![https://i.imgur.com/Mysd4fDl.png](https://i.imgur.com/Mysd4fDl.png)
![](http://)

Create a constant and set it equal to the useContext function with your context function being passed in:

![https://i.imgur.com/X84JPuSl.png](https://i.imgur.com/X84JPuSl.png)

You then can simply call that value within your view:

![https://i.imgur.com/phhwfTCl.png](https://i.imgur.com/phhwfTCl.png)

In conclusion using context instead of props is definitly more difficult to set up but once it is set up it is much easier to pass to nested children all over your application.






