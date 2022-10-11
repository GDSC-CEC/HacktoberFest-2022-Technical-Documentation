# Application Programming Interface

Have you heard the term API before? If not, then don't worry, you'll learn about APIs in this blog.

API is literally everywhere, whether you are posting posts or stories on Instagram or ordering food through Zomato, you are using different APIs unknowingly. Cool, right?

So enough of the suspense part, now let's start with the definition of the APIs, and then we'll dive deep into the technical detail.

<br>

## What is an API?
![Image](https://cdn.hashnode.com/res/hashnode/image/upload/v1653940767645/IqsbTe3r8.avif?auto=compress,format&format=webp)

API is nothing but just a digital waiter. But wait, what does that even mean?

You've probably gone to a restaurant, right? So, what happens there? You just sit at the table and when it's time to order food then you'll call someone and not just directly go inside the kitchen, aren't you?

In this case, the critical link that will connect you with the chef is known as the waiter. The waiter will act as an interface between you and the chef. Here neither you can directly talk to the chef nor the chef can directly deliver food to your table. Thus, both have to communicate with each other with the help of the waiter.

Just like this, API is also a waiter in the Client-Server Architecture who acts as an interface and helps different services to communicate with each other.

![image](https://cdn.hashnode.com/res/hashnode/image/upload/v1653940795125/Ypeje8GVb.avif?auto=compress,format&format=webp)

In more technical terms, the API stands for Application Programming Interface. It helps different services to communicate with each other.

Thanks to the APIs that as a developer we don't have to build something from scratch, instead we can use the APIs of existing services to integrate their functionality into our project.

For example, you've probably used Zomato to order your food. There you've seen that you can locate your driver through a map, right? So does Zomato actually launch their satellites into the earth's orbit to track location? No, otherwise it'll bankrupt the entire company. So how they are locating us? They are actually using the Google Maps API. As Google's satellites are already out there in Earth's orbit to track locations and google also launched its Google map API in 2005. Therefore, with the help of this API, Zomato is using the Google Map functionality in their app.

## Why we should use APIs?
We should use APIs because:
* API makes the life of developers easy
* Software has become more complex and collaborative over the years. And, developers no longer need to create every service from scratch
* APIs allow developers to access data from a service (like Google or Twitter) without any knowledge of how the codebase has been implemented.
* API also acts as a security layer as it is giving the user only the final food. It is not showing the recipe of the food or how the food is being prepared internally. And by the food, I mean data.

## Role of Request-Response Cycle
![image](https://cdn.hashnode.com/res/hashnode/image/upload/v1653941363420/d4EoBN1VC.PNG?auto=compress,format&format=webp)

A Request-Response Cycle is when a client sends a request to the server and in return, the server sends back some kind of response to the client.

* Client: Any entity that can send a request to the internet
* Network: You can think of it as the internet
* Server: It is the place where your Requested data is located

## Request
There are generally three ingredients when it comes to making a request:
* Method: It is used to tell the server what you want to do with the Data. There are various Methods out there but the main ones are:
    * GET: Used to get the data from the server
    * POST: Used to send data to the server
    * PUT/PATCH: Used to update data that are present in the server
    * DELETE: Used to delete data from the server


* Address: It is the address of the server
* Path: It is the destination where a request can be heard and executed

## Response
A body can also be sent to the client by the server in response. This body of the response can be in any of the following forms:

* form data
* JSON
* text
* HTML
* XML
* files
* GraphQL … and more!

While receiving a response from the server you also get a status code that tells you what happens with your request.

200 OK is usually the best response that the API works as 200 OK means Successful.

The most common examples are: 201 Created, 400 Bad Request, 401 Unauthorized, 403 Forbidden, 404 Not found.