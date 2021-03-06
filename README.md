# FERN-Base
A base template for working with the Google Firestore, Express, React, Node.js tech stack.  
***
## Quick Start
The section will guide you through setting up a Google Firebase project with a Firestore database 
and enable user authentication via Google Authentication, and configuring the project to utilize it.

1.  Login to the [Firebase Console](https://console.firebase.google.com), click '+ Add Project', and follow the prompts 
to set up a new Firebase project.
2.  Add a web app to the project by clicking on the '</>' icon on the project dashboard and give it a name. 
3.  Once you get to the 'Add Firebase SDK' step, copy the firebaseConfig json object into the 
[firebase-config.js](client/src/firebase-config.js) file in the React client.
4.  Click 'Go to console', then navigate to the Cloud Firestore page via the sidebar. Click 'Create Database', 
ensure that the 'Start in production mode' radio button is selected before continuing.  Follow the rest of the prompts 
to initialize the database. 
5.  Navigate to the Authentication page via the sidebar. Click 'Set up sign-in method' and enable the Google sign-in 
option.
6.  Follow the instructions under your Firebase project's Project Settings -> Service Accounts -> 
Generate new private key to generate a Firestore database secret and fill [firebase-secret.json](./firebase-secret.json) 
with its content
7. Change the firestoreUrl variable in [index.js](./routes/index.js) to match your project's database Url, found under 
Project Settings -> Service Accounts, in the Node.js code snippet.

Firebase has now been configured and is ready to use.
***
## Running the Project
There are two servers to run - the api server and the react frontend server.  Initialize both by running 

    npm install
    
from the project root directory and from the client directory.  To run the project, 
start up the api server followed by the frontend server by running

    npm start
    
in the project root directory followed by the client directory.  The website is available at 
```localhost:3000``` and the api server handles requests on ```localhost:5000```.