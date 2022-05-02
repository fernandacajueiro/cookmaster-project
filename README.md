# Welcome to the Cookmaster project repository! 👩🏻‍🍳

## Project description

This is the back-end application of a recipes registration and search system. Using `JWT`, `multer`, `model-service-controller` and `REST` architecture. In this project it is possible to register and login users and only these people will be able to access, modify and delete the recipes they have registered.

In order to make any type of change in the database (such as registration, editing or deletion of recipes) you will need to authenticate yourself. It is possible to register users of the `client` and `admin` type. A `client` user will only be able to trigger actions on the recipes that he himself has created. An `admin` person can trigger any action on any recipe.

Through this application, it is possible to perform the basic operations that can be done in a given database (create, read, update and delete - **CRUD**).

---

## Skills

While developing this project, I was able to:
- Understand what is inside an authentication token;
- Generate tokens from information such as login and password;
- Authenticate Express routes, using `JWT` token;
- Upload files in REST APIs;
- Save files on the server through a REST API;
- Query server files through a REST API;
- Perform integration tests;

---

## Install and run

1. Open the terminal and create a directory in your preferred location:
  ```
  mkdir fernandacajueiro-projects
  ```
2. Enter the directory you just created and then clone the project:
  ```
  cd fernandacajueiro-projects
  git clone git@github.com:fernandacajueiro/cookmaster-project.git
  ```
3. Go to the directory and install the necessary dependencies:
  ```
  cd cookmaster-project
  npm install
  ```
---

## How to use

- To register a new user, use the route `/users` and the method `POST`. The request body should follow the format:
  ```json
  {
    "name": "string",
    "email": "string",
    "password": "string"
  }
  ```
- To register a new recipe, use the route `/recipes` and the method `POST`. The request body should follow the format:
  ```json
  {
    "name": "string",
    "ingredients": "string",
    "preparation": "string"
  }
  ```
- To list all the recipes, use the route `/recipes` and the method `GET`.
- To list an specific recipe, use the route `/recipes/:id` and the method `GET`.
- To edit a recipe, use the route `/recipes/:id` and the method `PUT`. The request body should follow the format:
  ```json
  {
    "name": "string",
    "ingredients": "string",
    "preparation": "string"
  }
  ```
- To delete a recipe, use the route `/recipes/:id` and the method `DELETE`.
- To add an image to a recipe, use the route `/recipes/:id/image` and the method `PUT`.
- To access a recipe image, use the route `/images/<recipe-id>.jpeg` and the method `GET`.

**TIP**: use [Insomnia](https://insomnia.rest/) app to interact easily with the HTTPS-based APIs.

---

## Comments

This project was developed during the course at Trybe in 2021.
