# Routes - Auth

File Name :  auth.js  
File Path :   /server/routes/auth.js  
Auth route contains login and logout routes. Also routes can be added which require authentication. These functionalities are included in Auth Controller.

#### Login Route

1. **API Path:** api/auth/login
2. **Method:** POST
3. **Description:** Login route verifies email and password for the user. Once a user is authenticated, a token is generated.
4. **Parameters:**
   * Name: req
     Type: Object

<br/>
   <table class="table table-bordered">
        <thead>
            <tr>
                <th>Name</th>
                <th>In</th>
                <th>Type</th>
                <th>Required</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>email</td>
                <td>req.body</td>
                <td>String</td>
                <td>true</td> 
            </tr>
            <tr>
                <td>password</td>
                <td>req.body</td>
                <td>String</td>
                <td>true</td> 
            </tr>
            <tr>
                <td>userType</td>
                <td>req.body</td>
                <td>String</td>
                <td>true</td> 
            </tr>
        </tbody>
    </table><br />

   * Name: res
     Type: Object
5. **Response:**
   Returns an object with three properties: success \(bool\), message, data.
   The third parameterdata is an object with two properties: jwtAccessToken and user object.

* Http Code: 200
  Name: returnObj
  Type: Object

<br/>
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
    </table><br />



#### LogOut Route

1. **API Path:** api/auth/logout
2. **Method:**
   GET
3. **Description:**
   This is a protected route which requires authentication token in the header. Logout route simply changes the login status and logouts the user from the database.
4. **Parameters:**
   * Name: Authorization
     In: Header
     Description: Contains JWT access token required to check the authenticity of the user who makes a API call.


   * Name: res
     Type: Object
 
5. **Response:**
   Returns an object with three properties: success \(bool\), message, data. The third parameterdata is an object with two properties: jwtAccessToken and user object.
   * Http Code: 200
     Name: returnObj
     Type: Object

<br/>
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
    </table><br />


