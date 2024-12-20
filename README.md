# Setup Instructions:
## Prerequisite: Sufficient understanding of react, javascript, express,mongodb(web account), HTML, and CSS are the required prerequisites.

## How to set up the App: 
## Install node.js and npm:
Go to https://nodejs.org/en to install node.js and make sure to click npm manager in the installation screen to install both node.js and npm together.
Go to your command prompt and run npm -v or node -v to verify the installation
Or, You can do npm install to install npm after installing node.js.
Do npm start to start the app. The app will then get started on the local host.
Be sure to perform npm install and npm start on both server and client directories in the terminal( also, you only need to perform npm install once)
When you open up the folder, be sure to import cors, and bcrpyt in the server directory before running npm start. Do this by running npm install cors and npm install bcrpyt. (there's a small chance they might not be installed in there if you open it).
Go to this website for more information:https://radixweb.com/blog/installing-npm-and-nodejs-on-windows-and-mac 

## VScode installation:
Go to https://code.visualstudio.com/docs/setup/windows to install vscode
Complete the installer screen, then run the app
Verify npm and node works on it by running npm -v or node -v in the terminal

## MongoDB setup: 
Go to https://www.mongodb.com/ and click sign up
Click Create project and add a name to it. then click create project.
Then click Build Database and be sure to choose the free option for the cluster with aws and choose your nearest region location. Then click CREATE at the very bottom of the page.
Where it says “Security Quickstart”, Enter your username and password. Be sure to keep your username and password somewhere for you to remember, like in a notepad. Click Add User when you're done. If need be, include your ip at the very bottom, but for now it should be done for you already.
Click finish and close to end setup.
Then click Connect. This is to configure any mongodb installation to your software. Choose Drivers and then choose nodejs 6.7. Mongodb should be installed in the app already so just copy and paste the third option(it says “Add your connection string into your application code”.
Place the the code URL in the .env file in the application where it says MONGO_URL. Be sure to replace the <password> with your password from step 4.
This should configure the database for you.
If you need more help, watch this video from the “Set up mongodb and connect it” section of the video.https://youtu.be/XPC81RWOItI?t=2034 

## Zip file import:
Go to the github https://github.com/kiwimped/MedConnectNew 
Click on the code button and download the zip file
Delete node_modules in both server and client folders before extracting them(they contain too many files)
Place the file and extract it into a distinct folder 
Run the folder in VScode, and be sure to type npm install in both directories (you only need to do this once), then type npm start in the project folder’s directory in the terminal to run the project i.e( c:/projectFolder/client and /server  npm start)

## Extras:
Make sure that the directories(i.e. functions or constants) that are called in the code go to their intended folder and file.
Also, make sure that any of the dependencies of the react project from the images below are in their package.json file.
## Client:
"dependencies": {
    "@emotion/react": "11.13.3",
    "@emotion/styled": "11.13.0",
    "@mui/material": "6.1.6",
    "axios": "^1.7.7",
    "mdbreact": "5.2.0",
    "phosphor-react": "1.4.1",
    "react": "^18.0.0",
    "react-dom": "^18.0.0",
    "react-hot-toast": "^2.4.1",
    "react-native": "0.76.1",
    "react-native-safe-area-context": "4.14.0",
    "react-native-web": "0.19.13",
    "react-router-dom": "6.27.0",
    "react-scripts": "^5.0.0"
  },
  
## Server:
{
  "name": "server",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "start": "nodemon index.js"
  },
  "author": "",
  "license": "ISC",
  "dependencies": {
    "bcrypt": "^5.1.1",
    "cookie-parser": "^1.4.7",
    "cors": "^2.8.5",
    "dotenv": "^16.4.5",
    "express": "^4.21.1",
    "jsonwebtoken": "^9.0.2",
    "mongodb": "^6.10.0",
    "mongoose": "^8.8.2",
    "nodemon": "^3.1.7"
  }
}

## Config Instructions: Environmental variables must be configured and a .env file is usually needed.For the MONGO_URL, replace to old url with the one from your mongodb web database(check mongodb setup from early in the document). The routing also needs to be configured as in App.js, you need paths for pages such as /login, /register, and /account. These are managed by react-router-dom.
