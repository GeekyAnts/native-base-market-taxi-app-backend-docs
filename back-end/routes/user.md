# Routes - User

**File Name:** user.js  
**File Path:**  /server/routes/user.js  
Contains route which register, update, view and delete the user details. These functionalities are included in User Controller.

#### Registration Route



1. **API Path:** api/users/register
2. **Description:** Register route is used to register a new user. User can be either a Rider or a Driver. This route also checks if user has already been registered or not.
3. **Parameters:**
   * Name: req
   * Type: Object

   <table class="table table-bordered">
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
                <th>Required</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>email</td>
                <td>String</td> 
                <td>true</td> 
            </tr>
            <tr>
                <td>password</td>
                <td>String</td> 
                <td>true</td> 
            </tr>
            <tr>
                <td>fname</td>
                <td>String</td> 
                <td>true</td> 
            </tr>
              <tr>
                <td>lname</td>
                <td>String</td> 
                <td>true</td> 
            </tr>
              <tr>
                <td>phoneNo</td>
                <td>Number</td> 
                <td>true</td> 
            </tr>
              <tr>
                <td>userType</td>
                <td>String</td> 
                <td>true</td> 
            </tr>
        </tbody>
    </table>

4. **Response:**
   Returns an object with three properties: success \(bool\), message, data.
   The third parameter data is an object with two properties: jwtAccessToken and user object.

   * Http Code: 200 
   * Name: returnObj
   * Type: Object

   <table class="table table-bordered">
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>success</td>
                <td>
                   boolean
                </td> 
            </tr>
            <tr>
                <td>message</td>
                <td>string</td>
                  </tr>
                    <tr>
                <td>data</td>
                <td>Object</td>
                  </tr>
        </tbody>
    </table>


#### Get User Details Route

1. **API Path:** api/users
2. **Method:** GET
3. **Description:** This is a protected route which gets the user details through JWT access token which is provided in the header.
4. **Parameters:**

   * Name: jwtAccessToken 
   * In: Header 
   * Type: String 
   * Description: JWT access token is used to check the authenticity of the user.


   * Name: res 
   * Type: Object 
   * Description: res is nothing but the response object which gets you the user details.

5. **Response:**

  * Http Code: 200 
  * Name: returnObj 
  * Type: Object

   <table class="table table-bordered">
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>success</td>
                <td>
                   boolean
                </td> 
            </tr>
            <tr>
                <td>message</td>
                <td>string</td>
                  </tr>
                    <tr>
                <td>data</td>
                <td>Object</td>
                  </tr>
        </tbody>
    </table>



#### Update User Details Route

1. **API Path:** api/users
2. **Method:** PUT
3. **Description:** This is a protected route which update the user details.
4. **Parameters:**

   * Name: req
   * Type: Object

   <table class="table table-bordered">
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>email</td>
                <td>String</td>
            </tr>
            <tr>
                <td>password</td>
                <td>String</td>
            </tr>
            <tr>
                <td>fname</td>
                <td>String</td>
            </tr>
              <tr>
                <td>lname</td>
                <td>String</td>
            </tr>
              <tr>
                <td>phoneNo</td>
                <td>Number</td>
            </tr>
        </tbody>
    </table>

   * Name: jwtAccessToken 
   * In: Header 
   * Type: String 
   * Description: JWT access token is used to check the authenticity of the user.


5. **Response:**
   * Http Code: 200 
   * Name: returnObj 
   * Type: Object

   <table class="table table-bordered">
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>success</td>
                <td>
                   boolean
                </td> 
            </tr>
            <tr>
                <td>message</td>
                <td>string</td>
                  </tr>
                    <tr>
                <td>data</td>
                <td>Object</td>
                  </tr>
        </tbody>
    </table>



#### Delete User Details Route

1. **API Path:** api/users
2. **Method:** DELETE
3. **Description:** Remove a user from the database.
4. **Parameters:**
   * Name: req 
   * Type: Object


   * Name: jwtAccessToken 
   * In: Header 
   * Type: String


   * Name: res 
   * Type: Object
     
5. **Response:**
   * Http Code: 200 
   * Name: returnObj 
   * Type: Object

   <table class="table table-bordered">
        <thead>
            <tr>
                <th>Name</th>
                <th>Type</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>success</td>
                <td>
                   boolean
                </td> 
            </tr>
            <tr>
                <td>message</td>
                <td>string</td>
                  </tr>
                    <tr>
                <td>data</td>
                <td>Object</td>
                  </tr>
        </tbody>
    </table>


