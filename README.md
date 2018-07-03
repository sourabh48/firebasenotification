# Sending Notification Using Firebase Function And Firebase Cloud Messaging.

## About This Project ( Must Read )

This project is based on "Healing Factor" app, all the commands are customized according to requirement. "index.js" can be found in the function folder. 

This “index.js” file handles the Firebase Cloud Messaging and Firebase Realtime Database. When a new value for the notification is pushed in the database this file acts like a trigger to send a notification by creating a payload and sending it to the desired user using Firebase Cloud Messaging Service. I have also created a trigger to delete user details from the database when the user deletes his/her account from the authentication services. This will this remove unwanted data from database.

## Downloading "index.js" File

You can download and use index.js in your Firebase Functions Folder.

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
