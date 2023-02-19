# To-Do-List
A To-Do List using a Postgres database to hold the information

## Build a simple full-stack to-do list app leveraging the structure of MVC!

## Part 1 - Setting up the Project

Within the root directory of project, install the dependencies in package.json.
Remember that you can install dependencies in package.json by running the below command:
`npm install`

Next, set up the application’s view directory by navigating there from your terminal and installing the dependencies.
Remember that you can install dependencies in package.json by running the below command:
`npm install`

Now that our project has all of the necessary node modules installed, let’s set up PostgreSQL locally on our computer. Be sure to write down your PostgreSQL username and password. We’ll need these later when we set up our environment file.

Once we’ve set up PostgreSQL on our local computer, use the code in the todo.sql file to create a database and a table called todo that our application will populate.

If you are using Postbird, navigate to the Query tab and copy-paste the following SQL code below:
`CREATE TABLE todo(
  todo_id SERIAL PRIMARY KEY,
  description VARCHAR(225) NOT NULL 
);`

You can also use the PostgreSQL terminal to create a database called todo by running the following command:
`CREATE DATABASE todo;`

Then, create the todo table within the database we just created by running:
`CREATE TABLE todo(
  todo_id SERIAL PRIMARY KEY,
  description VARCHAR(225) NOT NULL 
);`

With PostgreSQL set up, we can use the database.js file to connect our application to our database. Create a .env file to correlate with the process.env declarations provided within the database.js file.

You can use the below as boilerplate code, filling in the empty variables with our database username and password.
`DB_USER=
DB_PASSWORD=
DB_HOST=localhost
DB_POST=5432
DB_DATABASE=todo
PORT=8000`

## Part 2 - Deploying Locally

We are now ready to run our to-do list app! Start the project by running npm start inside the root directory as well as inside the view directory. Remember that you’ll need to start your back-end server first for the app to work correctly.

We are using nodemon to run the back-end server. nodemon is a Node package that watches our files and automatically restarts the server each time we save a change. Without it, we’d need to restart the server each time we made a change to see those changes take effect.

## Debugging Tips

Feeling stuck? Try the following:

Google your question: Often, someone has had the same question as you! Check out websites like StackOverflow and Dev.to to see how other folks have found solutions.
Read the documentation: Make sure to carefully read through the documentation for any languages and libraries you are using. Often they’ll have examples of what you’re looking for!
Rubber ducking: Try to explain a problem to a friend or co-worker. Often you’ll figure out the solution as you’re trying to explain it. And if not, getting another pair of eyes on your code can be helpful.
Discuss with other learners: Sometimes, it’s helpful to talk things out with someone at a similar point in their learning journey. Check out the Codecademy Forum for Off-Platform projects to connect with other learners who are working on the same project.

## Review

Congratulations! You’ve just implemented a to-do list app built using the MVC architecture. In this project, we reorganized files, altered existing files, created new ones to build out our MVC components and connect them.

As a challenge, try adding additional routes or experimenting with the available response methods. You can check out the Express documentation on routing to learn more.
