# 1 - Node and Express 101

### Learning Objectives <a href="#learning-objectives" id="learning-objectives"></a>

By the end of this lesson students should be able to:

* Explain what Node.js is.
* Explain what Express is.
* Create a simple REST API using Express.
* Explain what Postman is and how it works.
* Working with GET Requests using Postman.
* Working with POST Requests using Postman.
* Communicating with the server.
* Implement routing to return different resources depending on the URL.
* Implement query parameters to return different content.

### What is Node.js?

Node.js is an open-source\* and cross-platform JavaScript runtime environment. The _runtime environment_ is the _environment_ in which a program or application is executed. It's the hardware and software infrastructure that supports the running of a particular codebase in real time.

Node.js runs the V8 JavaScript engine (the core of Google Chrome) outside of the browser. This allows Node.js to be very performant. A Node.js app runs in a single process, without creating a new thread for every request. **Threads** are a way for a **program** to divide (termed "split") itself into two or more simultaneously (or pseudo-simultaneously) running tasks.

Node.js has a unique advantage because millions of front-end developers that write JavaScript for the browser can write the server-side code in addition to the client-side code without the need to learn a completely different language.

_**\*Open source**_ is a term that originally referred to _open source_ software (OSS). _Open source_ software is code that is designed to be publicly accessible—anyone can see, modify, and distribute the code as they see fit.

### What is Express? <a href="#a-vast-number-of-libraries" id="a-vast-number-of-libraries"></a>

Express.js or simply Express is a minimal, open source and flexible Node.js web framework designed to make developing websites, web apps, and APIs much easier. It lets you structure a web application to handle multiple different `http` requests at a specific URL (Uniform Resource Locator).

Express helps you respond to requests with **route** support so that you may write responses to specific URLs. The nice thing about it is that it’s very simple and it’s open-source.

A **route** is a section of **Express** code that links an HTTP action ( GET, POST, PUT, DELETE, etc.) to a URL path/pattern, and a function that is called to handle that pattern.

### Creating a simple Rest API

The **REST** abbreviation stands for representational state transfer. The definition can be conveyed with simpler words: data presentation for a client in the format that is convenient for it. One of the main points that you need to understand and remember is that REST is not a standard or protocol: it is an approach to, or architectural style for, writing APIs.

**API** stands for Application Programming Interface. It is a way to provide information for other applications. Basically, it enables communication between applications.

![](<../../../../.gitbook/assets/image (218).png>)

REST is an architectural style, and RESTful is the interpretation of it. This means that if your back-end server has a REST API and you make client-side requests (from a website/application) to this API, then your client is RESTful.

RESTful API best practices come down to four essential operations:

* receiving data in a convenient format
* creating new data
* updating data
* deleting data

### Get started

### **Step 1**: Go to the terminal and create a folder called node-web-server

```
mkdir node-web-server
```

****

### **Step 2**: Go inside the project and generate the `package.json` file using **`npm init`**

```
cd node-web-server
npm init
```

You can keep pressing 'enter' through all of the options that you will see in your terminal. After this, you will see that a file called `package.json` has been created automatically.

The terminal will look something like this once you execute `npm init`

```
npm init
This utility will walk you through creating a package.json file.
It only covers the most common items, and tries to guess sensible defaults.

See `npm help init` for definitive documentation on these fields
and exactly what they do.

Use `npm install <pkg>` afterwards to install a package and
save it as a dependency in the package.json file.

Press ^C at any time to quit.
package name: (new)
version: (1.0.0)
description:
entry point: (index.js)
test command:
git repository:
keywords:
author:
license: (ISC)
About to write to /home/yogi/new/package.json:

{
  "name": "new",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "",
  "license": "ISC"
}


Is this OK? (yes)
```

****

### **Step 3**: Install Express

```
npm install express
```

****

### **Step 4:** Create a file called `server.js` in the root/main project folder ( e.g. node-web-server )

```
touch server.js
```

This is the file where we will configure all our routes.



### **Step 5**: Paste the following code in your `server.js` file:

