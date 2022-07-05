
# AWS S3, AWS Lambda Basics and CDN

# AWS S3
## What is Amazon S3?
Amazon Simple Storage Service (Amazon S3) is an object storage service that offers industry-leading scalability, data availability, security, and performance. Customers of all sizes and industries can use Amazon S3 to store and protect any amount of data for a range of use cases, such as data lakes, websites, mobile applications, backup and restore, archive, enterprise applications, IoT devices, and big data analytics. Amazon S3 provides management features so that you can optimize, organize, and configure access to your data to meet your specific business, organizational, and compliance requirements.

## Name some use cases for Amazon S3.
Amazon S3 Use Cases

Amazon S3 has many use cases, including:

- Storage for Internet
Amazon S3 is ideal when you want to store application images and videos, and render with faster performance. All AWS services (including Amazon Prime and Amazon.com), as well as Netflix and Airbnb, use Amazon S3 for this purpose. Combining Amazon S3 with Amazon CloudFront enables much faster delivery due to CloudFront’s edge locations.

- Backup and Disaster Recovery

Amazon S3 is suitable for storing and archiving highly critical data or backup because it is automatically replicated cross-region, providing maximum availability and durability. For even more protection, you can use Amazon S3 versioning, which stores multiple versions of each file so it’s easy to recover the files or older copies. With Amazon S3, it’s rare to lose data if you keep your recovery point objective (RPO) and recovery time objective (RTO) as low as possible.

- Analytics

Amazon S3 provides a sophisticated in-place querying functionality to run powerful analytics on data which is in rest on S3. It eliminates the need to move and store data, as it supports a majority of third-party service integrations.

- Data Archiving

You can store and move TBs of data from Amazon S3 to Amazon Glacier’s very cheap and durable archiving solution for compliance purposes. You can also automate when data should be archived with a lifecycle policy that helps reduce efforts to manage data.

- Static Website Hosting

Amazon S3 stores various static objects. One interesting use case is its ability to host static websites. More and more web apps are becoming single page and static (Angular, ReactJS, etc.), and it’s costly to keep running a web server for their hosting. S3 offers a static website hosting feature that will enable you to use your own domain without incurring huge web server hosting costs.

- Security and Compliance

Amazon S3 provides multiple encryption and compliance standard features for PCI-DSS, HIPAA/HITECH, FedRAMP, the Data Protection Directive, FISMA, and more. These features help customers satisfy compliance requirements for virtually every regulatory agency around the world. They also make it easy to limit access access to critical data with the help of bucket policies.


## Name some benefits of using Amazon S3.
Amazon S3 is a pioneer in cloud data storage and has uncountable benefits, but let’s have a look at the 5 most prominent ones :

•	Reliable Security:

•	All-time Availability:

•	Very Low cost:

•	Ease of Migration:

•	The Simplicity of Management:


# AWS Lambda Basics

## What is AWS Lambda?

AWS Lambda is a serverless computing service provided by Amazon Web Services (AWS). Users of AWS Lambda create functions, self-contained applications written in one of the supported languages and runtimes, and upload them to AWS Lambda, which executes those functions in an efficient and flexible manner.

The Lambda functions can perform any kind of computing task, from serving web pages and processing streams of data to calling APIs and integrating with other AWS services.

The concept of “serverless” computing refers to not needing to maintain your own servers to run these functions. AWS Lambda is a fully managed service that takes care of all the infrastructure for you. And so “serverless” doesn’t mean that there are no servers involved: it just means that the servers, the operating systems, the network layer and the rest of the infrastructure have already been taken care of, so that you can focus on writing application code.

## Name some use cases for AWS Lambdas.

Due to Lambda’s architecture, it can deliver great benefits over traditional cloud computing setups for applications where:

1.	individual tasks run for a short time;

2.	each task is generally self-contained;

3.	there is a large difference between the lowest and highest levels in the workload of the application.

Some of the most common use cases for AWS Lambda that fit these criteria are:

