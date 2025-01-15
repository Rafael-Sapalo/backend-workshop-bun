# Backend Workshop with Hono and Bun

## Beginner Level

### Workshop Goals
- Understand the basics of backend development.
- Set up a simple Hono application using Bun.
- Learn basic routing and request handling.

### Steps

1. **Introduction to Hono and Bun**
   - Research what Hono and Bun are and understand their purposes.
   - Write a brief note on why lightweight frameworks like Hono are advantageous for small to medium-scale projects.
   - Compare the speed and performance benefits of Bun against Node.js in a simple table format.

2. **Environment Setup**
   - Install Bun: [https://bun.sh](https://bun.sh)
     ```bash
     curl -fsSL https://bun.sh/install | bash
     ```
   - Create a new project directory:
     ```bash
     mkdir hono-beginner && cd hono-beginner
     bun init
     ```
   - Verify the installation of Bun by running:
     ```bash
     bun --version
     ```

3. **Create a Basic Server**
   - Install Hono:
     ```bash
     bun add hono
     ```
   - Create a file named `index.ts` and set up a basic Hono server that listens on port 3000 and responds with "Hello, World!".
   - Explore the Hono documentation and add comments in your code to explain what each part does.

4. **Run the Server**
   - Use Bun to run the server:
     ```bash
     bun run index.ts
     ```
   - Open your browser and verify the server is running at [http://localhost:3000](http://localhost:3000).
   - Add console logs to confirm the server is receiving requests.

5. **Add More Routes**
   - Add routes for `/about` and `/contact` that return respective responses.
   - Explore how to return JSON responses for these routes instead of plain text.

6. **Workshop Challenges**
   - Add a `/services` route.
   - Create a dynamic route, e.g., `/user/:id`, that extracts and returns the user ID from the URL.
   - Enhance the `/user/:id` route to return a JSON response with a mock user object.

---