```
const express = require('express');
const app = express();

app.get('/', (req, res) => {
    res.send('Hello Express')
});

app.listen(3000, () => console.log("Server is up and running"))
```

_**Line 1:** We already installed Express in Step 3, but we need to make sure it is included in this file specifically so we can use its methods. In Node.js, when you want to use a package in another file, you must require it. You can think of require as a need to import something. You can instantiate the package at the top of your file. Instantiate means creating an example or single occurrence of something and we assign that example or instance to a variable, for example "express"_\
_**Line 2**: To initialise/create our server, we need to call the `express()`function. This will perform a set of operations behind the scene and create an Express application for us and we can assign it to the app variable._\
_**Line 4: `app.get`**is saying that when it gets that route, it should give the response that is specified in the function. It takes in two arguments: (1) the URL (2) the function that tells Express what to send back to the person making the request._\
_**Line 8:** One more step left: we need to set a port for our server to listen to. Think of a port as a door number; any requests that comes to the server will come via that door. Setting a port will allow us to find out where our server is running. We use the **`app.listen`**method to do this. This method takes two arguments: a **port** and a **callback** function telling it what to do once the server is running._

_**Note :**_ If the port `3000` is in use (e.g. you already have a project running on port `3000`), then your system will throw an error. In this case you will have to manually change port in _**Line 8** `app.listen(3001)`_ **or** _`app.listen(3002)`_ **or** _`app.listen(3003)`_ till you find the next available port and run the server with that.&#x20;

When you run `npm install package_name` in the terminal, the package you want gets added as one of the dependencies into the __ `package.json` file:

```
{
  “name”: “node-web-server”,
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "",
  "dependencies": {
     "express": "4.15.3",
     "jade": "*",
     "underscore": "^1.7.0"
  }
}
```

* The syntax it uses is semantic versioning **(SEMVER)**, which means you can specify which version of the dependency you would like.
* A star symbol (**\***) means it can be any version, whichever is the latest one.
* A carrot symbol (**^**) prior to the version means I want that version or anything newer.

**SEMVER :** Given a version number (e.g `"express": "4.15.3"` ) MAJOR.MINOR.PATCH, increment the:

1. ( `"express": "4.x.x"` ) MAJOR version when you make incompatible API changes,
2. ( `"express": "x.15.x"` ) MINOR version when you add functionality in a backwards compatible manner, and
3. ( `"express": "x.x.3"` ) PATCH version when you make backwards compatible bug fixes.

**Note :** We never installed "jade" and "underscore". These are mentioned for explaining SEMVER and you can ignore these packages here.



### **Step 6**: To run the application, change into the root directory of the project and type the following in the terminal:

```
node server.js
```

Go to your browser and type the following URL (use port 3000 or whichever port you used in the previous step)

```
http://localhost:3000/
```

You should see “Hello Express” on your screen.

**Note:** Whenever you make any changes in your project, you will have to **manually restart the server**. You can do this by pressing**`ctrl c` ** on your keyboard to stop the current server and then repeat the step to start the server:`node server.js`

####

### **Step 7**: Setting up a server to listen to changes automatically

Install the package _**nodemon**_ globally on your machine by using following command:&#x20;

```
npm install -g nodemon
```

When you install an npm package using the **-g** flag, that package gets installed in your system instead of in your program, and you do not need to install it ever again. Now you can use`nodemon` instead of`node` when running your app locally. Nodemon monitors your app for any changes and automatically restarts your application when you change anything. With the`node` command, you have to restart manually after you make changes.

```
nodemon server.js
```

Go to your browser and go to port 3000 (or whichever port you used in step 5)

```
http://localhost:3000/
```

You should see “Hello Express”.



### **Step 8:** Npm Scripts

`package.json` has various sections. `scripts` is one of them, and it allows you to write an npm script that you can run using `npm run <script-name>.`

```
"scripts": {
  "test": "echo \"Error: no test specified\" && exit 1"
}
```

Typically we can have a scripts section. The scripts are defined as JSON with the key-value script. Key is the command name that we will use to run and value is the command we want to run.

