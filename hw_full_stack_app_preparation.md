# Homework: Full Stack Games Hub App

### Learning Objectives

- Understand the relationship between client, server and database
- Be able to navigate a codebase that you haven't written

## Brief

Your boss has asked to you look over the codebase of a full-stack JavaScript application. The front-end is written in JavaScript using Vue, the back-end uses an Express server and a MongoDB database. Your task is to make yourself familiar with the codebase.

The application includes a README.md with instructions on running the application.

![Overview of the tech stack and tooling with commands](images/tech_stack_with_commands.png)

*Overview of the tech stack and tooling with commands*

## MVP

### Task

Draw a diagram showing the dataflow through the application starting with a form submission, ending with the re-rendering of the page. This will involve a multi-direction data-flow with the client posting data to the server and the server sending data back to the client with the response. Detail the client, server and database in the diagram and include the names of the files involved in the process.

### Questions

1. What is responsible for defining the routes of the `games` resource?
server.js using routers create through create_router.js
2. What do you notice about the folder structure?  Whats the client responsible for? Whats the server responsible for?
The file structure is spit into two - one server and one client with the db falling under the server. Client is responsible for user view and passing user input to the server. Server is responsible for sending requests to the database and fetching data.
3. What are the the responsibilities of server.js?
server.js is responsible for creating the database connection and fetching and retrieving data for routes.
4. What are the responsibilities of the `gamesRouter`?
the games router is the controller routing data to the client depending on the route provided.
5. What process does the the client (front-end) use to communicate with the server?
It uses api requests.
6. What optional second argument does the `fetch` method take? And what is it used for in this application? Hint: See [Using Fetch](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch) on the MDN docs
It takes an init argument which is an object that defines custom settings of the fetch request e.g. credentials or redirect information.
7. Which of the games API routes does the front-end application consume (i.e. make requests to)?
http://localhost:3000/api/games/ and http://localhost:3000/api/games/:id
8. What are we using the [MongoDB Driver](http://mongodb.github.io/node-mongodb-native/) for?
It allows the server to interact to the database through an api.

## Extension

Why do we need to use [`ObjectId`](https://mongodb.github.io/node-mongodb-native/api-bson-generated/objectid.html) from the MongoDB driver?
This is used to specify id's in mongodb - this is their format.

Add to your diagram the dataflow for removing a game.
