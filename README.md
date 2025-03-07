# To-Do-List

This project allows users to keep track of to-do-items! I developed this project to include 
a PostgreSQL database so that even if the user closes the browser or application, their items still remain. 

## Technologies Used

- Node.js: JavaScript runtime environment used for building the server.
- Express: Web framework for Node.js that simplifies server creation and routing.
- EJS: Embedded JavaScript templating for rendering views.
- Body-Parser: Middleware to parse incoming request bodies in various formats (JSON, URL-encoded).
- dotenv: Loads environment variables from a .env file.
- pg: PostgreSQL client for Node.js.
- PostgreSQL: Used to store user data and information about visited countries. 

## Installation Steps

To install this project, you will want to follow these instructions in order:
1. Ensure you have Node.js installed on your local machine. 
    1. If you don't have Node.js installed, you can download it from [here](https://nodejs.org/en/download).Once Node.js is running, open a new terminal and move to the next step.
2. Clone the repository by entering 'git clone https://github.com/ericdurban/To-Do-List.git' in the terminal.
3. Enter in terminal, 'cd To-Do-List'. 
4. Enter in terminal, 'npm install' to ensure all the needed dependencies are added and installed locally. 
PLEASE NOTE: If you have any issues in later steps running the project, try individually installing dependencies listed on top of index.js file. For example, enter in terminal, 'npm i express' to install express dependency package.
5. Install PostgreSQL on your local machine, set up PostgreSQL database and create a table for the tasks.
    1. If you don't have PostgreSQL installed, you can download it from [here](https://www.postgresql.org/download/).
    2. Create a database for the project by entering the following:
        CREATE DATABASE to_do_list;
    3. Either select the database from PostgreSQL Admin or connect to your database in the terminal by entering the following:
        \c to_do_list;
    1. Please use the following schema to create the necessary table:
        CREATE TABLE tasks (
            id SERIAL PRIMARY KEY,
            task VARCHAR(255) NOT NULL,
            completed BOOLEAN NOT NULL DEFAULT FALSE
        );
    2. Please create an .env file in the root directory and add the database connection detals:
        DB_HOST=localhost
        DB_USER=your-db-username
        DB_PASSWORD=your-db-password
        DB_NAME=to_do_list
        DB_PORT=5432
6. Enter in terminal, 'npm start'. Your terminal should register the command and provide a message "Server running on port: 3000". 

## Usage

Steps to utilize the application:
1. Once you've received the message from your terminal that the server is running, open your browser and navigate to http://localhost:3000. 
2. Now that you are on the application, you can add, delete, or edit your to-do-items! 
    1. Adding a to-do item: Type in the new item at the bottom of the to-do-list and then click the plus button.
    2. Deleting a to-do item: Click the checkbox next to the selected item you'd like to delete. 
    3. Editing a to-do item: Click on the pencil icon next to the item you'd like to select. The text will then become editable. 

## Contributing 

If you'd like to contribute, please follow these steps:
1. Fork the repository.
2. Create a new branch (git checkout -b feature/your-feature).
3. Make your changes.
4. Commit your changes (git commit -am 'Add new feature').
5. Push to the branch (git push origin feature/your-feature).
6. Create a new pull request.

## License
This project does not currently have a license. All rights reserved. 
This project is free to use for personal, non-commercial purposes only. You may not distribute or modify the project without the author's permission.

## Acknowledgements

- Thanks to Angela Yu and her amazing bootcamp that helped me develop the tools I needed to make this website!
