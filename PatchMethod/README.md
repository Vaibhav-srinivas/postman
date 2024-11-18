# postman
# Project Name - Practice Project

This Postman collection provides a set of requests for interacting with the Project Name USER, which allows you to GET user details, POST new user details, PUT method for updating a user’s details, PATCH method to make partial updates to user details, DELETE method is used to delete an existing user details from a server and access core features.

## Prerequisites
- Postman [Download here](https://www.postman.com/downloads/)

# Using the PATCH Method in Postman
# 1. Open Postman
    Launch the Postman application.

# 2. Add a New Request to the Collection
     Click on your collection (e.g., Practice Project).
     Click the Add Request button or the "+" icon next to Requests.
     Name your request (e.g., Partial Update User).
     Optionally, add a description for the request.

# 3. Select the PATCH Method
     In the request window, select PATCH from the dropdown list next to the request URL input field.

# 4. Enter the Request URL
     Enter the URL for the API endpoint you want to partially update. For example:
     https://reqres.in/api/users/2

# 5. Enter the Required Details in the Body Tab
     Go to the Body tab.
     Select raw and choose JSON from the dropdown.
# 6. Enter Data in JSON Format
     Add the JSON object you want to update, such as:
    {
     "job": "Lead Developer"
    }

# 7. Enter the Required Details in the Tests Tab
     Go to the Scripts tab: Click on the Post-response
     Add the following code snippet to validate the response:
# 8. Enter Data in JSON Format
     pm.test("Status code is 200", function () {
     pm.response.to.have.status(200);
     });
# 9. Save the Request
     Click the Save button to save your request within the collection.
# 10. Send the Request
     Click the Send button to execute the PATCH request.
    Review the response in the Response section below the request window.
By following these steps, you can successfully create a structured PATCH request within a Postman collection.

# curl Command to Partially Update User Data with PATCH

# 1. curl --location --request PATCH 'https://reqres.in/api/users/2' \
     --header 'Content-Type: application/json' \
    --data '{
    "job": "Lead Developer"
    }'
Explanation:
curl: Command-line tool used for making HTTP requests.

# 2. --location:

     Instructs curl to follow any redirects if the server responds with a redirect status (e.g., 301 or 302).
    --request PATCH:

Specifies that this is a PATCH request.
# 3. 'https://reqres.in/api/users/2':

    This is the URL or endpoint of the API where the PATCH request is being sent.
    The /2 at the end specifies that we are updating the user with ID 2.
# 4 --header 'Content-Type: application/json':

    Sets the Content-Type header to application/json, indicating the format of the request body.
# 5. --data:

Specifies the JSON data to be sent in the body of the request.

{
  "job": "Lead Developer"
}
