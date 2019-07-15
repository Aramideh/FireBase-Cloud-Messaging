# Java based Firebase Cloud Messaging (FCM) Quickstart & Python client for FCM

The Firebase Cloud Messaging Android Quickstart app demonstrates registering an Android app for notifications and handling the receipt of a message. InstanceID allows easy registration while FirebaseMessagingService and FirebaseInstanceIDService enable token refreshes and message handling on the client.
This projects contains python scripts necessary to send clients diffrent types of messages.

## Getting Started

* [Add Firebase to your Android Project.](https://firebase.google.com/docs/android/setup)
* Run the sample on Android device or emulator.
* for in depth understanding of Python client you can visit [pyfcm project](https://pypi.org/project/pyfcm/) or for the working example you can skip this part and go to #Sending Notifications.

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Sending Notifications
* Use Firebase console to send FCM messages to device or emulator.
* after installing pyfcm you can use below code to send message to the client


```
from pyfcm import FCMNotification

push_service = FCMNotification(api_key="SERVER_KEY")
registration_id = "REGISTERATION_TOKEN"
message_title = "your title"
message_body = "Hi, your message body goes here!"
result = push_service.notify_single_device(registration_id=registration_id, message_title=message_title, message_body=message_body)

print result
```


* SERVER_KEY:
you can get your SERVER_KEY from firebase consol, go to the project setting and from Cloud Messaging tab get copy your SERVER_KEY


* REGISTERATION_TOKEN:
this token will be created the first time app installs on the device, you can get this token from the Log in android studio or t
with clicking on the token button in the app



## Authors

* **Sadeq Aramideh** - *Initial work* - [Aramideh](https://github.com/Aramideh)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments
* [Firebase Cloud Messaging Quickstart](https://github.com/firebase/quickstart-android/tree/master/messaging)
* [DimitarStoyanoff/Notifications](https://github.com/DimitarStoyanoff/Notifications)
* [PyFCM](https://pypi.org/project/pyfcm/)
