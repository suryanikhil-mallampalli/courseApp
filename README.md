<!DOCTYPE html>
<html lang="en">

<body>
    <h1>Course Management App</h1>

  <p>This is the README file for the Course Management App project. This project is a basic web application built using Node.js, Express.js, and MongoDB for managing courses and users. It includes authentication for both administrators and users, allowing administrators to create and update courses, while users can sign up, log in, and purchase courses. Below, you'll find information on how to set up and use the application.</p>

  <h2>Prerequisites</h2>

  <p>Before you begin, ensure you have met the following requirements:</p>

  <ul>
        <li>Node.js installed on your machine.</li>
        <li>MongoDB database (You can use MongoDB Atlas or install it locally).</li>
    </ul>

  <h2>Getting Started</h2>

  <p>Follow these steps to set up and run the application:</p>

  <ol>
        <li>Clone the repository to your local machine:</li>
        <pre><code>git clone &lt;https://github.com/suryanikhil-mallampalli/courseApp&gt;</code></pre>

  <li>Install the project dependencies:</li>
        <pre><code>cd &lt;project_directory&gt;</code></pre>
        <pre><code>npm install</code></pre>

  <li>Configure Environment Variables:</li>
        <ul>
            <li>Create a <code>.env</code> file in the project root.</li>
            <li>Define the following environment variable in the <code>.env</code> file:</li>
        </ul>

 <pre><code>
SECRET=your_secret_key
MONGODB_URI=your_mongodb_connection_uri
        </code></pre>

  <p>Replace <code>your_secret_key</code> with a strong secret for JWT token generation, and <code>your_mongodb_connection_uri</code> with the MongoDB connection URI.</p>

  <li>Start the application:</li>
        <pre><code>npm start</code></pre>
        <p>The application will run on port 3000 by default. You can access it in your web browser at <a href="http://localhost:3000">http://localhost:3000</a>.</p>
    </ol>

<h2>API Endpoints</h2>

<p><strong>Admin Routes</strong></p>
    <ul>
        <li><code>POST /admin/signup</code>: Sign up as an admin.</li>
        <li><code>POST /admin/login</code>: Log in as an admin.</li>
        <li><code>POST /admin/courses</code>: Create a new course (requires authentication).</li>
        <li><code>PUT /admin/courses/:courseId</code>: Update an existing course (requires authentication).</li>
        <li><code>GET /admin/courses</code>: Get a list of all courses (requires authentication).</li>
    </ul>

   <p><strong>User Routes</strong></p>
    <ul>
        <li><code>POST /users/signup</code>: Sign up as a user.</li>
        <li><code>POST /users/login</code>: Log in as a user.</li>
        <li><code>GET /users/courses</code>: Get a list of all published courses (requires authentication).</li>
        <li><code>POST /users/courses/:courseId</code>: Purchase a course (requires authentication).</li>
        <li><code>GET /users/purchasedCourses</code>: Get a list of purchased courses (requires authentication).</li>
    </ul>

  <h2>Authentication</h2>

  <ul>
        <li>Admins and users need to sign up and log in to access their respective routes.</li>
        <li>JWT (JSON Web Tokens) are used for authentication and authorization.</li>
        <li>Admins have access to course management routes, while users can purchase and view courses.</li>
    </ul>

  <h2>Database</h2>

  <p>The application uses MongoDB as its database. Make sure you have configured the <code>MONGODB_URI</code> environment variable with the appropriate MongoDB connection string.</p>

  <h2>Security</h2>

  <ul>
        <li>Ensure that you keep your <code>SECRET</code> environment variable secure. It's crucial for JWT token generation.</li>
        <li>Always sanitize and validate user input to prevent potential security vulnerabilities.</li>
        <li>Consider implementing HTTPS for better security when deploying the application in production.</li>
    </ul>

  <h2>Deployment</h2>

  <p>This README covers setting up the project for development. For production deployment, consider using a platform like Heroku, AWS, or DigitalOcean, and follow best practices for securing your application and database.</p>

</html>
