---
layout: post
title:      "Json Server and Negrok Setup"
date:       2019-10-18 20:51:10 +0000
permalink:  json_server_and_negrok_setup
---


Setting up a json server for your DB with Ngrok. You want to start by starting a new directory called jsonserver, change into that directory and then create a new package.json file by doing npm init. Then you need to install some node modules. With "npm install json-server ngrok" will give you all the node modules you will need. you then want to open up the directory in your code editor and start by adding a new file called db.json. In this file we want to tell the json server the different types of resources we want to manage. You want to insert an object inside that file and a key set to an empty array. For instance if you wanted to store your blog posts you would do something like this: 

![https://i.imgur.com/aSNgwoSl.png](https://i.imgur.com/aSNgwoSl.png)

Then we want to go to our package.json file and change the current scripts to this:

![https://i.imgur.com/rqTQB8Pl.png](https://i.imgur.com/rqTQB8Pl.png)

The json server uses the default of local host 3000. You then need to have two different terminal tabs. The first you want to type "npm run db" and this will start up the json server on port 3000. The second tab you will want to type "npm run tunnel". That will start up a tunnel for you and will run for 8 hours before terminating the session. You can then copy that forwarding address and see all your resources. 

Once this is all set up you now have to run 3 different terminal windows in order for this to work. One is for the react native bundler  started with:

![https://i.imgur.com/28loi1Hl.png](https://i.imgur.com/28loi1Hl.png)

Two is inside of the jsonserver directory with:

![https://i.imgur.com/w2JGfhml.png](https://i.imgur.com/w2JGfhml.png)

Three is also inside our jsonserver directory and is started with: 


![https://i.imgur.com/28loi1Hl.png](https://i.imgur.com/28loi1Hl.png)


