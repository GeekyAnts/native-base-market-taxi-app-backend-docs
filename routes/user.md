# Routes - User

**File Name:** user.js  
**File Path:**  /server/routes/user.js  
Contains route which register, update, view and delete the user details. These functionalities are included in User Controller.

#### Registration Route



1. **API Path:**
   api/users/register
2. **Description:**
   Register route is used to register a new user. User can be either a Rider or a Driver. This route also checks if user has already been registered or not.
3. **Parameters:**
   * Name: req
     Type: Object
   * | Name | Type | Required |
     | :--- | :--- | :--- |
     | email | String | true |
     | password | String | true |
     | fname | String | true |
     | lname | String | true |
     | phoneNo | Number | true |
     | userType | String | true |
   * Name: res
     Type: Object
 
4. **Response:**
   Returns an object with three properties: success \(bool\), message, data.
   The third parameter data is an object with two properties: jwtAccessToken and user object.

   * Http Code: 200
     Name: returnObj
     Type: Object
   * | Name | Type |
     | :--- | :--- |
     | success | boolean |
     | message | String |
     | data | Object |



#### Get User Details Route

1. **API Path:**
   api/users
2. **Method:**
   GET
3. **Description:**
   This is a protected route which gets the user details through JWT access token which is provided in the header.
4. **Parameters:**
   * Name: req
     Type: Object
   * Name: jwtAccessToken
     In: Header
     Type: String
     Description: JWT access token is used to check the authenticity of the user.


   * Name: res
     Type: Object
     Description: res is nothing but the response object which gets you the user details.
5. **Response:**
   * Http Code: 200
     Name: returnObj
     Type: Object
   * | Name | Type |
     | :--- | :--- |
     | success | boolean |
     | message | String |
     | data | Object |



#### Update User Details Route

1. **API Path:**
   api/users
2. **Method:**
   PUT
3. **Description:**
   This is a protected route which update the user details.
4. **Parameters:**
   * Name: req
     Type: Object
   * | Name | Type |
     | :--- | :--- |
     | email | String |
     | fname | String |
     | lname | String |
     | phoneNo | Number |
   * Name: jwtAccessToken
     In: Header
     Type: String
     Description: JWT access token is used to check the authenticity of the user.


   * Name: res
     Type: Object
5. **Response:**
   * Http Code: 200
     Name: returnObj
     Type: Object
   * | Name | Type |
     | :--- | :--- |
     | success | boolean |
     | message | String |
     | data | Object |



#### Delete User Details Route

1. **API Path:**
   api/users
2. **Method:**
   DELETE
3. **Description:**
   Remove a user from the database.
4. **Parameters:**
   * Name: req
     Type: Object


   * Name: jwtAccessToken
     In: Header
     Type: String


   * Name: res
     Type: Object
5. **Response:**
   * Http Code: 200
     Name: returnObj
     Type: Object
   * | Name | Type |
     | :--- | :--- |
     | success | boolean |
     | message | String |
     | data | Object |



