# Canvasboard Server

GraphQL and REST API for Canvasboard with Strapi and Koa.

## Introduction

This repository is a dependency to run the Canvasboard. It contains all the models and routes necessary to manage the project.
It provides the user interface to administer the student and teacher registration received for Canvasboard, student assignments and submissions, grading and general project configuration.

## Getting Started

### Prerequisites

Ensure you have the following installed on your local machine:

- [NodeJS](https://nodejs.org/en/download/)
- [MongoDB Compass](https://www.mongodb.com/download-center/compass) (Optional)

### Usage ✨

_1._ `git clone https://github.com/Canvasbird/canvasboard-backend.git`

_2._ Navigate to the project's directory using: `cd canvasboard-backend`

_3._ Run `npm install` in the root directory to install the dependencies.

_4._ Now you need to connect to a database. To do this, duplicate the file .env.example into a new file called .env, and replace the content of the variables as described in the comments. You need to have a DB running before this. We recommend using MongoDB Atlas or Mlab. They both offer a free tier with up to 512MB free storage.

_5._ Now that you have a DB running, run `npm run develop` to start the server and watch for changes

_6._ It will serve a page under http://localhost:1337/admin so you can create your first admin user or login with an existing one.

### Test GraphQL calls

Our version of Strapi comes with GraphQL installed so, after you serve the application, you can access the GraphQL playground by visiting
http://localhost:1337/graphql

### Creating a new model or content type

Content types in Strapi are data models with integrated API endpoints and UI inside Strapi. You can create one from the admin very easily, however, everytime you create one, Strapi will be creating a group of documents for the API and route to work appropiatly.

This may cause 2 different issues that you need to bear in mind:

_1._ If you are running this application in Heroku, you need to make sure that you include the new changes in your Heroku repository, locally in your machine, and then you push them as part of your regular git process.
Don't attempt to create content-types directly from your application served in Heroku. Heroku will delete all files once it goes to sleep.

_2._ Creating new content-types will also make your repository differ from our master. We suggest using namespaces for your content-type so you increase your compatibility with our master to be able to pull next time again. 

Example  
Let's say that your project's name is YOLO. Instead of creating a content-type Library choose a name like YoloLibrary.

## Technology stack 💻

- **Backend** : Strapi and Koa are used to make a GraphQL and REST API for Canvasboard.

- **Database** : MongoDB Atlas free tier with up to 512MB free storage is deployed on AWS.

## Contribution 🤝

Start working on a feature by making a separate branch and make commits with meaningful messages. Feel free to open [new-issues](https://github.com/Canvasbird/canvasboard-backend/issues/new) if you encounter bugs or want to suggest some enhancement in the app.

Before contributing to this project do check [CONTRIBUTING.md](./CONTRIBUTING.md) file and [CODE_OF_CONDUCT.md](./CODE_OF_CONDUCT.md) file.

[![built with love](https://forthebadge.com/images/badges/built-with-love.svg)](https://github.com/sharmaaditya570191/) [![smile please](https://forthebadge.com/images/badges/makes-people-smile.svg)](https://github.com/sharmaaditya570191/)

