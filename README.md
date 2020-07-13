# Sending Notification Using Firebase Function And Firebase Cloud Messaging.

## About This Project ( Must Read )

This project is based on "Healing Factor" app, all the commands are customized according to requirement. "index.js" can be found in the function folder. 

This “index.js” file handles the Firebase Cloud Messaging and Firebase Realtime Database. When a new value for the notification is pushed in the database this file acts like a trigger to send a notification by creating a payload and sending it to the desired user using Firebase Cloud Messaging Service. I have also created a trigger to delete user details from the database when the user deletes his/her account from the authentication services. This will this remove unwanted data from database.

## How to Setup?

Step 1: Download and install NodeJS.

Step 2: Now open cmd-prompt and download Firebase Functions,Firebase Admin, and Firebase Tools.  

````
npm install firebase-functions@latest firebase-admin@latest --save
npm install -g firebase-tools
````

Step 3: Login to your account and select the application you want to deploy the function to.

````
firebase login
````

Step 4: Go to your Firebase project directory in cmd-prompt and now type:

````
firebase init
````

Step 5: Select  function and the project name. It will automatically download the dependancies. Select 'Javascript' as the language support.

Now the file structure will be like this.
````
myproject
 +- .firebaserc    # Hidden file that helps you quickly switch between
 |                 # projects with `firebase use`
 |
 +- firebase.json  # Describes properties for your project
 |
 +- functions/     # Directory containing all your functions code
      |
      +- .eslintrc.json  # Optional file containing rules for JavaScript linting.
      |
      +- package.json  # npm package file describing your Cloud Functions code
      |
      +- index.js      # main source file for your Cloud Functions code
      |
      +- node_modules/ # directory where your dependencies (declared in
                       # package.json) are installed

````

## Downloading "index.js" File

You can download and use index.js in your Firebase Functions Folder.

Folder structure

```
- Notification (any blank folder of your choice)
  |- functions
    |- index.js (replace this file with the file above).
```


## Firebase Database Structure

### Users Table :

```
- Users
  - user_push_id
    - device_token : user_device_token
    - name : user_name
```

### Notification Table :

```
- notifications
  - to_user_id
    - notification_id
      - from : from_user_id
```

# Important :

Currently this method works with user who is logged in a single device.


## Support
If you think my projects are helpful you can contribute me anything at paypal.me/sourabh48


