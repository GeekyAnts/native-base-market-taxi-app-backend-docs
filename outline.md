# Outline

#### Initiating Server

```
mongod
```

**Mongod**

is the primary daemon process for the MongoDB system.

```
npm start
```

Starts the node server and executes`index.js`of the project.

#### Index.js

Mainly performs three tasks in following order:

1. **MongoDb connection:**
   Mongoose makes a connection to mongoDB.
2. **Socket connection:**
   Starts the socket server
   \(/config/socket-server.js\)
3. **Node server:**
   Starts the node server and configure port
   \(/config/express.js\)

#### MongoDB Models

All the mongoDB models or schemas are defined under/server/models.

#### Socket Server

Socket-server performs following functionalities :

1. Starts the socket server
2. Once when client is connected, it checks for authentication
3. If successfully authenticated, Socket Handler is called to handle different socket scenarios
   \(/server/socketHanlder/index.js\)

#### Socket Handler

Socket Handler handles three scenarios, namely:

* **requestTripHandler:**
  Handles all the request-trip events
  \(request-trip.js\)
* **startTripHandler:**
  Handles all the event related to trip
  \(start-trip.js\)
* **updateLocationHandler:**
  Handles event related to updation of user's GPS location
  \(update-location.js\)

#### Express JS

Express JS contains all the configuration details related to node server. It performs the following tasks:

1. Create and start server
2. Add different middleware namely:
3. * **bodyParser:**
     Parse body params and attache them to req.body
   * **cookieParser:**
     Parse Cookie header and populate req.cookies with an object added as key by the cookie names.
   * **Compress:**
     Helps in decreasing the size of the response body and improve the speed of the API calls.
   * **Passport:**
     Helps to authenticate different API call.
   * **Helmet:**
     Helps to protect the application from different attacks such as cross-site scripting \(XSS\), script injection.
   * **Cors:**
     It helps in connecting different domain to the application i.e enable cross origin resource sharing.
   * **APIError:**
     Handles any other error that occurred inside of an API calls such as:
     API not found, internal server error, parameter validation error.

   * **Api route:**
     Manage various other routes of the application
     \(/server/routes/index.js\)

#### Passport JS

This module lets you authenticate endpoints using a JSON web token and passport-jwt. A passport middleware is added to all the routes and socket which will check for authorised token. We can also change the strategy of the passport in thepassport-config.jsfile.

#### Api Routes

It handles the different routes of the application, namely:

* **users:**
  This route contain different routes related to the user such as registration of new user, updating the user details, etc.
* **auth:**
  Manages the login and logout route. This route handles the authentication of the user by generating the token.
* **trips:**
  Handles the user trip related route such as getting the trip history of the user, etc.

#### Controllers

Following are the controllers defined for the above mentioned routes:

* **User Controller**
  Performs user related functions, such as:
* * Create new user
  * Get user details
  * Update user details
  * Delete user
* **Auth Controller**
  Performs user authentication tasks: Login and LogOut

* **Trip Controller**
  Defines trip related functions such as getHistory.