To exit the running the server, type `crtl c`. Instead of running the server with `nodemon server.js` every time, we can create an alias (a shortcut) for it in `package.json`.

Under the `scripts` property, add `"start: nodemon server.js"`.&#x20;

```
"scripts": {
  "test": "echo \"Error: no test specified\" && exit 1",
  "start": "nodemon server.js"
}
```

We can now run our server using `npm start` which will be an alias for `nodemon server.js`.Go to the terminal and type `npm start` and make sure that the server still runs.



### What is Postman

**Postman** is a scalable API testing tool which started in 2012 to simplify the API workflow in testing and development.

#### Why Use Postman?

Developers use Postman for the following reasons:

1. Accessibility - To use the Postman tool, a developer can log into their own account, making it easy to access files anytime, anywhere, as long as a Postman application is installed on the computer.
2. Use of Collections - Postman lets users create collections for their Postman API calls. Each collection can have sub-folders and multiple requests. This helps in organizing your test suites.
3. Collaboration - Collections and environments can be imported or exported, making it easy to share files. A direct link can also be used to share collections.
4. Debugging - Postman console helps to check what data has been retrieved, making it easy to debug tests.
5. Continuous Integration - With its ability to support continuous integration, development practices are maintained.

#### How to download and install Postman

Postman is an Open Source tool and can be easily downloaded. Here are the steps to install:

**Step 1)** Go to [https://www.postman.com/downloads/](https://www.postman.com/downloads/) and choose your desired platform  (Mac, Windows or Linux). Click _Download_

![](<../../../../.gitbook/assets/image (121).png>)

**Step 2)** The message _Your download is in progress'_should now display on the Apps page. Once the Postman download is completed, click on _Run_

![](<../../../../.gitbook/assets/image (58).png>)

**Step 3)** Installation Starts

![](<../../../../.gitbook/assets/image (213).png>)

**Step 4)** In the next window, signup for a Postman Account

![](<../../../../.gitbook/assets/image (160).png>)

NOTE: There are two ways to sign up for a Postman account. One is to create a new Postman account, and the other is to use a Google account. Though Postman allows users to use the tool without logging in, signing up ensures that your collection is saved and can be accessed for later use.

**Step 5)** Select the workspace tools you need and click _Save My Preferences_

![](<../../../../.gitbook/assets/image (28).png>)

**Step 6)** You will see the Startup Screen

![](<../../../../.gitbook/assets/image (215).png>)

#### How to use Postman to execute APIs

Below is the Postman Workspace. Let's explore the step by step process on **How to use Postman** and different features of the Postman tool!

**Note: Don't worry about all the features mentioned below, right now you just need a few.**

![](<../../../../.gitbook/assets/image (17).png>)

1. New - This is where you will create a new request, collection or environment.
2. Import - This is used to import a collection or environment. There are options such as import from file, folder, link or paste raw text.
3. Runner - Automation tests can be executed through the Collection Runner. This will be discussed further in the next lesson.
4. Open New - Open a new tab, Postman Window or Runner Window by clicking this button.
5. My Workspace - You can create a new workspace individually or as a team.
6. Invite - Collaborate in a workspace by inviting team members.
7. History - Past requests that you have sent will be displayed in History. This makes it easy to track actions that you have done.
8. Collections - Organize your test suite by creating collections. Each collection may have sub-folders and multiple requests. A request or folder can be duplicated as well.
9. Request tab - This displays the title of the request you are working on. By default, "Untitled Request" would be displayed for requests without titles.
10. HTTP Request - Clicking this will display a drop-down list of different requests such as GET, POST, COPY, DELETE, etc. In Postman API testing, the most commonly used requests are GET and POST.
11. Request URL - Also known as an endpoint, this is where you will identify the link to where the API will communicate with.
12. Save - If there are changes to a request, clicking save is a must so that new changes will not be lost or overwritten.
13. Params - This is where you will write parameters needed for a request such as key values.
14. Authorization - In order to access APIs, proper authorization is needed. It may be in the form of a username and password, bearer token, etc.
15. Headers - You can set headers such as content type JSON, depending on the needs of the organization.
16. Body - This is where you can customize details in a request commonly used in POST request.
17. Pre-request Script - This is a script that will be executed before the request. Usually, pre-request scripts for the setting environment are used to ensure that tests will be run in the correct environment.
18. Tests - These are scripts executed during the request. It is important to have tests as it sets up checkpoints to verify if response status is OK, retrieved data is as expected and other tests.

