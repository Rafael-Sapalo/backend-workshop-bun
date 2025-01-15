## Intermediate Level

### Workshop Goals
- Implement middleware.
- Work with JSON data and query parameters.
- Use environment variables effectively.

### Steps

1. **Middleware Basics**
   - Create a middleware function that logs the HTTP method, URL, and timestamp of each request.
   - Modify the middleware to reject requests with a missing or invalid custom header, e.g., `X-Auth-Token`.

2. **Working with JSON**
   - Add a POST route for user creation. The route should:
     - Accept a JSON payload with `name` and `email` fields.
     - Validate the input fields and return appropriate error messages for invalid data.
     - Return a success message along with the received data if validation passes.

3. **Query Parameters**
   - Add a `/search` route that accepts a query parameter `q` and returns it in the response.
   - Modify the `/search` route to simulate a database search and return mock results.

4. **Environment Variables**
   - Create a `.env` file with variables like `API_KEY` and `PORT`.
   - Use the `dotenv` package to load these variables and log them in the server console.
   - Update the server to dynamically use the `PORT` variable from the environment file.

5. **Testing**
   - Write tests for your routes using a testing framework compatible with Bun.
   - Create tests for:
     - Middleware functionality.
     - Successful and error scenarios for the `/search` and POST routes.
   - Use a testing utility to mock request and response objects for unit testing.

6. **Workshop Challenges**
   - Add middleware to check if a `token` query parameter exists for certain routes.
   - Create a `/calculate` route that accepts two numbers as query parameters and performs addition.
   - Write comprehensive tests for the `/calculate` route to handle edge cases like missing or non-numeric parameters.

---