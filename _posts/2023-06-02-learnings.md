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