### Working with GET requests using Postman

GET requests are used to retrieve information from the given URL. There will be no changes done to the endpoint.

We will use the following URL for all examples in this Postman tutorial. It is a website for testing HTTP requests.

```
https://jsonplaceholder.typicode.com/users
```

In the workspace

1. Set your HTTP request to GET.
2. Copy the link above in the request URL field, &#x20;
3. Click Send
4. You will see a _200 OK_ message
5. There should be 10 user results in the body. This means that your test has run successfully.

![](<../../../../.gitbook/assets/image (135).png>)

**Note:** There may be cases that a Postman GET request is unsuccessful. It can be due to an invalid request URL, or that authentication is needed.

### Working with POST Requests using Postman

POST requests are different from GET request because there is data manipulation: the user adds data to the endpoint. Using the same data from the previous tutorial on the GET request, let's now add our own user.

**Step 1)** Click a new tab to create a new request.

![](<../../../../.gitbook/assets/image (22).png>)

**Step 2)** In the new tab

1. Set your HTTP request to POST.
2. Input the same link in the request URL: [https://jsonplaceholder.typicode.com/users](https://jsonplaceholder.typicode.com/users)
3. Switch to the Body tab

![](<../../../../.gitbook/assets/image (172).png>)

**Step 3)** In Body,

1. Click raw
2. Select JSON

![](<../../../../.gitbook/assets/image (149).png>)

**Step 4)** Copy and paste one user result from the previous GET request (see example below). Ensure that the code has been copied correctly with paired curly braces and brackets. Change`id` to 11 and`name` to any desired name. You can also change other details like the address.

```
[
    {
        "id": 11,
        "name": "Krishna Rungta",
        "username": "Bret",
        "email": "Sincere@april.biz",
        "address": {
            "street": "Kulas Light",
            "suite": "Apt. 556",
            "city": "Gwenborough",
            "zipcode": "92998-3874",
            "geo": {
                "lat": "-37.3159",
                "lng": "81.1496"
            }
        },
        "phone": "1-770-736-8031 x56442",
        "website": "hildegard.org",
        "company": {
            "name": "Romaguera-Crona",
            "catchPhrase": "Multi-layered client-server neural-net",
            "bs": "harness real-time e-markets"
        }
    }
]
```

![](<../../../../.gitbook/assets/image (140).png>)

**Note:** An online POST request should have the correct format to ensure that the requested data will be created. It is a good practice to use GET first to check the JSON format of the request. You can use tools like [https://jsonformatter.curiousconcept.com/](https://jsonformatter.curiousconcept.com/)

![](<../../../../.gitbook/assets/image (143).png>)

**Step 5)** Next,

1. Click _Send_.
2. _Status: 201 Created_ should be displayed
3. The posted data are showing up in the body.

![](<../../../../.gitbook/assets/image (157).png>)

### &#x20;<a href="#step-3---communicating-with-the-server" id="step-3---communicating-with-the-server"></a>

### Communicating with the server <a href="#step-3---communicating-with-the-server" id="step-3---communicating-with-the-server"></a>

Now that we've built the server, we need to communicate with it. We are going to control the server with **handler functions**.

#### What is a handler function? <a href="#what-is-a-handler-function" id="what-is-a-handler-function"></a>

When a request reaches the server, we need a way of responding to it. In comes the handler function. The handler function is a function that receives requests and handles them, hence the name.

The handler function is always called with a `req` and `res` (= request and response) object. The response object is what gets sent back to the client. It contains the information that gets displayed in the web page. You can decide what to send back in your response.

