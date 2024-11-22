# Using the DELETE Method in Postman
# 1. Open Postman
     Launch the Postman application.

# 2. Add a New Request to the Collection
     Click on your collection.
     Click the Add Request button or the "+" icon next to Requests.
     Name your request (e.g., Delete User).
     Optionally, add a description for the request.
# 3. Select the DELETE Method
     In the request window, select DELETE from the dropdown list next to the request URL input field.

# 4. Enter the Request URL
     Enter the URL for the API endpoint where the DELETE operation will be performed. For example:
     https://reqres.in/api/users/2

# 5. Test the Response
     Go to the Scripts tab: Click on the Post-response
     Add the following code snippet to validate the response: Example:
     pm.test("Status code is 204", function () {
    pm.response.to.have.status(204);
     });
# 6. Save the Request
     Click the Save button to save your request in the collection.
# 7. Send the Request
     Click the Send button to execute the DELETE request.
     Review the response in the Response section below the request window.

    
# curl Command to Delete User Data

# 1. curl --location --request DELETE 'https://reqres.in/api/users/2' \
--header 'Content-Type: application/json'
Explanation:
curl: Command-line tool used for making HTTP requests.

# 2. --location: 
     Instructs curl to follow any redirects if the server responds with a redirect status.

# 3. --request DELETE: 
     Specifies that this is a DELETE request.

# 4.'https://reqres.in/api/users/2': 
     URL of the API endpoint. 
     The /2 at the end specifies that we are deleting the user with ID 2.

# 5. --header 'Content-Type: application/json': 
     Sets the header to indicate the content type, though DELETE requests often don't have a body.