# 2 - APIs in Node

### Learning Objectives <a href="#learning-objectives" id="learning-objectives"></a>

By the end of this lesson students should be able to:

* Define what each part of CRUD is and what it does
* Process a GET request using Express and Node to retrieve data from memory
* Process a POST request using Express and Node and store data in memory
* Process a PUT request using Express and Node and update existing data in memory
* Process a DELETE request using Express and Node to remove data from memory
* Install a third party library using `npm`
* What is a middleware

### CRUD Continued <a href="#crud-continued" id="crud-continued"></a>

We will now build a **CRUD** API. CRUD stands for Create, Retrieve, Update, Delete. If you think about it, this is what most applications do:

* Create some "resources"
* Retrieve them (GET them)This step will require you to use POSTMAN because our project does not have client interface (front-end part) with a HTML form for creating new quotes.
* Update them
* Delete them

Below are three in-class exercises that can be used to demonstrate parts of the API workshop below.

#### (1) Get Exercise <a href="#1-get-exercise" id="1-get-exercise"></a>

This is an instructor-led exercise that can be used to show how we can retrieve an element by ID using a GET request.

**Objective**

Change a quote API server to allow GETting a quote according to the given ID.

The id should be given in the URL structure like this:

> /quotes/2

You should use the starting project: [node-quotes-api](https://github.com/Migracode-Barcelona/node-quotes-api). This is because this project has quotes with IDs.

When you fork and clone the starting project, run `npm install` to install required dependencies.



#### (2) Post Exercise <a href="#2-post-exercise" id="2-post-exercise"></a>

This is an instructor-led exercise that can be used to show how we can add an element to an array

**Objective**

Change a quote API server to allow POSTs of new quotes.

The new quotes should be added to your quotes list, which is just an array in memory.

You can assume the POSTed quotes are all in the correct JSON format.

The route should use the HTTP method POST and should use the URL:

> /quotes





#### (3) Put Exercise <a href="#1-get-exercise" id="1-get-exercise"></a>

This is an instructor-led exercise that can be used to show how we can update existing data in memory using a PUT request.

**Objective**

Change the quote API server to allow updating a quote according to the given ID.

The route should use the HTTP method PUT and ID should be given in the URL structure like this:

> /quotes/2

This step will require you to use POSTMAN because our project does not have client interface (front-end part) with a HTML form for updating quotes.



#### (4) Delete Exercise <a href="#3-delete-exercise" id="3-delete-exercise"></a>

This is an instructor-led exercise that can be used to show how we can remove an element to an array

**Objective**

Change a quote API server to allow updating a quote according to the given ID.

The id should be given in the URL structure like this:

/quotes/2

You should use the `delete` HTTP method.

### Workshop <a href="#workshop" id="workshop"></a>

You can use this [Express Cheatsheet](https://github.com/nbogie/express-notes/blob/master/express-cheatsheet.md) to help you.

**API** stands for Application Programming Interface.

Read this description of what an API does from [How To Geek](https://www.howtogeek.com/343877/what-is-an-api/).

> Think of an API like a menu in a restaurant. The menu provides a list of dishes you can order, along with a description of each dish. When you specify what menu items you want, the restaurant’s kitchen does the work and provides you with some finished dishes. You don’t know exactly how the restaurant prepares that food, and you don’t really need to. Similarly, an API lists a bunch of operations that developers can use, along with a description of what they do. The developer doesn’t necessarily need to know how, for example, an operating system builds and presents a “Save As” dialog box. They just need to know that it’s available for use in their app.

An API does not have to be web-based. But in our work, since we are doing web development, we will work only with web-based APIs (also referred to as **Web Services**), and we will communicate with those services using the protocol for the Web: **HTTP**.

> **Checkpoint:** Let us recap what we know about HTTP before continuing.

#### Objective <a href="#objective" id="objective"></a>

Our **API** will manage Beyoncé albums:

* Create a new album,
* Retrieve a list of albums or a single album,
* Update an existing album's information
* Delete an album

We will build these endpoints:

`GET /albums` should return all the albums `GET /albums/:albumId` should return a single album (that matches the passed albumId) `POST /albums` should save a new album `PUT /albums/:albumId` should update the album (that matches the passed albumId) `DELETE /albums/:albumId` should delete the album (that matches the passed albumId).

#### GET /Albums <a href="#get-albums" id="get-albums"></a>

1. In `server.js` Add the endpoint for `GET /albums`.

```
const albumsData = [
  {
    albumId: "10",
    artistName: "Beyoncé",
    collectionName: "Lemonade",
    artworkUrl100:
      "http://is1.mzstatic.com/image/thumb/Music20/v4/23/c1/9e/23c19e53-783f-ae47-7212-03cc9998bd84/source/100x100bb.jpg",
    releaseDate: "2016-04-25T07:00:00Z",
    primaryGenreName: "Pop",
    url:
      "https://www.youtube.com/embed/PeonBmeFR8o?rel=0&amp;controls=0&amp;showinfo=0",
  },
  {
    albumId: "11",
    artistName: "Beyoncé",
    collectionName: "Dangerously In Love",
    artworkUrl100:
      "http://is1.mzstatic.com/image/thumb/Music/v4/18/93/6d/18936d85-8f6b-7597-87ef-62c4c5211298/source/100x100bb.jpg",
    releaseDate: "2003-06-24T07:00:00Z",
    primaryGenreName: "Pop",
    url:
      "https://www.youtube.com/embed/ViwtNLUqkMY?rel=0&amp;controls=0&amp;showinfo=0",
  },
];

app.get("/albums", function (req, res) {
  res.send(albumsData);
});
```

1. Test the endpoint with Postman. `GET /albums` should return a JSON reply with the array we specified.
2. Add another item to the array and test that the `GET /albums` returns three items.

#### Step 1: GET /albums/:albumId <a href="#step-1-get-albumsalbumid" id="step-1-get-albumsalbumid"></a>

**Complete in-class (1) GET Exercise at this point**

Sometimes, we do not want to _list_ all the information in one request, maybe we only want to get the information related to a single album. Imagine if we have a page to display the details of one album, we could call the server and get all albums then filter the one we need _client-side._ Would it not be more effective to tell the server to just return the one album we are interested in?

Let us add a new endpoint to return only a single album `GET /albums/:albumId`. In this case, _albumId_ will tell us what album we can return so the call will be something like `GET /albums/10` and that will return the album with that has _albumId_ 10.

This endpoint has something different. The endpoint `/albums/:albumId` has a _dynamic_ part, because the _albumId_ will vary depending on what the client sends. If we call `/albums/12` then albumId is 12, and if we call `/albums/10` then we will return the album with albumId 10, and so on.

**How can we achieve that using** `express` - `req.params`&#x20;

These are properties attached to the URL named route parameters. You prefix the parameter name with a colon (**:**) when writing your routes.

For instance,

```
  app.get("/albums/:albumId", (req, res) => {
   console.log(req.params.albumId)
  })
```

To send the parameter from the client, just replace its name with the value

```
  GET  http://localhost:3000/albums/123456
```

```
app.get("/albums/:albumId", function (req, res) {
  // req.params.albumId will match the value in the url after /albums/
  console.log(req.params.albumId);
  // now we can use the value for req.params.albumId to find the album requested
  // how do we "find" something in an array

  // finish the code yourself - it should end with res.send(album) where album is the single album you found  based on the id
});
```

**Tip** :- Install nodemon following previous week's [guide](https://syllabus.migracode.org/course-content/nodejs/week-1#step-7-setting-up-server-to-listen-to-changes-automatically)



#### Step 2: Add a new album <a href="#step-2-add-a-new-album" id="step-2-add-a-new-album"></a>

**Complete in-class (2) Post Exercise at this point**

> Our analogy with the Restaurant menu is somewhat incomplete. In a restaurant, we only GET items from the menu. In the world of APIs, we also have the possibility to create items, we can provide _ingredients_ to create a new dish. In this case, we provide some data (a payload) and we use a different verb **POST** (Create) as opposed to GET.

`POST /albums` should save a new album and return `200` with JSON `{ success: true }` to the user.

```
// notice .post (not .get)
app.post("/albums", function (req, res) {
  console.log("POST /albums route");
});
```

Let's start by testing using Postman. Do a `POST` request to the endpoint and make sure it prints the console.log message we have added.

> In Postman, change the request `method` to `POST` instead of `GET` and test our endpoint. It should log the message to the terminal but the request will hang because we did not end it, i.e. we did not say `res.send(something)`

So what format does the client send the data with? It is up to us, but since we already are familiar with `json`, let us use it.

In order for our _server-side_ to receive and use the data sent by the client. We will need to use a **middleware**. Lets take a pause to learn about middleware and then we will come back to this exercise.



#### What is a Middleware

Middleware is just a function which gives you access to `req` and `res` in the apps request-> response cycle.

#### **What does a middleware function look like?**

![](<../../../../.gitbook/assets/image (168).png>)

There are several important things to point out here:

1. Middleware functions usually have 3 standard params `req`, `res`, and `next`. The first two are objects, the last is a function that will call the next middleware function, if there is one.
2. Usually there is a _middleware chain_, meaning a chain of functions that are called one after the other, with the last function sending the response back to the browser. So we get the request from the browser, make any modifications and data additions, and then send a response back.
3. You must call `next()` (unless it’s the last function in the chain) or the request will just hang and eventually timeout. In the browser this will manifest as a really long spinner before a message of “connection timed out” or similar.
4. Any changes you make to `req` or `res` will be available in the next middleware function.
5. `req` and `res` are unique for each request. Meaning that the changes you make to `req` or `res` in one request will not be reflected in a new request.&#x20;

#### How do I write my own middleware for certain routes?

This is where middleware is the most useful.

![](<../../../../.gitbook/assets/image (210).png>)

When we run the above code, and request the `/user/someName` route, the server will check to see if the user is already logged in. If they are not, the server tells the browser to redirect to the `/login` route.



Now that we know what is a **middleware** function, lets continue with the exercise.

The **express.json()** function is a built-in middleware function in Express. It parses incoming requests with JSON payloads and is based on **body-parser.** It **** makes it easier for our endpoints to receive and understand different formats of data.

```
app.use(express.json()); // before our routes definition
```

Now we will receive the data as `req.body`.

```
app.post("/albums", function (req, res) {
  console.log("POST /albums route");
  console.log(req.body);
});
```

> Exercise: Use Postman to `POST` this data to `/albums` endpoint.

```
{
  "albumId": "13",
  "artistName": "Beyoncé",
  "collectionName": "B'Day (Deluxe Edition)",
  "artworkUrl100": "http://is5.mzstatic.com/image/thumb/Music/v4/6c/fc/6a/6cfc6a13-0633-f96b-9d72-cf56774beb4b/source/100x100bb.jpg",
  "releaseDate": "2007-05-29T07:00:00Z",
  "primaryGenreName": "Pop",
  "url": "https://www.youtube.com/embed/RQ9BWndKEgs?rel=0&amp;controls=0&amp;showinfo=0"
}
```

> Finish the code for the route `POST /albums` to add the album data to the albums list (how to amend an array?).

#### Step 3: Delete an album <a href="#step-3-delete-an-album" id="step-3-delete-an-album"></a>

**Complete in-class (3) DELETE Exercise at this point**

Lets look back at our original objectives.

> `DELETE /albums/:albumId` should delete the album that matches the passed albumId.

This means that `DELETE /albums/2` should delete an album with the id `2` and return `200` with JSON `{ success: true }` to the user.

The code will look like this:

```
// notice .delete
app.delete("/albums/:albumID", function (req, res) {
  console.log("DELETE /albums route");
});
```

Can you work out how to remove an album using this code?

