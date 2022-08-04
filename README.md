## Practice

This practice comprises 6 exercises

### Problem Statements

#### Practice 1 - Create Complex JSON

The details of flights from Chicago to New York are provided in the tabular format below:

| from    | to                | departure-date | flight no | airlines | departure-time | arrival-time | stop overs | isDirect | departure-from | arrival-at |
| ------- | ----------------- | -------------- | --------- | -------- | -------------- | ------------ | ---------- | -------- | -------------- | ---------- |
| Chicago | New York          | 22-Jun-2022         | DL551     | Delta    | 06:00:00       | 09:16:00     |            | TRUE     | ORD            | LGA        |
|||| UA2606  | United Airlines   | 19:45:00       | 23:10:00  |          | TRUE           | ORD          | LGA        |
|||| UA1253  | United Airlines   | 12:45:00       | 18:09:00  | 1        | FALSE           | ORD          | LGA        |
|||| AA2371  | American Airlines | 10:30:00       | 13:59:00  |          | TRUE           | ORD          | JFK        |
|||| DL556   | Delta Airlines    | 08:30:00       | 11:48:00  |          | TRUE           | ORD          | LGA        |
|||| AA2992  | American Airlines | 13:48:00       | 16:48:00  |          | TRUE           | ORD          | EWR        |

**Note:**
- The value for fields `from`, `to`, and `departure-date` are same for all flight options and hence need not be repeated.
- The list of flight options should be represented as a collection within the JSON along with these fields.
- Each item in the collection is an object that represents a flight option with details such as `flight no`, `airlines`, `departure-time`, `arrival-time`, `stop overs`, `is Direct`, `departure from` and `arrival at`.

Create JSON with the details provided and save it in `p1-submission.json` file. 

The file is located inside the folder `p1-json-with-objects`.

#### Practice 2 - Install json-server

Refer to the instructions given in `p2-installation-guide.md` file for downloading and installing `json-server`.

The file is located in the folder named `p2-install-json-server`.

Start the `json-server` from the same folder, to read data from `db.json` file.

Note down the installation and start up details and record it in file `p2-submission.md` located in the same folder.

#### Practice 3 - Install Postman App

Download source for desktop version of Postman app from [here](https://www.postman.com/downloads/)

Use the downloaded source code to install Postman App.

Refer to the instructions given in `p3-installation-guide.md` file for downloading and installing Postman app.

The file is located in the folder named `p3-install-postman`.

To make requests run the json-server with db.json file getting created in this folder.

Note down the request and response details in `p3-submission.md` file located in the same folder.

#### Practice 4 - Make HTTP Request to Fetch Movies

For the `json-server` serving movies data, list down the HTTP request URLs for fetching movies based on the criteria specified.

Use Postman desktop app to test the requests

##### Task – 1 

From the command terminal, switch to the root folder which contains the file `movies.json`.

To start `json-server` and run the movies API, run the command 
```
json-server movies.json
```

The following output is expected on the terminal once the `json-server` has started and the movies API is running
```
  \{^_^}/ hi!

  Loading movies.json
  Done

  Resources
  http://localhost:3000/movies

  Home
  http://localhost:3000

  Type s + enter at any time to create a snapshot of the database
```
##### Task – 2

An API specification (spec) is a document that provides the details of APIs published by the server.

The client application uses this document to infer what all requests can be made to the server and what responses in return should be expected.

The `movies-api-spec.json` contains specification for movies API in JSON format. 

Read the specification and write HTTP requests to 
  - fetch all movie data
  - fetch movie data by id `502`
  - fetch movie by movie title `365 Days`.
  - fetch movies by genre `Action`
  - fetch movies by genre `Action` released in the year `2022`
  - fetch movie by invalid id `600`

Test the request URLs using Postman.

Note down the status code for each response received in the in` p4-submission.csv` file.

The file is located in the folder `p4-make-http-fetch-request`.

Ensure the details match with the requests and responses mentioned in the specification document. 

#### Practice 5 - Make HTTP Request to Add a Movie

For the `json-server` serving movies data, write down the HTTP request URL for adding a new movie to the list of movies.

Refer to the API specification document to understand the request and response details for saving movies data.

Write HTTP Request URLs in `p5-submission.csv` file to add movies with details given in table below:

| ID  | Movie-name          | Year of Release | Genre  | Director      | Actor-1     | Actor-2        | Actor-3        | Rating   | On OTT |
| --- | ------------------- | ---- | --------- | --------------- | --------------- | -------------- | --------------- | -------- | -- |
| 514 | Father of the Bride | 2021 | Adventure | Gary Alazraki   | Actor name: Andy Garcia Screen name: Billy Herrera | Actor name: Gloria Estefan Screen name: Ingrid Herrera | Actor name: Adria Arjona Screen name:  Sofia Herrera | 5.9 / 10 | No |
| 503 | Spiderhead          | 2022 | Action    | Joseph Kosinski | Actor name: Chris Hemsworth Screen name: Abnesti | Actor name: Miles Teller Screen name: Jeff | Actor name: Jurnee Smollett Screen name: Lizzy| 5.4 / 10 | No |

Test the URLs using Postman.

Note down the status code for each response received in the in `p5-submission.csv` file.

The file is located in the folder `p5-make-http-save-request`.

#### Practice 6 - Make HTTP Request to Update Movie

For the json-server serving movies data, write down the HTTP request URL for updating an existing movie with the details provided.

Refer to the API specification document to understand the request and response details for updating movies data.

Write HTTP Request URLs in `p6-submission.csv` file to update movie with details given in table below:

| ID  | Movie-name          | Year of Release | Genre  | Director      | Actor-1     | Actor-2        | Actor-3        | Rating   | On OTT |
| --- | ------------------- | --------------- | ------ | ------------- | ----------- | -------------- | -------------- | -------- | ------ |
| 504 | Father of the Bride | 2022            | Comedy | Gary Alazraki | Actor name: Andy Garcia Screen name:  Billy Herrera   | Actor name: Gloria Estefan  Screen name:  Ingrid Herrera | Actor name: Adria Arjona Screen name:  Sofia Herrera| 5.9 / 10 | Yes    |
| 500 | Top Gun             | 1986            | Action | Tony Scott    | Actor name:  Tom Cruise Screen name: Maverick   | Actor name: Tim Robbins Screen name:  Merlin | Actor name: Kelly McGillis Screen name:  Charlie | 6.9 / 10 | Yes    |

Test the URLs using Postman.

Note down the status code for each response received in the in `p6-submission.csv` file.

The file is located in the folder `p6-make-http-update-request`.

#### Practice 7 - Make HTTP Request to Delete Movie

For the `json-server` serving movies data, write down the HTTP request URL for deleting an existing movie.

Refer to the API specification document to understand the request and response details for saving movies data.

Write HTTP Request URLs in `p7-submission.csv` file to delete movie with ids 501 and 550.

Test the URLs using Postman.

Note down the status code for each response received in the in `p7-submission.csv` file. 

The file is located in the folder `p7-make-http-delete-request`.

