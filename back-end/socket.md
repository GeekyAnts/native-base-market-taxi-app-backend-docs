# Socket

### Socket Server

The Socket Server functions as listed:

* Start socket server function is used to start the socket server.
* When the socket is connected, it first checks authenticity using JSON webtoken.
* This JWT access token is provided with the query parameter during the HandShake process between socket-server and socket-client.
* JWT access token is the same as that of token which is provided to the user at the time of login.
* If the socket is authenticated, then the sokcet is added to the **socket store **using addByuserId\(\), else the socket is disconnected.

### Socket Handler

Socket handler contains functionality which helps to manage different scenarios related to socket. Each scenario is taken as a story, which is handled separately. Socket handler manages three stories, namely: request trip, start trip and update location.

#### Request Trip

Request trip handler, handles many other trip request scenario.

* When the rider make a request for a trip, this emits a socket event from the rider side which is handled by
  `requstTripHandler()`
* Each request trip is stored in the mongoDB insidetriprequestcollection.
* During the trip request, thetripRequestStatuscan have following values:
  * **request:**
    Initially when the rider makes a request trip.
  * **noNearByDriver:**
    When the rider does not find any driver nearBy. Or when all the nearBy drivers reject the rider's request trip.
  * **rejected:**
    When the driver does not accept the request trip made by a rider.
  * **enRoute:**
    When driver accepts the request trip and enroutes towards the rider.
  * **arriving:**
    When the distance between the driver and the rider's pickup location is the range of 0.5 and 0.7 km.
  * **arrived:**
    When the driver has reached the rider's pick up location.
  * **completed:**
    When the driver starts the trip.

#### Start Trip

Start trip handler actuallly handles the ride which the rider takes.

* When the driver starts the trip, a socket event is emitted from the driver side which is handled by
  `start-trip() .`
* Every trip details are stored in the mongoDB within the trip collection.
* During the trip, thetripStatuscan have following values:
  * **onTrip:**
    When driver starts the trip
  * **endTrip:**
    Driver on reaching the destination

#### Update Location

* Update location handler handles updation of the GPS location of the rider or driver.

* It checks if the driver is in any tripRequest or trip.

* If yes, then an event is emitted to the corresponding rider with updated GPS location.
* Same procedure is followed at the rider side.



