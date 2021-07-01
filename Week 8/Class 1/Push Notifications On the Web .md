# Push Notifications On the Web

Class: Server
Class Date: June 28, 2021 10:06 AM
Type: Theory
Video Link: https://drive.google.com/file/d/1qRchPuSqJKBoRPXYboABRehL6Tg7qUFQ/view
Link 2: https://drive.google.com/file/d/1t4IVhP7UGl0ksT2L8_mlE1vngJ17EpoG/view

**Notion File Link:** shorturl.at/pxHJ7



------

Need **2 APIs** to make Push Notification Work

- **Notification API :**  To show any notification on the display.
- **Push API :**  Allows A Service Worker to handle push messages from a server, even when server is not running. Here Server is Facebook and **Client is User's Browser.**

### *Important Terms*:

- **Notification** : A message displayed as pop up to user. Not all pop ups are notifications.
- **Push Message** : A Message sent from Server to Client. Not all Push Messages are Push Notification
- **Push Notification** : If we want to show Push Message as a Notification to the User with the help of a Notification API, then it is Push Notification.
- **Web Push** : The whole process that is involved in sending a message from server to client. All the components needed here are part of Web Push.
- **Push Service** : A system of routing Push Message from Server to Client. Each browser implements it in its own way. Push Service is actually a Server. So each browser has its own Push Service. Server sends message to Push Service of Browser and then the Push Service routes the message to the individual client.
- **Web Push Protocol** : Describes how application or server interacts with Push Service.

   

### *Push Notification can be used for* :

- Alert user to an important event.
- Display an icon and small piece of text that the user can click to open up your site.
- Integrate buttons, sounds, vibrations.

### *Restrictions of Push Notifications :*

- Although Push Noti for Native Apps are quite common and easy to implement, Push Notifications for Browser is actually a new concept and the APIs aren't easily available
- For Push Notifications on the Web, we don't know which browser will use our app or in which condition.

### *Workflow of Push Notification :*

The Server needs to know how to uniquely identify each client so we can send specific      notifications to intended client.

**Functions of Service Worker:**

- Displays Notifications
- Handles Interactions
- Listens in the Background

![Push%20Notifications%20On%20the%20Web%200e2682108b864cde92f88075ca999cb7/Screenshot_8.png](Push%20Notifications%20On%20the%20Web%200e2682108b864cde92f88075ca999cb7/Screenshot_8.png)

Work Flow

# Notifications API(Client Side Work)

   This has two parts

1. Invocation API : Controls how to make notification appear. (Client Side Code)
2. Interaction API : Controls what happens when users interacts with it.

- ***How to Display Notification?***
    1. First we need to Check Permission. We also need to Request Permission.
    2. To display Notification we need to Write a Function. This function will first check if we have permission. If Permission is Granted, we show Notification using Service Worker.

        Primary Key : Gives each notification an unique id. We can give notification to user based on how he interacts with it using Primary Key. Primary Key tracks User Behaviour

    3. Then we send Notification to Service Worker. Service worker then displays Notification.

    4. After it displays notification, Service Worker waits for events(Notification Close,Swipe) so it can handle it.

    In this way Notification API, displays notifications and then goes to sleep.

    ![Push%20Notifications%20On%20the%20Web%200e2682108b864cde92f88075ca999cb7/Screenshot_9.png](Push%20Notifications%20On%20the%20Web%200e2682108b864cde92f88075ca999cb7/Screenshot_9.png)

# Push API (Server Side)

> **What actually happens when we give Permission to a Website to show Notification?**

We are actually giving granting permission to the website to use the Push Service of our Browser. Then our web app actually Subscribes to the browser's push service. Push Service then sends an Object to the Server. This Object has 2 things .

1. End Point URL (Contains URL of where we will Send Message and and an Unique Identifier that enables us to identify our user).
2. Public Key :  Public Key of our Application.

![Push%20Notifications%20On%20the%20Web%200e2682108b864cde92f88075ca999cb7/Screenshot_10.png](Push%20Notifications%20On%20the%20Web%200e2682108b864cde92f88075ca999cb7/Screenshot_10.png)

​                                                                             

Push Notification only works through HTTPS

## Summary

![Push%20Notifications%20On%20the%20Web%200e2682108b864cde92f88075ca999cb7/Screenshot_11.png](Push%20Notifications%20On%20the%20Web%200e2682108b864cde92f88075ca999cb7/Screenshot_11.png)
