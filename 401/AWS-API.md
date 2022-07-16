# AWS: API Gateway, DynamoDB and Dynamoose


## AWS API Gateway Overview

### What is Amazon API Gateway?

Amazon API Gateway is a managed service that allows developers to define the HTTP endpoints of a REST API or a WebSocket API and connect those endpoints with the corresponding backend business logic. It also handles authentication, access control, monitoring, and tracing of API requests.

### Why is Amazon API Gateway an important part of the Serverless ecosystem?

Within the Serverless ecosystem, API Gateway is the piece that ties together Serverless functions and API definitions. Being able to trigger the execution of a Serverless function directly in response to an HTTP request is the key reason why API Gateway is so valuable in Serverless setups: it enables a truly serverless architecture for web applications. When using API Gateway together with other AWS services, it’s possible to build a fully functional customer-facing web application without maintaining a single server yourself.
This brings the advantages of the serverless model—scalability, low maintenance, and low cost due to low overhead—to mainstream web applications.

### How does API Gateway integrate with other AWS services?

Many AWS services support integration with Amazon API Gateway, including:

 
 • AWS Lambda: run Lambda functions to generate HTTP API responses.

• AWS SNS: publish SNS notifications when an HTTP API endpoint is accessed.

• Amazon Cognito: provide authentication and authorization for your HTTP APIs.

API Gateway supports direct integrations that can be configured in the API Gateway user interface (or via the API Gateway’s own API) for the following actions:

• Invoking an AWS Lambda function.

• Invoking another HTTP endpoint, with or without VPC Link.

• Making an HTTP call against the API of any AWS service that provides an HTTP API.

• Returning a mock response generated within API Gateway without calling out to other services.

You can also connect an HTTP endpoint created in API Gateway with a service that doesn’t offer a native integration. Perhaps the best way to achieve this is to set up an AWS Lambda function that contains all the business logic for the integration and then connect that Lambda function with an HTTP endpoint in API Gateway.

### What are the some benefits of using Amazon API Gateway?

- Efficient API development

- Performance at any scale

- Cost savings at scale

- Easy monitoring

- Flexible security controls

- RESTful API options


### What two API types might you choose from?

- RESTful APIs

- WEBSOCKET APIs

## AWS DynamoDB Guide

### What is DynamoDB?

DynamoDB is a hosted NoSQL database offered by Amazon Web Services (AWS). It offers:
   
   • reliable performance even as it scales;
   
   • a managed experience, so you won't be SSH-ing into servers to upgrade the crypto libraries;
   
   • a small, simple API allowing for simple key-value access as well as more advanced query patterns.
      

### Under what circumstances would you recommend DynamoDB over MongoDB?

   
   • MongoDB is more popular than DynamoDB, partly due to its head start and partly due to its wider availability.
   
   • DynamoDB has a more hands-off operations model than MongoDB as you don't think to think about instances and scaling up or down.
   
   • At high scale, DynamoDB and MongoDB have very similar data modeling principles.
   
   • At lower scale, MongoDB has a more flexible data model.
   
   • DynamoDB's connection and security model make it a popular choice for use with serverless compute like AWS Lambda.


### Explain to a non-technical friend how DynamoDB works.

Amazon DynamoDB is a fully managed, serverless, key-value NoSQL database designed to run high-performance applications at any scale. DynamoDB offers built-in security, continuous backups, automated multi-Region replication, in-memory caching, and data export tools.

## Dynamoose

### What is Dynamoose?

Dynamoose is a modeling tool for Amazon's DynamoDB. Dynamoose is heavily inspired by Mongoose, which means if you are coming from Mongoose the syntax will be very familar.

### What are some key features of Dynamoose?

   • Type safety
   
   • High level API
   
   • Easy to use syntax
   
   • Ability to transform data before saving or retrieving documents
   
   • Strict data modeling (validation, required attributes, and more)
   
   • Support for DynamoDB Transactions
   
   • Powerful Conditional/Filtering Support
   
   • Callback & Promise support

