## Reading list
In this course we will create an Express [Rest API](https://searchmicroservices.techtarget.com/definition/RESTful-API) for the backend of our own [9gag](https://9gag.com/) clone. We will make use of [HTTP methods](https://spring.io/understanding/REST).

We will also use some basic SQL: [SQL select](https://www.w3schools.com/sql/sql_select.asp), [SQL select where clause](https://www.w3schools.com/sql/sql_where.asp), [SQL update](https://www.w3schools.com/sql/sql_update.asp)

//Please read all the links and try some SQL exercises from the w3school links
---
Today we will build [9gag.com](https://9gag.com/)
---
Where do we start?

Let's break it down
---
We will have to get the jokes from somewhere

We will have to post the jokes to somewhere

Where is somewhere?
---
The database!
---
![database, server, client](http://afterhoursprog.wpengine.com/wp-content/uploads/2014/09/webFlowWithDatabase.gif)
---
Let's have a look at the database.
Go to [www.phpmyadmin.co](http://www.phpmyadmin.co)
```
Server: sql7.freemysqlhosting.net
Username: sql7253327
Password: siuhUBG93p
Database: sql7253327
```
---
Clone the [NodeJS course](https://github.com/HackYourFutureBelgium/NodeJS_course)
```
git clone https://github.com/HackYourFutureBelgium/NodeJS_course.git
cd NodeJS_course/course_2/9gag/client
npm install
npm start
```
---
Let's setup the server
```
mkdir server
cd server
npm init -y
npm install express --save
npm install nodemon --save-dev
```
create file: index.js

add following statement in the script tag of package.json
```
"start": "nodemon index.js",
```
---
let's do the regular setup we learned last week
---
install the [MySQL npm package](https://www.npmjs.com/package/mysql)
---
let's connect to the database.

Create a file named: connection.js and follow these [instructions](https://www.npmjs.com/package/mysql#introduction)
---
Requirements to get all the jokes
```
route path: /get/jokes
callback: [
  {
      id: 1,
      title: "",
      image_location: "",
      up_votes: 0,
      down_votes: 0
      upload_time
  },
  {
    ...
  },
  ...
]
ordered by "upload_time"
```
---
Requirements to upvote a joke
```
route path: /update/joke/upvote
post variables: { jokeID }
callback: {
  status: "succes",
  message: "joke upvoted"
}
```
(Make variation for downvote)
---
Requirements to upload a joke
```
route path: /post/joke
post variables: {
  title,
  file: {
    base64,
    type
  }
}
callback: {
  status: "succes",
  message: "joke uploaded"
}
```
---
Requirements to get a single joke
```
route path: /get/joke/:id
callback: {
  id: 1,
  title: "",
  image_location: "",
  up_votes: 0,
  down_votes: 0
  upload_time
}
```
---
HOMEWORK
---
Requirements to get comments per joke
```
route path: /get/comments/:jokeId
callback: [
  {
    id: 1,
    joke_id: "",
    username: "",
    text: "",
  },
  {
    ...
  },
  ...
]
```
---
Requirements to post a comment
```
route path: /post/comment
post variables: {
  text,
  username,
  joke_id
}
callback: {
  status: "succes",
  message: "comment posted"
}
```
---
