---
toc: true
layout: post
title: Pickup Station - Express JS Reflection
description: A relfection and guide on how to create a project using express JS
---

# Introduction

For our pickup station project, we decided to try something new and create a website using Express JS. This was a new experience but there were a lot of similarities between it and aspects of our java projects and python projects. 

## Creating an EJS Server

There were quite a few steps required to set up, such as making dockerfiles and docker-compose files, but the main thing we needed to do was create an express server. This was done by creating a new file called server.js and adding the following code:

```javascript

// import app and mongoose
const express = require("express");
const app = express();
const mongoose = require("mongoose");
require("dotenv").config();

app.set("view engine", "ejs");
app.use(express.urlencoded({ extended: false }));
app.use(express.static("public"));
app.use(express.json());

mongoose.connect(process.env.MONGO_URL, {
  useNewUrlParser: true,
  useUnifiedTopology: true,
});
mongoose.connection.on("connected", () => {
  console.log("Mongoose is connected");
});

```

Note that above, there is also a mention of mongoose. This is something we chose to use to connect to a database called mongoDB, which made it really easy for us to have a database hosted separately from this deployed project and made it easy to sort through and avoid any conflicts (as in previous projects there were many merge conflicts when having a database in the same project).

## Creating MongoDB Schemas

Here is an example of a MongoDB schema. This is a schema for a user, which is used to store information about a user such as their name, email, password. This is then used to create a new user in the database, which can be used to login and access the website.

```javascript
const mongoose = require("mongoose");

const userSchema = new mongoose.Schema({
  fullName: {
    type: String,
    required: true,
  },
  email: {
    type: String,
    required: true,
    unique: true,
  },
  password: {
      type: String,
  },
  createdAt: {
    type: Date,
    default: Date.now,
  }
});

module.exports = mongoose.model("Users", userSchema);
```

This tells the database what a user should have, and then we can import the user into server.js and use it using these lines:

```javascript
const User = require("./models/user");

// make sure to define email, password, and name variables
const user = new User({ email, password: hashedPassword, fullName: name });
```

## Rendering Views

Rendering views is pretty simple, we just need to create a new folder called views and then create a new file for each page. For example, if we wanted to create a page for messages, we would create a file called messages.ejs and then we could render it using this code:

```javascript
app.get("/messages", (req, res) => {
  res.render("social/messages");
});
```

## Creating Routes

This is where we felt it was more similar to python than the java projects, it seemed very close to the python layout. In our server.js, we would define our routes and what method they use. For example, here is how you would define an async register post method:

```javascript
app.post("/register", async (req, res) => {
    // function goes here
});
```

## Summary

With all of this, put together, you can create a website using express JS. It was a new experience for us so it took a bit to figure out how everything worked, but it quite interesting to do something different from a standard Java project this year. Maybe you can use this for data structures next year as a way to encourage students to build more javascript skills and try something new.

## Reflection - Daniel Tsivkovski

I believe that this year was a lot of learning for me. First of all, it was a lot of learning about Java, as Java was something I was completely unfamiliar with, but most of all was something I struggled with even during first trimester. It took me so long to finally learn the syntax of Java, as I struggled to understand the difference between public/private and static vs non-static. It especially was a struggle working with database stuff that I just didn't know how it worked - JPA stuff was so difficult for me but I figured it out eventually.

I think one of my weaknesses during this trimester was collaboration. It's difficult to communicate with people with such varied ideas, but it was especially difficult to communicate with some people with very different methods of work than me. I think, however, that my organization helped to facilitate some of my communication with the team through making issues and making sure everyone was able to figure out what to do. Aadit's indecisiveness on the project kind of threw me for a loop here, but it was another part of learning how to work with different perspectives. I'm glad we tried Pickup Station, as it was great to get to know how to use ExpressJS and the MongoDB system. I think it's a lot simpler than Java, there were less issues with it when setting up the backend, which I appreciated as I spent a lot of my time on the backend of the project.

I think my time at Chapman CS will be very good for me, as they have a thing called the Grand Challenges Initiative which is a 2-year long project that features collaboration with students from other engineering/STEM majors and is meant to cause a positive change in the community. I'm also excited because their engineering program is growing substantially and they are making a big push to promote it and increase its strength.

I think over the past two years, I have grown so much and clearly have learned a lot. I think I still need to work on communication and collaboration with a team, but I think having a fresh start at Chapman will help me to really feel confident in doing that. I appreciate all the help and guidance you have given me, Mr. M, and I think that without this class I never would have even thought about majoring in Comp Sci, I probably would have stuck with biochemistry or something similar.


