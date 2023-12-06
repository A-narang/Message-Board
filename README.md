# Message Board Application

This message board allowed users to post and view messages. The application is built using a combination of Node.js, Express.js, SQLite, HTML, CSS, and JavaScript.

## Overview

### Files
   - Public
      - Script.js
      - Index.html
      - Styles.css
   - App.js
   - Messages.db

### Data Flow
   1. Posting a Message 
      - User inputs a message in the front end,
      - When "Post" is pressed the postMessage funcntion in scripts.js is called,
      - If the message is empty ot greater than 128 characters an error is given.
      - if the message is valid a message object is created and the message is added to the SQLite Database.

   2. Viewing a Message
      - When the page is refreshed the loadMessages function is called from scripts.js,
      - A GET request is sent to the server's API and all messages are retrived from the database,
      - the message is displayed with a timestamp.
   

## Components

### Backend Components

1. **Node.js and Express.js:**
   - Handle server-side logic and routing.
   - Receive and process incoming requests from the frontend.

2. **SQLite Database:**
   - Store and manage messages.
   - Data retrieval and storage.

### Frontend Components

   1. Index.html:
      - The HTML file containing the structure of the message board.
   2. style.css
      - Basic styling for the message board interface, making it user-friendly.
   3. app.js: 
      - The frontend JavaScript file that loads messages and handles displaying new messages.

### Backend Components
   1. server.js
      - The backend file that sets up an Express server. It retrives messages from and adds messages to the SQLite database. 
   2. messages.db
      - The SQLite database file storing the messages. A message contains the conent of the message and the timestamp of when it was posted. 

## Requirements
   - Displays an error message when message is empty or greater than 128 characters
   - Messages diplay date and time of post and are ordered from most to least recent
   - Users on different computers can view the messages when the page is refreshed


## How to Start the Application

### Cloud Version: https://c4cmb.azurewebsites.net/

### To Start Locally:
  1. git clone https://github.com/A-Narang/Message-Board.git
  2. cd c4c in the terminal
  3. Start the server with by entering npm start in the terminal
  4. go to http://localhost:8080/
