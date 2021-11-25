# How to run this boilerplate

A tutorial on how to create cloudinary > accounts, install dependencies and run the project.

1. Install dependencies
Run yarn install or npm install on both client and server folders, this command will install the project's dependencies.

2. Create cloudinary account
Go to cloudinary images website and create an account.

Under the Account Details section is a url named API environment variable this is your cloudinary url.

3. Create a env file
Create a file named .env and, inside of it, place this:

HOST=[HOST]
PORT=[PORT]

DATABASE_URL=[DATABASE_URL]

CLOUDINARY_NAME=[CLOUDINARY_NAME]
CLOUDINARY_KEY=[CLOUDINARY_KEY]
CLOUDINARY_SECRET=[CLOUDINARY_SECRET]
Where:

[PORT] is which port you want the server to run on (usually 3001)
[COOKIE_SECRET] is a random string used for authentication on the admin.
[CLOUDINARY_URL] is the url you got from step 3.2
5. Running in development
To run this project in development mode, we will need to run two servers, the react one on /client and keystone on /server.

The command to run react is yarn start or npm start depending on which tool was used on installation, the react server will run on port 3000 by default.

Before running the keystone server, go to /server/updates/0.0.1-admin.js and change the admin user as you want, this user will be the first created, but you will be able to create others and delete this one later.

To run keystoneJS server, use the command node index.js, the server will run on whatever port is in the variale in the env file, you will find the admin interface in http://localhost:[PORT]/admin

6. Running in production
To run the server in production, go to /client and run the command yarn server, this command will create a react production optimized build and move it to /server.

Then go to /server and run node index.js, you will find the project on http://localhost:[PORT]

Developed by Jorrmungandr
This boilerplate was meant to be used in CITi's selective process on 2020.1, to help the development of onepage websites.
