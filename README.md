Sending Notification Using Firebase Function And Firebase Cloud Messaging.

# About This Project ( Must Read )

This project is based on "Healing Factor" app, all the commands are customized according to requirement. "index.js" can be found in the function folder. 

# Downloading "index.js" File

You can download and use index.js in your Firebase Functions Folder.

## Firebase Database Structure

### Users Table :
'''
- Users
  - user_push_id
    - device_token : user_device_token
    - name : user_name
'''

### Notification Table :
'''
- notifications
  - to_user_id
    - notification_id
      - from : from_user_id
'''

# Important :

Currently this method works with user who is logged in a single device.
