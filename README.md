##Simple backend project to use the mongoose to store the user data.

##text

├── models/
│   └── user.js              # Mongoose user schema & model
├── public/
│   └── stylesheets/         # Custom CSS files
├── views/
│   ├── index.ejs            # Create user form / home page
│   ├── read.ejs             # Page displaying all user cards
│   └── edit.ejs             # Page to update user details
├── app.js                   # Main application server & routes
├── package.json             # Project dependencies
└── package-lock.json        # Locked dependency versions

## Tech Stack & Dependencies
- **Runtime Envieonment:** Node.js
- **Framework:** Express.js
- **Database:** MongoDB with Mongoose ODM
- **Template Engine:** EJS (Embedded javaScript)

##Database Schema
*(models/user.js)*
THe user document in mongoDB contains the following fields:

Field            Type              Description

name            String             Full name of the user
email           String             User's email address
image           String             URL pointing to the user's profile image


##Applicatino Routes

HTTP Method     Route path           View Rendered                Description

GET             /                    Views/index.ejs              Reders the home page with the form to cerate a user
POST            /cerate              N/A                          Receives form data and creates a new user 
GET             /read                Views/read.ejs               Display all registered user in cards
GET             /edit/:userid        Views/edit.ejs               Renders the edit form populated with user details
POST            /update/:userid      N/A                          Update the user's details
GET/DELETE      /delete/:userid      N/A                          Deletes the specified user 

## How to run the project

1- Clone or download the project folder.
2- install dependencies:
  - npm install
3- Start the server:
  - node app.js
(or useing *npx nodemon app.js* for automatic server restarts)
4- open in browser:
  - Navigate to *http://localhost:3000*
