# API - Trip

**File Name:** admin.js  
**File Path:**  /server/routes/admin.js  
Contains all possible route which an admin about can access about trip such as details of all trip, specific trip, all trips of specific user etc.

* **Contents:**
* All Trip Details
* Specific Trip Details
* User Trip Details
* Revenue Details

#### All Trip Details

1. **API Path:** api/admin/trip
2. **Method:** GET
3. **Description:**

   * This route fetch data related to all the trips which a user \(both rider and driver\) has commuted.

     Also it has a filter functionality which is use to filter the data based on the tripStatus.

   * Renders paginated data.

   * Functionality:
     `./controllers/admin-trip.js`
   * Includes a filter functionality, which filters the data based on the
     **tripStatus**

4. **Parameters:**

   <table class="table table-bordered">
        <thead>
            <tr>
                <th>Name</th>
                <th>req</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>type</td>
                <td>
                   object
                </td> 
            </tr>
            <tr>
                <td>Contains</td>
                <td>Query: { limit: Number,
 pageNo: Number, Name: pageNo, Type: Number, Name: filter, Type: string
}</td>
                  </tr>
        </tbody>
    </table>

   * Name: res

     Type: Object

     **Description:** Response object returned to the api which contains collection of trip details.

     Filter can take three values namely: **All** \(default\), **Ongoing** and **Completed**  

5. **Response:**

   * Returns object with four properties:
     **success **\(bool\), **message**, **data **and **meta .**
   * **Data** field is an array of trip object containing all the details of the trip.
   * **Meta** field contains fields related to pagination such as totalNoOfPages, currPageNo, limit etc.

   * **Http Code**: 200

     **Name**: returnObj

     **Type**: Array of object

#### Specific Trip Details

1. **API Path:** api/admin/trip/:tripId
2. **Method:** GET
3. **Description:**
   * This route fetch details of a specific trip, including rider and driver details.
   * Requires **trip ID**  as input parameter.
   * Functionality: `./controllers/admin-trip.js`
4. **Parameters:**

 <table class="table table-bordered">
      <thead>
          <tr>
              <th>Name</th>
              <th>req</th>
          </tr>
      </thead>
      <tbody>
          <tr>
              <td>type</td>
              <td>
                 object
              </td> 
          </tr>
          <tr>
              <td>Contains</td>
              <td>params: {
                 Name: tripId,
                   Type: string
                }</td>
          </tr>
      </tbody>
  </table>

   * Name: res

     Type: Object

     **Description:** Response object returned to the api which contains requested trip details.

5. **Response:**

   * Returns object with three properties:
     **success**\(bool\), **message** and **data**
   * **Data** field is an object containing the details of requested trip along with rider and driver details.

   * **Http Code**: 200

     **Name**: returnObj

     **Type**: Array of object

#### User Trip Details

1. **API Path:** api/admin/trip/user/:userId
2. **Method:** GET
3. **Description:**
   * This route fetch details of all the trips commuted by an user.
   * Requires **user ID **as input parameter.
4. **Parameters:**

   <table class="table table-bordered">
        <thead>
            <tr>
                <th>Name</th>
                <th>req</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>type</td>
                <td>
                   object
                </td> 
            </tr>
            <tr>
                <td>Contains</td>
                <td>params: {
                   Name: userId,
                   Type: string
                  }</td>
            </tr>
        </tbody>
    </table>

   * Name: res

     Type: Object

     **Description:** Response object returned to the api which contains data regarding trip requests and trips corresponding to a user.

5. **Response:**

   * Returns object with tree properties:
     **success**\(bool\), message and **data .**
   * **Data** field is an object containing the details of trip request along with rider and driver details.

   * **Http Code**: 200

     **Name**: returnObj

     **Type**: Object

#### Revenue Details

1. **API Path:** api/admin/trip/charts
2. **Method:** GET
3. **Description:**

   * This route is use to fetch data related to the revenue earned in each month. This route fetches data from past 12 months. Its functionality is defined inside ./controllers/admin-trip.js.

   * This route fetch details of revenue earned per month.

   * Fetches data not more than 12 months.

   * Functionality:
     `./controllers/admin-trip.js`

4. **Parameters:**

   <table class="table table-bordered">
        <thead>
            <tr>
                <th>Name</th>
                <th>req</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>type</td>
                <td>
                   object
                </td> 
            </tr>
        </tbody>
    </table>

   * Name: res

     Type: Object

     **Description:** Response object returned to the api which contains revenue details per month.

5. **Response:**

   * Returns object with tree properties:
     **success**\(bool\), **message **and **data**
   * **Data**  field is an object containing revenue details per month.

   * **Http Code**: 200

     **Name**: returnObj

     **Type **: Array of object



