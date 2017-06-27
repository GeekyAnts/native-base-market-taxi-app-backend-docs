# Service

### Socket Store

SocketStore class is used to manage operation related to socket. It contains a store that includes mapping of userId with their socket. Also includes static methods such as addByUserId, getByUserId, removeByUserId, emitByUserId.

#### addByUserId\(\)

* **Description:** Used to add socket to the store with which user is connected to. This function maps between the socket and userId. By doing this we store all the sockets at one place that correspond to the user.
* **Parameter:**
  * Name : userId
    Type: Schema.Types.ObjectId
    Description : unique userId


  * Name : socket
    Type: Object
    Description: Socket object to which user is connected to
* **Response:**
  * Type : Object
    Description: Returns object with three properties: success \(bool\), message, data \(which is to be sent\).

#### getByuserId\(\)

* **Description:** Used to get all the socket objects to which user is connected.
* **Parameter:**
  * Name : userId
    Type: Schema.Types.ObjectId
    Description : unique userId
* **Response:**
  * Type : Object
    Description: Returns object with three properties: success \(bool\), message, data \(which is to be sent\).

#### emitByUserId\(\)

* **Description:** Emits an event to the user whose userId is provided in the parameters. This emits event to all the sockets to which user is connected.
* **Parameter:**
  * Name : userId
    Type: Schema.Types.ObjectId
    Description : unique userId


  * Name : eventName
    Type: String
    Description: name of the event which to be emitted


  * Name : payload
    Type: Object
    Description: payload contains the data which has to be sent over the socket

#### removeByUserId\(\)

* **Description:**
  Removes the socket from the store.
* **Parameter:**
  * Name : userId
    Type: Schema.Types.ObjectId
    Description : unique userId


  * Name : socketObj
    Type: Object
    Description: Socket object which is to be removed from the store
* **Response:**
  * Type : Object
    Description: Returns object with three properties: success \(bool\), message, data \(which is to be sent\).



