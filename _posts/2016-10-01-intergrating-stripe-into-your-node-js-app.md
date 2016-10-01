---
layout: post
published: false
title: Intergrating Stripe into your Node.js app
---

## Introduction

Many a times where you may have contemplated integrating a form of payment system within your app. Maybe you 
want to help your friend set up her online shop to push some of the cool things she makes and you haven't the slightest clue about it.
Fear not. With Stripe and node.js, all this can be made possible, rather easily.

### Technical
Stripe needs no introduction to many of us. It has over its relatively short period of existence, managed to 
become synonymous with payment processing over the internet. Developers as well as many ecommerce sites all around the world have widely adopted it. 
It's popularity could be attributed to its dead simple integration within apps as well as the brilliant documentation 
supporting the API.

Now, on to getting our hands dirty.

For this tutorial, I will assume you have node.js and npm installed and configured for your development box.

We will now quickly set up our project by running the following commands within your project directory.

```sh
$ mkdir node-stripe
$ npm init
$ npm install express --save
```

Create our entry point, app.js and paste in the following code:

```javascript
var express = require("express");
var app = express();
var port = 3000; 

app.get('/', function (req,res,next) {
    res.send("Our simple stripe app works!"); //Type in quirky message
})

app.listen(port, function () {
    console.log("Magic happens at port " + port);
})
```

With that, run the app!

```sh
$ node app.js 
```

And you should see something similar to that quirky message you typed in :)

So far so good. Give yourself a pat on the back.

NOTE: BY all means, this is a simple example that implements no security whatsoever. 
You may want to look at [this article] for tips on how to secure your app as we go along.
Time to sort out our sample page that will have our super awesome stuff that we're selling.
