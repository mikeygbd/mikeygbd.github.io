---
layout: post
title:      "useEffect Clean Up Function"
date:       2019-11-25 02:36:48 +0000
permalink:  useeffect_clean_up_function
---


useEffect has a lot of good uses and can come in handy as a hook but it also can slow down or even crash your application if your not careful. I very simple way to make sure that doesn't happen is by using a clean up function at the very end of your useEffect. Lets say you are using useEffect to get a users location like so:

![https://i.imgur.com/U38mKXYl.png](https://i.imgur.com/U38mKXYl.png)

This works great but everytime the callback function changes we are calling startWatching and running this chunk of code again to expo:

![https://i.imgur.com/HXgPSdEl.png](https://i.imgur.com/HXgPSdEl.png)

This could be asking for a listener everytime the callback changes and slow down the application quite a bit. So in order to fix this we would use a clean up function by simply returning a function at the very end of the useEffect hook to make sure you remove the listener like so:

![https://i.imgur.com/AELZ0o2l.png](https://i.imgur.com/AELZ0o2l.png)

with an end result looking like this:

![https://i.imgur.com/mqdLDmpl.png](https://i.imgur.com/mqdLDmpl.png)



