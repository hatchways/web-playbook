# General

## What is the difference between GET and POST?

- **GET**: The GET request is the most common method for retrieving data from a server. You should not modify any resources in the server code for a GET request. In addition, you cannot send a request body when making a GET request.
- **POST**: A POST request is the second most common method - it is used to send data to an API to create or modify a resource. You send a response body in a POST request. A POST request is [non-idempotent](https://www.infoq.com/news/2013/04/idempotent/).
