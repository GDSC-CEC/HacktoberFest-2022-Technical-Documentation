# Postman

![Postman](https://miro.medium.com/max/1100/1*V1DtI0ibW6nuisexHAK09A.jpeg)

<br/>

[API](https://github.com/GDSC-CEC/HacktoberFest-2022-Technical-Documentation/blob/main/ShaileshKumar007.md) or Application Programming Interface is a simple and flexible way to communicate (fetch or give information) between web services. If we have the intention to build, test, and modify an API, we need to choose some development tool and one of the common technologies we could learn is POSTMAN. It is used by over 5 million developers from all over the world.

Postman helps developers embed the required functionality into their system. The API helps with the HTTP requests like GET, POST, PUT, PATCH, DELETE, with the environments that can later be used and to convert the API to code in the programming languages like JavaScript and Python.

Let’s see how the Postman software is used to send and receive requests while we implement an API. We can also POST the data to the server via this tool. The software testing tool makes sure that the API testing is done very efficiently by adding on the documentation of the APIs.

## Formal Definition of Postman

Postman can be defined as a software testing API platform that integrates a simple Graphic User Interface with an intention of an easy view of the HTTP requests and responses in the system. The impressive feature of the postman is that you don’t need to write an HTTP client network code but can instead build test suites called collections which will then help the interaction between Postman and the API.

<br/>

## Concepts to know while learning Postman

### API

API or Application Programming Interface is a simple and flexible way to communicate (fetch or give information) between web services. When we use any the applications like Instagram, Facebook, Twitter, or LinkedIn, we use an API.

<br/>

### HTTP

Hypertext Transfer Protocol or HTTP is the communication between clients and servers in the form of requests and responses. A client sends an HTTP request using a browser to the server where the request is then processed. Following is the response the server sends to a client. All kinds of data can be transmitted via HTTP like text, images, audio, video, etc. GET, POST, PUT, PATCH, HEAD, and DELETE are the most used HTTP operations. 

<br/>

| **Let's look at the five major components of HTTP request: -** |
| -------------------------------------------------------------- |
| HTTP Operations: GET, PUT, POST, DELETE |
| Uniform Resource Identifier (URI) to locate a resource |
| HTTP version (HTTP v1.1) |
| Content-Type: application/JSON, Content-Length: 511) Request Headers |
| Payload |
| **Likewise, the core components are: -** |
| The status of the server is indicated by the Status?Response Code. (404-resource not found and 200-response ok) |
| The response header is where key-value pairs of metadata for the HTTP response message are stored—for instance, content length, content type, response date, and server type. |


<br/>

### Global Unique Identifier

THe Global Unique Identifier (GUID) includes hexadeimal digits separated hy hyphens. The postman identifier GUID fulfills the goal of uniqueness. 

<br/>

## What programming language is used for postman tests ?

Postman tests are run using Javascript.

<br/>

## Using Custom Javascript libraries in our scripts with an example

We may utilize the many built-in tools and libraries that Postman offers to include our pre- or post-request scripts or test cases. Consider the use of the moment.js library. It offers a variety of helpful methods for formatting data around time. Consider a POST request that must provide the generated date for the user, who anticipates the format "DD/MM/YYYY." You can use the moment library with just one line of code. To obtain the data with the proper formatting and then store it in an environment variable, we must add the following lines of code to our pre-request script:

```
var moment = require('moment');

pm.environment.set('createdDate',moment().format('DD/MM/YYYY'));
```

<br/>

## What is Postman cloud ?

Postman cloud is a shared repository from where you - as a business can have the access Postman collections. It helps you immediately save your work in the clous after you login. As a team member, you can access the data and collections from anywhere you like. 

However, the suggestion to save your work in Postman cloud is not preferred if your company data needs to be confidential. There is a security risk when Postman asks you to sign in to save your work. 

<br/>

## Logging Variable Values in Postman 

The use of following command can be used to log the variable values on the console. 

`console.log(pm.varaibles.get("variable_name));`

And to access these variables, use variable name `{{var}}` 

<br/>

## Variables scopes by Postman 

There are variety of variable scopes provided by Postman: -

| Variable scopes |
| --------------- |
| Global Variables | 
| Local Variables |
| Environment Variables |
| Collection Variables |
| Data Variables |

<br/>

## Postman authorization methods

Postman has the following API request authorization options to choose from: -

| **Authorization Methods** |
| --------------------- |
| API Key |
| Basic auth |
| Digest auth |
| Hawk Authentication |
| Oauth 1.0 |
| Oauth 2.0 |
| Bearer Token |
| NTLM Authentication |
| AWS Signature |

<br/>

## Basic Auth and Digest Auth

Basic Auth is a method of authorization offered by Postman for HTTP user agents, such as web browsers, to enter login and password. It becomes connected with the request after the username and password are entered.

One of Postman's authorization techniques is digest auth or digest authorization. Through this method, clients can send requests to the API first and then receive responses from the server, such as 401 illegal responses and numbers that can only be used once as absolute values. 

<br/>

## API requests supported by Postman

| **API Requests** |
|----------- |
| GET |
| POST |
| PUT |
| PATCH |
| COPY |
| DELETE |
| HEAD |
| OPTIONS |
| LINK |
| UNLINK |
| PURGE |
| LOCK |
| UNLOCK |
| PROPFIND |
| VIEW |

<br/>

## Can we reuse the authentication token for multiple requests ?

**Yes!!!** You can reuse the authentication token for multiple requests. You can create a collection - add all requests with the same authentication token and then finally assign the collection with the auth token to the collection. This will allow you to reuse the aforementioned multiple requests. By choosing "Inherit auth from parent" under the Authorization tab, we may apply it to each request separately.

<br/>

## Writing test cases for basic authentication on Postman

One of the authentication methods offered by Postman, Basic Authentication, ensures we can specify the username and password along with the API calls. We can achieve this by first configuring the API's credentials by:

Going to the Authorization tab
From the drop-down option, choose Basic Auth
Enter the API's username and password in the corresponding fields
You can write the test cases like this:

```
pm.test("Is the Request Authenticated?", function () {

       var jsonData = pm.response.json();

       //if authenticated then assert to true

pm.expect(jsonData.authenticated).to.eql(true);

  });

pm.test("Is the Content-Type present?", function () {

pm.response.to.have.header("Content-Type");

  });

pm.test("Is it a successful POST Request?", function () {

pm.response.to.have.status(200);

  });
  ```

  <br/>

## Setting same headers for all requests in Postman Collection

Pre-request scripts are supported at the collection level and for individual requests in Postman. Any script that applies to every request in the Collection may get included in the pre-request scripts. The steps are as follows:

To access the pre-request tab, right-click the Collection.

Add the script's lines of code below to add a request header for each request included in the Collection.

```
pm.request.headers.add({

    key: 'TestHeader',

    value: 'testValue'

});
```

To save the script, click Update.

Run the request in the Collection and check the Postman console to ensure that the headers have been added.

<br/>

## Saving Responses of API to a file 

There are only two ways we can save an API response to a file in Postman: - 

| **The ways to save an API response to file a file in Postman** |
| -------------------------------------------------------------- |
| Click the download button in the response section |
| Press arrow next to send button - there will be an option to send and download. When you click it - Postman prompts you for the location to save the response after executing the request. |

<br/>

## Advantages of using Postman

There are of the merits of using Postman over other alternatives. 

| **Advantages of Postman** |
| --------------------- |
| Postman is easily accessible since it can be used anywhere with just an installation and login activity. |
| With the help of Postman, you can build collections for the API calls and create multiple requests and subfolders that will lead to an organized test suite. |
| The test environment of Postman includes verifying successful HTTP response status to add them to each of the API calls and thus test the checkpoints. |
| Automation testing can be performed repeatedly with the Collection Runner or Newman — saving time for repeated tests. |
| Multiple environments are formed to make the test replication less because the different setting has the same collection. |
| Since the data retrieval is tracked — debugging is easy. |
| The collections can be imported and exported with a direct connection to share them. |
| Continuous integration is supported. |

<br/>

## Limitations of Postman 

As much as the advantages of Postman is high - there are some limitations as well. 

| Limitations of Postman |
| ---------------------- |
| Postman cannot process more than 1000 API requests. |
| Large Projects have difficulty managing collections adn requests. |
| SInce there is dynamic API requests - the coding workspace will lead to code duplication. |

<br/>

## Alternatives of Postman

Postman is used for API testing and can be replaced with some other development tools like the ones below:

| **Alternatives of Postman** |
| --------------------------- |
| Tricentis Tosca |
| Katalon Studio |
| Apigee |
| Jmeter |
| SoapUI |