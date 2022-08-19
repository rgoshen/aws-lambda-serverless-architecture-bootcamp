# AWS Lambda & Serverless Architecture Bootcamp

[Udemy Course](https://www.udemy.com/course/aws-lambda-serverless-architecture/learn/lecture/12903128#overview)

## Table of Contents

- [AWS Lambda & Serverless Architecture Bootcamp](#aws-lambda--serverless-architecture-bootcamp)
  - [Table of Contents](#table-of-contents)
  - [Section 1: Getting Started With Serverless Computing on AWS](#section-1-getting-started-with-serverless-computing-on-aws)
    - [What is Serverless? (A 30,000 ft. View)](#what-is-serverless-a-30000-ft-view)
    - [How Serverless Works?](#how-serverless-works)
    - [How to Create 'Hello World' API with Serverless](#how-to-create-hello-world-api-with-serverless)

## Section 1: Getting Started With Serverless Computing on AWS

### What is Serverless? (A 30,000 ft. View)

- Serverless computing is the new trend in cloud computing that attempts to solve the challengs of applications that need to be fast, responsive, and scalable with almost no downtime.
- Serverless computing will help you build the next generation of systems that can handle demanding workloads and scale indefinitely without having to provision or manage any servers.

Traditional architecture:

- you got to create and setup servers,
- install operating systems,
- install and setupdatabases,
- manage software patches and hardware updates,
- manage capacity and scaling, ManageHigh-availability through load-balancing and so on

This server infrastructure and the computing power has its own costs, which are often substantial.

Serverless architecture:

- Serverless Architecture, all these mundane tasks of managing the underlying infrastructure are abstracted away from us.

 Serverless Computing still uses servers, but you no longer have to worry about managing them or worry about the uptime or availability or anything that has to do with the infrastructure part.

Advantages of Serverless vs. Traditional

- You kind of get to be more productive
- You can completely focus on writing your code without having to worry about the underlying support system
- So you simply upload your code to the cloud provider and it can be run on-demand as and when needed.

[back](#table-of-contents)

### How Serverless Works?

With Serverless, you write your code in the form of functions, just like you’d write a function in any programming language. And these functions then run in the cloud. So, you segregate your application logic in to small independent functions or microservices and upload them to the cloud provider.

These functions are stateless and can be invoked in repsonse to different events. These events could be file uploads, database updates, in-app activity, API calls, website clicks, or sensor outputs just like those from IoT devices and so on.

These serverless functions often run in Docker-like containers and hence several instances of these functions can be run concurrently, like in a Docker swarm for example, thus making them highly highly scalable.

Serverless means “Event-driven Computing” using “Small independent stateless functions” running inside “containers in the cloud”.

So, you have your code running on the cloud platform, AWS in our case.

Whenever the triggering event occurs, the cloud platform spins up a container or initializes a container, loads the function in it and executes the function. And this happens almost instantaneously, thereby allowing us to build applications that respond quickly to new information and thus enhance user experience. Once the function completes execution, it optionally returns a response back to the caller, and then finally exits or shuts down.

AWS Lambda and API Gateway are the two of the core services of the AWS serverless platform

[back](#table-of-contents)

### How to Create 'Hello World' API with Serverless

[AWS Management Console](https://us-west-1.console.aws.amazon.com/console/home?nc2=h_ct&region=us-west-1&src=header-signin#)

**Create an API**

1. Login in to `AWS Management Console`
2. Search for `API Gateway`
3. Choose an API type (Rest API in this case)
4. Click on **Build** button
5. Make sure REST is selected
6. Click on **New API** radio button
7. Name your API
8. Click on **Create API** button

Once completed, this will redirect you to Resources screen

- here we can create Resources and methods for the API

**Create an End Point/Resource manually**

1. Click on **Actions** drop down
2. Click on **Create Resource**
3. Name the resource
4. Click on **Create Resource** button

**Add a method to a resource**

1. Click on **Actions** drop down
2. Click on **Create Method**
3. Select the appropriate method
4. Click on the :heavy_check_mark: button
5. Select your Integration Type
6. Click on **Save** button

This will take you to the **Method Execution** screen

![method execution](assets/images/AWS_hw_method_execution.png)

When we make an API call, the incoming request is passed from the Method Request block tothe integration request block where we map or transform the incoming request to the formatthat our backend understands.

In our case there is no backend since we are simply mocking a response using the Mock integration Type.

The response received from the backend is then mapped or transformed in the Integration Response block to match the format that the calling application expects and then the Method response relays the response back to the client.

**Deployment**

1. Once all is configured, click on the **Actions** drop down
2. Select **Deploy API**
3. Choose **New Stage** from the **Deployment stage** drop down
4. Give your stage a name (ex. Test)
5. Click **Deploy** button

[back](#table-of-contents)