**What does a handler function look like in Express?**

The `get()` [method](http://expressjs.com/en/api.html#app.get.method) is one of the methods used to define a handler function in Express. It takes two parameters: the **endpoint** at which to trigger an action (we'll explain more about this in the next step), and the handler function that specifies exactly what to do. Here's a simple "Hello World!" example:

```
// req is the Request object, res is the Response object
// (these are just variable names, they can be anything but it's a convention to call them req and res)
app.get("/", (req, res) => {
  res.send("Hello World!");
});
```

Here, we are telling our server to respond with "Hello World!" when someone tries to access the webpage.

#### 1. Create your own handler function <a href="#1-create-your-own-handler-function" id="1-create-your-own-handler-function"></a>

Let us add a handler function to send back a message to the client. To do that, we're going to use the Express `send()` [method](http://expressjs.com/en/api.html#res.send). This will update the response object with the message.

Update your handler function like so:

```
const express = require("express");
const app = express();

app.get("/", function (req, res) {
  res.send("Yay Node!");
});

app.listen(3000, () => console.log("Server is up and running"))
```

> Exercise: Try to `console.log` the `request` object inside the handler function. Send the request again with Postman, then go to your terminal to see what it looks like. You should see a lot of data coming through.

#### 2. Check it out in Postman <a href="#2-check-it-out-in-postman" id="2-check-it-out-in-postman"></a>

Now, open Postman, and send a `GET` request to `http://localhost:3000`. If you see your message in Postman, congratulations! You have just sent your first response from the server.

### Routing <a href="#step-4---routing" id="step-4---routing"></a>

At the moment our server only does one thing. When it receives a request from the `/` endpoint, it sends back the same response: "Yay Node!".

> Try typing [http://localhost:3000/node](http://localhost:3000/node) and see what happens.

By making use of endpoints, we can make the server send different responses for different requests. This concept is called **routing**.

#### What is an endpoint? <a href="#what-is-an-endpoint" id="what-is-an-endpoint"></a>

An endpoint is the part of the URL which comes after `/`. For example: In this URL `https://jsonplaceholder.typicode.com/users` everything before `/users` is the base URL and  `/users` is the endpoint. It's the URL which we used in Postman example to send a request.

#### What are the elements of a URL? <a href="#what-is-url" id="what-is-url"></a>

![](<../../../../.gitbook/assets/image (40).png>)

#### Create your own endpoints and send different responses <a href="#create-your-own-endpoints-and-send-different-responses" id="create-your-own-endpoints-and-send-different-responses"></a>

We're going to try sending different responses at different endpoints. Remember the `app.get()` method? To set up routing in your server, we just need to repeat this method with different endpoints.

For example:

```
app.get("/", function (req, res) {
  res.send("Hello World!");
});

app.get("/chocolate", function (req, res) {
  res.send("Mm chocolate :O");
});
```

> **Exercise:** Add some code so that your server sends one message when the endpoint is `/node` and another one when it's `/migracode`.

### Query Parameters <a href="#step-5---query-parameters" id="step-5---query-parameters"></a>

So what is a query parameter?

In simple terms, a query string is the part of a URL after the question mark (?). It is meant to send small amounts of information to the server via the URL. This information is used as parameters to query a database or to filter results.

Here is an example of a URL with query strings attached:

> [https://stackabuse.com/?page=2\&limit=3](https://stackabuse.com/?page=2\&limit=3)

#### 1. Detect Query Parameters <a href="#1-detect-query-parameters" id="1-detect-query-parameters"></a>

We're going to try sending different responses at different endpoints. Remember the `app.get()` method? To set up routing in your server, we just need to repeat this method with different endpoints.

For example:

```
app.get("/", function (req, res) {
  let searchQuery = req.query.search;
  res.send("Hello World! You searched for " + searchQuery);
});
```

****

#### **Exercise:** Follow the instructions of [node-challenge-calculator](https://github.com/Migracode-Barcelona/node-challenge-calculator)
