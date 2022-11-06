

![1](https://user-images.githubusercontent.com/101529105/200438876-8b0ca58b-48a0-4e7c-9539-8276b58ded60.png)

## MVC Architecture in JavaScript Web Applications

![2](https://user-images.githubusercontent.com/101529105/200438878-7700a83c-67c0-420d-a156-dae0a6be9580.png)

## What is MVC?

An architectural design paradigm introduced in 1979 that separates the development of a web application into three main components:

- Models
- Views
- Controllers

![3](https://user-images.githubusercontent.com/101529105/200438880-a914de3e-0dc9-4cd3-bdf5-1b63f6ee81da.png)

## Client Side
**The Front End**

When the user interacts with the application in the browser, they send a request to the server

A request may be made by clicking on something within the app or by typing a URL in the address bar of the browser

What the user sees after making the request depends on what happens on the server

## Server Side
**The Back End**

When the server receives a request from the client, it will direct that request to the router that handles that action

A complex application may have many routers

Responds to the client's request

![4](https://user-images.githubusercontent.com/101529105/200438881-916e8565-440d-4ebe-899d-84a250231594.png)

![5](https://user-images.githubusercontent.com/101529105/200438883-f1dfeaba-abc0-4dcf-919b-235f7754b83c.png)

## Architecting Your Application
**Setting Up Folder Structure**

Setting up your folder structure in an organized, intuitive way makes it easier for others on your team to understand your code base and maintain your application

![6](https://user-images.githubusercontent.com/101529105/200438885-884f5d9d-055f-4ed4-b708-305469137fa6.png)

## Routers
**Directing Traffic**

Depending upon the complexity of the application, routers may be in the app.js or server.js file, or may have their own folder with separate files for different paths/actions

Different paths for different aspects of the application such as logging in, logging out, getting data, processing forms, etc.

![7](https://user-images.githubusercontent.com/101529105/200438886-60e0976d-27ac-461a-825d-c82036f64e2d.png)

## Controllers
**The Middleman**

#### Listen for requests from the client

- There may be multiple controllers on each route (or path)

#### Control & perform the application logic

- Communicate with Views & Models

- Handle functions for form actions

#### Controllers in JavaScript Applications

- Use JavaScript to dictate how the application behaves & sends data between the Views & Models

![8](https://user-images.githubusercontent.com/101529105/200438889-a50dd8c3-a2e8-49b9-a556-ca9df8232397.png)

## Example:
**Rendering a user login page**

#### Main Router

- In this Node.js application, when the user requests to be taken to the login page (example.com/login) the router directs this request to the authController

#### Auth Controller

- The controller checks whether or not the user is logged in. If they are not, the /login page is rendered. If they are, the user is redirected to the home page

![9](https://user-images.githubusercontent.com/101529105/200438891-af8a0a56-002e-4149-ad99-cfc0070ec35f.png)

## Views
**What's Visible to the User**

#### Are rendered in the web browser

- What the user sees & interacts with

- Can only receive responses from the Controller

#### Views in JavaScript Applications

- Can be generated using templating languages such as Handlebars, EJS, Pug, etc.

![10](https://user-images.githubusercontent.com/101529105/200438893-e3bac5c5-ade3-4727-bab1-3cb4c064961b.png)

## Example:
**Rendering a user login page**

#### Login View

- The authController has determined that the user is not already logged in, so it communicates with the Views folder to render the login view

- In this application, that page is rendered with EJS (Embedded JavaScript)

![11](https://user-images.githubusercontent.com/101529105/200438896-b42678e5-aa8e-42b4-ba4f-2bfd6bccb4fa.png)

## Models
**The Data**

Store data & data logic

Handle communication to the Database

#### Models in JavaScript Applications

- Some popular databases include MongoDB, MySQL, Oracle, etc.

- Can use libraries like Mongoose

![12](https://user-images.githubusercontent.com/101529105/200438897-7084e2d9-0090-4b4e-92a8-9a1023815369.png)

## MongoDB

- A noSQL database program

- Data records called Documents are stored in Collections

- A database has one or more collections

![13](https://user-images.githubusercontent.com/101529105/200438899-4567ce88-d282-48e4-8595-b2f95be71c1c.png)

## Mongoose

- Mongoose.js is an Object Data Modeling (ODM) library for Node.js & MongoDB

- Represents the data as a JSON object

- Provides a schema-based solution to model your application data

- Manages relationships between data, provides schema validation, and is used to translate between objects in code & the representation of those objects in MongoDB

![14](https://user-images.githubusercontent.com/101529105/200438900-4eb6fdd4-9c0b-4f6d-b6d0-32d1f8f93458.png)

## Example:
**Storing user data**

#### User Model

When a user logs into the application, their data is accessed from the database by the User Model. In this case the only user data we store is a username, email, & password

Note: never store a user's password as a plain string. Use password-hashing middleware like bcrypt to protect the user's password

![15](https://user-images.githubusercontent.com/101529105/200438901-9d731d1e-b691-47c2-b924-3096198ff36a.png)

## Summary
**Why build applications using MVC?

- A common design pattern you will likely encounter as it has been around for over 40 years

- Separates the front- and back-end into separate components

- Makes code easier to edit & update

- Simplifies the testing process

![16](https://user-images.githubusercontent.com/101529105/200438902-e43652f0-d8d1-4d7f-87eb-20d2658e2c2f.png)

## Sources

- MDN Web Docs — [developer.mozilla.org](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/mongoose)
- freeCodeCamp — [freecodecamp.org](https://www.freecodecamp.org/news/introduction-to-mongoose-for-mongodb-d2a7aa593c57/)
- MongooseJS — [mongoosejs.com](https://mongoosejs.com)
- MongoDB — [mongodb.com](https://www.mongodb.com)
- 100Devs — [twitch.tv/learnwithleon](https://www.twitch.tv/learnwithleon)
- Mayanwolfe — [twitch.tv/mayanwolfe](https://www.twitch.tv/mayanwolfe)