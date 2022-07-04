# AWS

## Cloud computing

Cloud computing is the on-demand delivery of IT resources over the Internet with pay-as-you-go pricing. Instead of buying, owning, and maintaining physical data centers and servers, you can access technology services, such as computing power, storage, and databases, on an as-needed basis from a cloud provider like Amazon Web Services (AWS).

## Cloud computing with AWS

Amazon Web Services (AWS) is the world’s most comprehensive and broadly adopted cloud platform, offering over 200 fully featured services from data centers globally. Millions of customers—including the fastest-growing startups, largest enterprises, and leading government agencies—are using AWS to lower costs, become more agile, and innovate faster.

### Benefits:

-	Most functionality

-	Largest community of customers and partners


-	Most secure

-	Fastest pace of innovation


-	Most proven operational expertise

## EC2 Instance 
Secure and resizable compute capacity for virtually any workload.

Amazon Elastic Compute Cloud (Amazon EC2) offers the broadest and deepest compute platform, with over 500 instances and choice of the latest processor, storage, networking, operating system, and purchase model to help you best match the needs of your workload.
### Use Cases
•	Run cloud-native and enterprise applications.

•	Scale for HPC applications.


•	Develop for Apple platforms.

•	Train and deploy ML applications.


## EC2 For Humans
Where can we find EC2 on the AWS Console ?

To connect to your instance using the browser-based client from the Amazon EC2 console:

•	Open the Amazon EC2 console at https://console.aws.amazon.com/ec2/.

•	In the navigation pane, choose Instances.


•	Select the instance and choose Connect.

•	Choose EC2 Instance Connect.


•	Verify the user name and choose Connect to open a terminal window.

## Difference between T2 Micro and X1
T2 instances are a low-cost, general purpose instance type that provides a baseline level of CPU performance with the ability to burst above the baseline when needed.

X1 Instances are a part of the Amazon EC2 memory-optimized instance family and are designed for running large-scale and in-memory applications in the AWS Cloud.

Compared to other EC2 instances, X1 instances have one of the lowest price per GiB of RAM, and are ideal for running in-memory databases like SAP HANA, big data processing engines like Apache Spark or Presto, and high-performance computing (HPC) applications.

## Elastic Beanstalk

Elastic Beanstalk is an easy-to-use service that deploys managesand scales web apps and sevices for you.

## Relationship Between EC2 and Elastic Beanstalk

Elastic Beanstalk is one layer of abstraction away from the EC2 layer. Elastic Beanstalk will setup an "environment" for you that can contain a number of EC2 instances, an optional database, as well as a few other AWS components such as a Elastic Load Balancer, Auto-Scaling Group, Security Group.

Benefits of Using Elastic Beanstalk

•	Timesaving server configuration.

•	Powerful customization.

•	Cost-effective price point.



