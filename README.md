# Homework 18: Social Network API

## Description

MongoDB is a popular choice for many social networks due to its speed with large amounts of data and flexibility with unstructured data. Because the foundation of these applications is data, it’s important to understand how to build and structure the API first.

This week's challenge was to build an API for a social network web application where users can share their thoughts, react to friends’ thoughts, and create a friend list using Express.js for routing, a MongoDB database, and the Mongoose ODM. In addition to using the Express.js and Mongoose packages, I've also used moment.js for the date library to format timestamps.

Because this application won’t be deployed, I've also created a walkthrough video that demonstrates its functionality and all of the acceptance criteria being met. Here is the walkthrough video link below:

- [Walkthrough](https://drive.google.com/file/d/1N8ZkSwIZUWR19EZhM2OqxAa6SC9GhJr1/view?usp=sharing)

## Installation

You'll need to **fork** or **clone** the Repo in order to run the application on Insomnia. Here is my Repo link for this application:
- [Social Network API](https://github.com/jasonchun7/hw-18-social-network-api)

## Usage

After forking/cloning to your local machine:

1. Open the command line in the root and `npm install` to install required dependencies (`express, mongoose, moment`)

3. `npm start` and open localhost:3001 on Insomnia.

## Tests:  

Testing restful API calls with Insomnia 

---
**`/api/users`**
- `GET` all users
- `POST` a new user:
    ```json
    // example data
    {
        "username": "lernantino",
        "email": "lernantino@gmail.com"
    }
    ```
---
**`/api/users/:userid`**
- `GET` a single user by its `_id` 
- `PUT` to update a user by its `_id`
- `DELETE` to remove user by its `_id`
---
**`/api/users/:userId/friends/:friendId`**
- `POST` to add a new friend to a user's friend list
- `DELETE` to remove a friend from a user's friend list
---
**`/api/thoughts`** 
- `GET` to get all thoughts
- `POST` to create a new thought
    ```json
    // example data
    {
    "thoughtText": "Here's a cool thought...",
    "username": "lernantino",
    "userId": "5edff358a0fcb779aa7b118b"
    }
    ```
---
**`/api/thoughts/:thoughtId`**
- `GET` to get a single thought by its `_id`
- `PUT` to update a thought by its `_id`
- `DELETE` to remove a thought by its `_id`
---

**`/api/thoughts/:thoughtId/reactions`**

- `POST` to create a reaction 
    ```json
    // example data
    {
    "reactionBody":"Hell Yeah!!",
    "username":"lernantino"
    }
    ```
---
**`/api/thoughts/:thoughtId/reactions/:reactionId`**
- `DELETE` remove a reaction by the `reactionId` 
