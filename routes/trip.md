# Routes - Trip

File Name :  trip.js  
File Path :   /server/routes/trip.js  
It has all the protected routes and contains route related to user trip. These functionalities are included in Trip Controller.

#### User Trip History Route

1. **API Path:**
   api/trips/history
2. **Method:**
   GET
3. **Description:**
   This route get the details of all the trip in which user is involved.
4. **Parameters:**
   * Name: req 
   * Type: Object


   * Name: jwtAccessToken 
   * In: Header 
   * Type: String 
   * Description: JWT access token used to check the authenticity of the user.
  

5. **Response:**
   Returns an object with three properties: success \(bool\), message, data.
   The third parameterdatais an object with two properties: jwtAccessToken and user object.
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



