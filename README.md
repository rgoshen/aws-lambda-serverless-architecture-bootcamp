# AWS Lambda & Serverless Architecture Bootcamp

[Udemy Course](https://www.udemy.com/course/aws-lambda-serverless-architecture/learn/lecture/12903128#overview)

## Table of Contents

- [AWS Lambda & Serverless Architecture Bootcamp](#aws-lambda--serverless-architecture-bootcamp)
  - [Table of Contents](#table-of-contents)
  - [Section 1: Getting Started With Serverless Computing on AWS](#section-1-getting-started-with-serverless-computing-on-aws)
    - [What is Serverless? (A 30,000 ft. View)](#what-is-serverless-a-30000-ft-view)
    - [How Serverless Works?](#how-serverless-works)

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
