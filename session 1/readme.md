# Backend Workshop with Hono and Bun

## Beginner Level

### Workshop Goals
- Understand the basics of backend development.
- Set up a simple Hono application using Bun.
- Learn basic routing and request handling.

### Steps

1. **Introduction to Hono and Bun**
   - Research what Hono and Bun are and understand their purposes.
   - What are the differences between Bun and Node.js?

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

3. **Create a Basic Server**
   - Install Hono.
   - Create a file named `index.ts` and set up a basic Hono server that listens on port 3000 and responds with "Hello, World!".

4. **Run the Server**
   - Use Bun to run the server.
   - Open your browser and verify the server is running.

5. **Add More Routes**
   - Add routes for `/about` and `/contact` that return respective responses.

6. **Workshop Challenges**
   - Add a `/services` route.
   - Create a dynamic route, e.g., `/user/:id`, that extracts and returns the user ID from the URL.

---