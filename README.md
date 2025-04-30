<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# APIs with Lambda + API Gateway

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-compute-api)

**Author:** Vijay Pratap Singh Hada  
**Email:** vijaypratapsinghhada9@gmail.com

---

![Image](http://learn.nextwork.org/blissful_yellow_calm_donkey/uploads/aws-compute-api_c9d0e1f2)

---

## Introducing Today's Project!

I will demonstarte how to set up serverless architecture and manage API's and I'm doing this project to  learn about AWS lambda function which is funcation as a service and API Gateway and also doing this to understand how things work behind the scenes in cloud three-tier architecture. 

### Tools and concepts

The services I used were AWS Lambda to run serverless functions and API Gateway to create and manage my API. Key concepts I learned include Lambda functions, which let you run code without managing servers, and the significance of API documentation, which helps users understand how to use the API effectively.

### Project reflection

This project took me approximately 2 hours and 30 minutes to complete.It was  most rewarding to see the complete setup work seamlessly and to gain a deeper understanding of serverless architecture and API management.

I did this project today to learn how to create a serverless API using AWS services. I wanted to understand how Lambda functions and API Gateway work together. This project met my goals by giving me hands-on experience with these technologies. 

---

## Lambda functions

AWS Lambda is a serverless compute service that allows you to run your code without the need to manage any servers. This means you only pay for the time your code is actually running, not when it’s idle. It can automatically scale to handle any number of requests, making it very efficient for various applications. In this project, I'm using Lambda to run code that retrieves data from a database, ensuring that users get the information they need quickly and efficiently.



The code I added to my function will grab the user ID from the event that triggers the function, such as when a user submits their ID through a form on a website. It then queries the DynamoDB database for a piece of data that matches that user ID. Additionally, the code includes error handling to return specific messages if the user ID is not valid or does not exist in the database. This ensures that users receive accurate information and feedback when attempting to retrieve their data.

![Image](http://learn.nextwork.org/blissful_yellow_calm_donkey/uploads/aws-compute-api_a1b2c3d5)

---

## API Gateway

APIs are tools that help different software systems communicate with each other. They act like messengers, carrying requests and responses between applications. There are various types of APIs, such as REST, HTTP, and WebSocket. Each type serves different purposes; for instance, REST APIs are ideal for standard web interactions, while WebSockets enable real-time communication, and HTTP APIs are used for routing requests. My API is a REST API because I will set it up to connect users with the Lambda function in an effective way.

Amazon API Gateway is an AWS service that makes it easy for developers to create, publish, maintain, monitor, and secure APIs at any scale. It manages incoming requests, directing them to the right services and ensuring that only authorized requests are processed. I'm using API Gateway in this project to handle user requests and send them to the Lambda function for processing. After that, API Gateway returns the results to the users, making the interaction safe and efficient.


When a user makes a request, the API Gateway receives the request and forwards it to the Lambda function. The Lambda function processes the request, retrieves the necessary data, and generates a response. After processing, the Lambda function sends the results back to the API Gateway, which then returns the information to the user. This teamwork between API Gateway and Lambda ensures that requests are handled quickly and securely, giving users the information they need efficiently.




![Image](http://learn.nextwork.org/blissful_yellow_calm_donkey/uploads/aws-compute-api_m3n4o5p6)

---

## API Resources and Methods

An API is made up of resources, which are individual endpoints that help the API manage different functions. Each resource represents a specific task, making it easier to organize and handle requests. For example, one resource might allow users to get their profiles, while another resource could be used to send messages. Organizing the API into resources simplifies development and maintenance.

Each resource consists of methods, which are actions that can be taken on that resource. These methods use standard HTTP commands to work with data over the internet. For instance, the GET method retrieves data, the POST method adds new data, the PUT method updates existing data, and the DELETE method removes data. By using these methods, we can efficiently manage how our API handles various requests.



I created a GET method for the /users resource, which enables the API Gateway to retrieve user data. When a user makes a request, the API Gateway will forward that request to the Lambda function I set up, called RetrieveUserData. This function processes the request, accesses the DynamoDB table, and returns the necessary user information back to the API Gateway, which then sends the response to the user.

![Image](http://learn.nextwork.org/blissful_yellow_calm_donkey/uploads/aws-compute-api_c9d0e1f2)

---

## API Deployment

When you deploy an API, you deploy it to a specific stage. A stage is a snapshot of your API at a particular moment, making it easier to manage different versions. I deployed to the production stage, which is the live environment where my API is fully functional. In this stage, the API deals with real traffic and is used by actual users, ensuring that everything works as expected.

To visit my API, I opened my browser and entered the URL: `https://1xich0uy8a.execute-api.ap-south-1.amazonaws.com/prod` in a new tab. However, I encountered an error because I have not set up the DynamoDB table yet. This happens often, and once the table is created, the API will work properly as intended.

![Image](http://learn.nextwork.org/blissful_yellow_calm_donkey/uploads/aws-compute-api_3ethryj2)

---

## API Documentation

For my project's extension, I am writing API documentation because it offers clear guidance on how to use the API effectively. This documentation covers the API's endpoints, methods, parameters, and possible responses. Good documentation is important for developers since it helps them understand the API's functionality and ensures smooth integration into their applications. By producing detailed documentation, I improve collaboration and make it easier for others to utilize the API in their projects.

Once I prepared my documentation, I published it to the production stage of my API. I chose the documentation type as API and included the required JSON details, which give an overview of the API's functionality. Publishing my API to a specific stage is important because it ensures that the documentation matches the current version of the API deployed in that stage. This helps maintain consistency and clarity for users who interact with my API.

My published and downloaded documentation provided a detailed overview of my API, including the x-amazon-apigateway-documentation section at the bottom. This section features information automatically generated by API Gateway, such as the API's version, title, resources like /users, and the methods available, like GET. While the generated documentation offers useful information, my manually written section adds more customization and clarity, helping users understand how to utilize the API more effectively.

![Image](http://learn.nextwork.org/blissful_yellow_calm_donkey/uploads/aws-compute-api_z9a0b1c2)

---

---
