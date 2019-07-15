## Java based Firebase Cloud Messaging (FCM) Quickstart & Python client for FCM

The Firebase Cloud Messaging Android Quickstart app demonstrates registering an Android app for notifications and handling the receipt of a message. InstanceID allows easy registration while FirebaseMessagingService and FirebaseInstanceIDService enable token refreshes and message handling on the client.
This projects contains python scripts necessary to send diffrent types of messages to registered clients.


![Image of Application](https://github.com/Aramideh/FireBase-Cloud-Messaging/blob/master/appView.jpg)

### Getting Started

* [Add Firebase to your Android Project.](https://firebase.google.com/docs/android/setup)
* Run the sample on Android device or emulator.
* for in depth understanding of Python client you can visit [pyfcm project](https://pypi.org/project/pyfcm/) or for the working example you can skip this part and go to #Sending Notifications.

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

#### Sending Notifications

You can send messages to the clients with these ways:

* Use Firebase console to send FCM messages to device or emulator.
 go to the firebase console and start sending messages to the clients.

* Using Pyfcm
visit https://pypi.org/project/pyfcm/ to instal pyfcm. create a file and copy below code.

```
from pyfcm import FCMNotification
  push_service = FCMNotification(api_key="SERVER_KEY")
  registration_id = "REGISTERATION_TOKEN"
  message_title = "your title"
  message_body = "Hi, your message body goes here!"
  result = push_service.notify_single_device(registration_id=registration_id, 
  message_title=message_title, message_body=message_body)

print result
```

run the saved file from command prompt and if everything is OK, you will see the notification on the client screen.


* ****SERVER_KEY:****
You can get your SERVER_KEY from firebase console, go to the project setting in firebase console and from Cloud Messaging tab get your SERVER_KEY




* ****SREGISTERATION_TOKEN:****
This token will be created the first time the app installs on an android device, you can get this token from the log in android studio or clicking on the token button in the app will show it to you.




### Authors

* [**Sadeq Aramideh**](https://github.com/Aramideh)



### License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details



### Acknowledgments
* [Firebase Cloud Messaging Quickstart](https://github.com/firebase/quickstart-android/tree/master/messaging)
* [DimitarStoyanoff/Notifications](https://github.com/DimitarStoyanoff/Notifications)
* [PyFCM](https://pypi.org/project/pyfcm/)
