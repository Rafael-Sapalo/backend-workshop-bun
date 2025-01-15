## Intermediate Level

### Workshop Goals
- Implement middleware.
- Work with JSON data and query parameters.
- Use environment variables.

### Steps

1. **Middleware Basics**
   - Create a middleware that logs the HTTP method and URL of every request.

2. **Working with JSON**
   - Add a POST route for user creation. The route should accept a JSON payload and return a success message with the received data.

3. **Query Parameters**
   - Add a `/search` route that accepts a query parameter `q` and returns it in the response.

4. **Environment Variables**
   - Create a `.env` file with a variable `API_KEY`.
   - Use the `dotenv` package to load and display the API key in a `/key` route.

5. **Testing**
   - Write tests for your routes using a testing framework compatible with Bun.
   - Test scenarios:
     - Successful route responses.
     - Error handling for missing or invalid input.

6. **Workshop Challenges**
   - Add middleware to check if a `token` query parameter exists for certain routes.
   - Create a `/calculate` route that accepts two numbers as query parameters and performs addition.
   - Write tests for the `/calculate` route to validate correct addition and error scenarios.

---