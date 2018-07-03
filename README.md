# Sending Notification Using Firebase Function And Firebase Cloud Messaging.

## About This Project ( Must Read )

This project is based on "Healing Factor" app, all the commands are customized according to requirement. "index.js" can be found in the function folder. 

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

# Abouts:

 This “index.js” file handles the firebase messaging services and firebase database. When a new value for the notification is pushed in the database this file acts like a trigger to send a notification by creating a payload to the desired user using firebase messaging service. I have also created a trigger to delete user details from the database when the user unregisters his/her account. This will this remove unwanted data from database.

# Important :

Currently this method works with user who is logged in a single device.
