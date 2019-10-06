---
layout: post
title:      "useEffect Hook"
date:       2019-10-06 20:33:33 +0000
permalink:  useeffect_hook
---


I recently learned the useEffect hook in React Native and think that I will be using this hook quite a bit in the future. useEffect can be used for multiple reasons for instance if you want to run an arrow function only when the component is first rendered you would simply import useEffect with React and useState:

![https://i.imgur.com/wLsmGb5l.png](https://i.imgur.com/wLsmGb5l.png)

and then create a useEffect arrow function with a second argument of an empty array like so:

![https://i.imgur.com/w7Whgrb.png](https://i.imgur.com/w7Whgrb.png)

Then call a function within this arrow function to make that function run only when the component is first rendered :

![https://i.imgur.com/mvnU5gj.png](https://i.imgur.com/mvnU5gj.png)

This will run the searchApi function with the argument of 'pasta' when the component is first rendered and will not continue to loop this call to searchApi.
