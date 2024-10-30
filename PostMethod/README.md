# postman
# Project Name - Practice Project

This Postman collection provides a set of requests for interacting with the Project Name USER, which allows you to GET user details, POST new user details, PUT method for updating a user’s details, PATCH method to make partial updates to user details, DELETE method is used to delete an existing user details from a server and access core features.

## Prerequisites
- Postman [Download here](https://www.postman.com/downloads/)

# Using the POST Method in Postman
 # 1. Open Postman
      Launch the Postman application.

 # 2. Add a New Request to the Collection
      Click on your newly created collection.
      Click the Add Request button or the "+" icon next to Requests.
      Name your request ( Create user).
      Optionally, add a description for the request.

 # 3. Select the POST Method
      In the request window, select POST from the dropdown list next to the request URL input field.

 # 4. Enter the Request URL
      Enter the URL for the API endpoint you want to retrieve data from. For example:
      https://reqres.in/api/users

 # 5. Enter the required details in the Body tab
      Go to the Body Tab: Select raw and choose JSON from the dropdown.
      
 # 6. Enter Data in JSON Format
      Add the JSON object you want to send, such as:
      {
    "name": "Vaibhav",
    "job": "Software Engineer"
      }

 # 7. Enter the required details in the Scripts tab
      Go to Scripts Tab: Click on Post-response 

 # 8. Enter Data in JSON Format
      pm.test("Status code is 201", function () {
      pm.response.to.have.status(201);
      }); 

 # 9. Save the Request
      Click the Save button to save your request within the collection.

 # 10. Send the Request
      Once saved, click the Send button to execute the POST request.
      Review the response in the Response section below the request window.

By following these steps, we can effectively create a structured POST request within a Postman collection.
# curl Command to POST User Data
  curl --location 'https://reqres.in/api/users' \
  --header 'Content-Type: application/json' \
  --data {
      "name": "Vaibhav",
      "job": "Software Engineer"
  }

 # 1. curl: The command-line tool curl is used for making HTTP requests. Here, it’s being used to send a request to the ReqRes API.

 # 2. --location:
      This flag instructs curl to follow any redirects if the server responds with a redirect status (e.g., 301 or 302).

 # 3. 'https://reqres.in/api/users':
      This is the URL or endpoint of the API where the request is being sent.
      In this case, the endpoint accepts POST requests to create a new user.

 # 4. --header 'Content-Type: application/json':
      This sets the Content-Type header to application/json, specifying that the request body is formatted as JSON.

 # 5.  --data '{ "name": "Vaibhav", "job": "Software Engineer" }':
      The --data option specifies the data to be sent in the body of the request.
      Here,
      "name": "Vaibhav": Specifies the name of the user.
      "job": "Software Engineer": Specifies the user’s job title.