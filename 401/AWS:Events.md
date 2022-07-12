## AWS SQS vs SNS

1.	What is the difference betweeen SQS and SNS?

 SNS is an abbreviation of Simple Notification Service, it’s a distributed publish-subscribe system which pushes a message to multiple(all) subscribers as soon as it receives it from a publisher. It’s a fully managed service that can send messages to many types of subscribers like phones, email recipients and HTTP endpoints. By default, each subscriber receives every message published to the topic. 

 Simple Queue Service (SQS), as the name suggests, is a distributed, fully managed message queuing service. Subscribers have to PULL  messages from SQS and messages can’t be received by multiple receivers at the same time. At a time, one receiver can receive a message, process and delete it; other receivers will not get to see that message. Using SQS you can easily decouple applications or integrate applications. 

### Key Differences

-	Entity Type

SQS : Queue (similar to JMS, MSMQ).

SNS : Topic-Subscriber (Pub/Sub system).

-	Message consumption

SQS : Pull Mechanism — Consumers poll messages from SQS.

SNS : Push Mechanism — SNS pushes messages to consumers.

-	Persistence

SQS : Messages are persisted for some duration is no consumer available. The retention period value is from 1 minute to 14 days. The default is 4 days.

SNS : No persistence. Whichever consumer is present at the time of message arrival, get the message and the message is deleted. If no consumers available then the message is lost.
In SQS the message delivery is guaranteed but in SNS it is not.

-	Consumer Type

SQS : All the consumers are supposed to be identical and hence process the messages in exact same way.

SNS : All the consumers are (supposed to be) processing the messages in different ways.


2.	What are some use cases for both SNS and SQS?

### Use Cases

-	Choose SNS if:

•	You would like to be able to publish and consume batches of messages.

•	You would like to allow same message to be processed in multiple ways.

•	Multiple subscribers are needed.


-	Choose SQS if:

•	You need a simple queue with no particular additional requirements.

•	Decoupling two applications and allowing parallel asynchronous processing.

•	Only one subscriber is needed.

## AWS SNS and SQS

1.	Describe how to use SQS and SNS in a “fanout” pattern.

One common design pattern is called “fanout.” In this pattern, a message published to an SNS topic is distributed to a number of SQS queues in parallel. By using this pattern, you can build applications that take advantage parallel, asynchronous processing. For example, you could publish a message to a topic every time a new image is uploaded. Independent processes, each reading from a separate SQS queue, could generate thumbnails, perform image recognition, and store metadata about the image.

2.	Explain how “push notifications” work, using SNS.

You send push notification messages to both mobile devices and desktops using one of the following supported push notification services:

•	Amazon Device Messaging (ADM)

•	Apple Push Notification Service (APNs) for both iOS and Mac OS X

•	Baidu Cloud Push (Baidu)

•	Firebase Cloud Messaging (FCM)

•	Microsoft Push Notification Service for Windows Phone (MPNS)

•	Windows Push Notification Services (WNS)

Push notification services, such as APNs and FCM, maintain a connection with each app and associated mobile device registered to use their service. When an app and mobile device register, the push notification service returns a device token. Amazon SNS uses the device token to create a mobile endpoint, to which it can send direct push notification messages. In order for Amazon SNS to communicate with the different push notification services, you submit your push notification service credentials to Amazon SNS to be used on your behalf. For more information.

In addition to sending direct push notification messages, you can also use Amazon SNS to send messages to mobile endpoints subscribed to a topic. The concept is the same as subscribing other endpoint types, such as Amazon SQS, HTTP/S, email, and SMS, to a topic. The difference is that Amazon SNS communicates using the push notification services in order for the subscribed mobile endpoints to receive push notification messages sent to the topic.

## SQS and SNS Basics

1.	How might a large scale, distributed application make use of a Queue system like SQS?

Amazon Simple Queue Service (SQS) is a fully managed message queuing service that enables you to decouple and scale microservices, distributed systems, and serverless applications. SQS eliminates the complexity and overhead associated with managing and operating message-oriented middleware, and empowers developers to focus on differentiating work. Using SQS, you can send, store, and receive messages between software components at any volume, without losing messages or requiring other services to be available. Get started with SQS in minutes using the AWS Management Console, Command Line Interface or SDK of your choice, and three simple commands.

SQS offers two types of message queues. Standard queues offer maximum throughput, best-effort ordering, and at-least-once delivery. SQS FIFO queues are designed to guarantee that messages are processed exactly once, in the exact order that they are sent.