Scalable APIs. When building APIs using AWS Lambda, one execution of a Lambda function can serve a single HTTP request. Different parts of the API can be routed to different Lambda functions via Amazon API Gateway. AWS Lambda automatically scales individual functions according to the demand for them, so different parts of your API can scale differently according to current usage levels. This allows for cost-effective and flexible API setups.

Data processing. Lambda functions are optimized for event-based data processing. It is easy to integrate AWS Lambda with datasources like Amazon DynamoDB and trigger a Lambda function for specific kinds of data events. For example, you could employ Lambda to do some work every time an item in DynamoDB is created or updated, thus making it a good fit for things like notifications, counters and analytics.

## Describe “serverless” to a non-technical friend.

The baking explanation of serverless

“A good analogy is selling cakes,” says Rami Sass, CEO at WhiteSource. “You can buy the ingredients, bake it, and sell it yourself, or you can give your recipe to a contractor and have them bake the cake every time someone orders one from you and get the same result. This is a more scalable process and although outsourcing is usually slightly more expensive than doing it yourself, you only pay for the cakes that were ordered and are free to invest your time and resources elsewhere.”


# CDN

## What is a CDN?

A Content Delivery Network (CDN) is a geographically distributed group of servers that work together to provide fast delivery of Internet content. A CDN allows for the fast transfer of data needed for loading Internet content including HTML pages, javascript files, stylesheets, images, and videos.

CDNs work through servers nearest to the website visitor respond to the request. The content delivery network copies the pages of a website to a network of servers that are spread out at geographically different locations, caching the contents of the page. When a user requests a webpage that is part of a content delivery network, the CDN will redirect the request from the originating site’s server to a server in the CDN that is closest to the user and deliver the cached content. CDNs will also communicate with the originating server to deliver any content that has not been previously cached. In turn, the speed is improved by distributing content closer to the website visitors by using a nearby CDN server, causing visitors to experience faster page loading times. In simpler terms, for example, instead of a user in London trying to access a server in LA, which can cause slower Internet speeds, the user would be redirected through a CDN that is geographically closest to them (London, Paris, Stockholm, etc). As of today, the majority of web traffic goes through through CDNs, including traffic from major sites like Facebook, Netflix, and Amazon.

Employing a CDN doesn’t only speed up the delivery of Internet content, it helps protect your website against certain forms of cyber attacks, such as Denial of Service attacks. It protects against these threats because CDNs allow for the handling of more traffic and withstanding hardware failure better than many origin servers. 


## How does a CDN work with relation to the website visitor?

At its core, a CDN is a network of servers linked together with the goal of delivering content as quickly, cheaply, reliably, and securely as possible. In order to improve speed and connectivity, a CDN will place servers at the exchange points between different networks.

These Internet exchange points (IXPs) are the primary locations where different Internet providers connect in order to provide each other access to traffic originating on their different networks. By having a connection to these high speed and highly interconnected locations, a CDN provider is able to reduce costs and transit times in high speed data delivery.
 
Beyond placement of servers in IXPs, a CDN makes a number of optimizations on standard client/server data transfers. CDNs place Data Centers at strategic locations across the globe, enhance security, and are designed to survive various types of failures and Internet congestion.


## What are the benefits of employing a CDN?

1.	Improving website load times - By distributing content closer to website visitors by using a nearby CDN server (among other optimizations), visitors experience faster page loading times. As visitors are more inclined to click away from a slow-loading site, a CDN can reduce bounce rates and increase the amount of time that people spend on the site. In other words, a faster a website means more visitors will stay and stick around longer.

2.	Reducing bandwidth costs - Bandwidth consumption costs for website hosting is a primary expense for websites. Through caching and other optimizations, CDNs are able to reduce the amount of data an origin server must provide, thus reducing hosting costs for website owners.

3.	Increasing content availability and redundancy - Large amounts of traffic or hardware failures can interrupt normal website function. Thanks to their distributed nature, a CDN can handle more traffic and withstand hardware failure better than many origin servers.

4.	Improving website security - A CDN may improve security by providing DDoS mitigation, improvements to security certificates, and other optimizations.


