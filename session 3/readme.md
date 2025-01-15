## Advanced Level

### Workshop Goals
- Build a complete API with Hono and Bun.
- Implement authentication.
- Integrate with a database (PostgreSQL using Drizzle ORM).
- Connect the backend to a frontend.
- Dockerize the application for deployment.

### Steps

1. **Database Integration**
   - Install PostgreSQL and Drizzle ORM:
     ```bash
     bun add drizzle-orm pg
     ```
   - Configure Drizzle ORM with a PostgreSQL connection:
    Follow the instructions in the [Drizzle ORM documentation](https://orm.drizzle.team/docs/get-started/postgresql-new).
   - Research and define the schema for your database tables (e.g., `users` and `todos`) using PostgreSQL and Drizzle ORM.
   - Write migration scripts to create and modify database schemas as required.
   - Verify the database connection by querying data from the tables.

2. **Authentication Middleware**
   - Implement JWT-based authentication middleware.
   - Create a login route that generates and returns a JWT upon successful login.
   - Protect certain routes using the middleware to verify the JWT.

3. **CRUD API**
   - Implement CRUD operations for `users` and `todos`:
     - Users:
       - Create a new user.
       - List all users.
       - Update a user by ID.
       - Delete a user by ID.
     - Todos:
       - Create a new todo item.
       - List all todos for a specific user.
       - Update a todo's status.
       - Delete a todo by ID.

4. **Frontend Connection**
   - Create a simple frontend using HTML, CSS, and JavaScript.
   - Use `fetch` or `axios` to make API calls to your backend.
   - Build forms for user login, creating todos, and updating todo statuses.
   - Display user and todo data fetched from the backend.

5. **Dockerization**
   - Create a `Dockerfile` for the application:
     ```dockerfile
     # Use Bun as the base image
     FROM oven/bun

     # Set the working directory
     WORKDIR /app

     # Copy package files and install dependencies
     COPY . .
     RUN bun install

     # Expose the application port
     EXPOSE 3000

     # Start the application
     CMD ["bun", "run", "index.ts"]
     ```
   - Create a `docker-compose.yml` file:
     ```yaml
     version: '3.8'
     services:
       app:
         build: .
         ports:
           - "3000:3000"
         environment:
           - API_KEY=your_api_key_here
           - DATABASE_URL=postgres://your_user:your_password@localhost:5432/workshop
       db:
         image: postgres
         environment:
           POSTGRES_USER: your_user
           POSTGRES_PASSWORD: your_password
           POSTGRES_DB: workshop
         ports:
           - "5432:5432"
     ```
   - Build and run the Docker container:
     ```bash
     docker-compose up --build
     ```

6. **Push Docker Image to a Registry**
   - Tag the Docker image for a container registry (e.g., Docker Hub):
     ```bash
     docker tag hono-app:latest your-dockerhub-username/hono-app:latest
     ```
   - Log in to the registry:
     ```bash
     docker login
     ```
   - Push the image:
     ```bash
     docker push your-dockerhub-username/hono-app:latest
     ```

7. **Testing and Debugging**
   - Write integration tests for the API endpoints.
   - Use tools like Postman or Insomnia to manually test API endpoints.
   - Set up logging to capture detailed error messages for debugging.

8. **Workshop Challenges**
   - Add role-based authentication (e.g., admin vs regular user).
   - Create a `/metrics` route that tracks API usage stats (e.g., total requests per route).
   - Enhance the frontend to display usage stats from the `/metrics` route.

9. **Database Optimization**
   - Use indexes to optimize database queries for large datasets.
   - Write database migration scripts to handle schema changes over time.

10. **Bonus: Advanced Frontend Integration**
    - Use a frontend framework like React or Vue.js to create a more dynamic interface.
    - Implement state management to handle user authentication and data fetching.

---

### Final Objective: Build a Full-Featured TODO App Backend

At the end of the workshop, participants will create a fully functional backend for a TODO application with the following features:
- User authentication and role-based access control.
- CRUD operations for managing TODO items (create, read, update, delete).
- PostgreSQL database integration with Drizzle ORM for storing users and TODO items.
- A `/metrics` route for tracking usage statistics.
- Dockerized application, ready to be pushed to a container registry.
- Frontend integration using RESTful APIs to manage TODOs.

Participants are encouraged to use all learned concepts, including middleware, authentication, database optimization, and testing, to complete this project.
