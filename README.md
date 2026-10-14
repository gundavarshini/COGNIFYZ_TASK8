# ServerOps – Advanced Server-Side Functionality

### Cognifyz Technologies | Full Stack Development Internship

**Level 4 – Task 8: Advanced Server-Side Functionality**

## Internship Completion Announcement

I am delighted to share that I have **successfully completed my Full Stack Development Internship at Cognifyz Technologies**.

Throughout this internship, I gained valuable practical experience in full-stack development, backend engineering, REST API development, middleware implementation, server-side caching, and asynchronous background job processing.

As part of **Level 4 – Task 8: Advanced Server-Side Functionality**, I developed **ServerOps**, a web application that demonstrates advanced backend concepts using Node.js, Express.js, Redis, and BullMQ.

This experience strengthened my technical knowledge, problem-solving abilities, and understanding of building responsive, efficient, and maintainable web applications.

I am grateful for this learning opportunity and look forward to applying these skills to real-world projects while continuing to grow as a Full Stack Developer.

## Project Overview

**ServerOps** is a web-based application developed to demonstrate advanced server-side functionality through an interactive dashboard.

The application integrates request-processing middleware, Redis-based caching, and BullMQ-powered background job processing. It allows users to explore backend operations, retrieve cached data, submit asynchronous tasks, and monitor task progress through a clean and responsive interface.

The primary goal of this project is to demonstrate how modern backend technologies can improve application performance, maintainability, and task-processing efficiency.

## Internship Details


| Detail            | Description                                               |
| ----------------- | --------------------------------------------------------- |
| Organization      | Cognifyz Technologies                                     |
| Internship        | Full Stack Development Internship                         |
| Internship Status | Successfully Completed                                    |
| Level             | Level 4 – Expert                                          |
| Task Number       | Task 8                                                    |
| Task Title        | Advanced Server-Side Functionality                        |
| Project Name      | ServerOps                                                 |
| Technologies Used | Node.js, Express.js, Redis, BullMQ, HTML, CSS, JavaScript |


## Project Objectives

- Implement middleware for request processing, request identification, and HTTP logging.
  
- Integrate Redis to improve performance through server-side caching.
  
- Implement asynchronous background jobs using BullMQ.
  
- Separate background processing from the main Express server.
  
- Track background task status using task identifiers.
  
- Build an interactive dashboard to demonstrate backend functionality.
  
- Handle errors and manage application configuration using environment variables.

## Key Features

### 1. Request Processing Middleware

- Generates unique request IDs for tracking incoming requests.
  
- Logs HTTP request activity for debugging and monitoring.
  
- Uses centralized error-handling middleware.
  
- Organizes request processing through reusable Express.js middleware.

### 2. Redis-Based Server-Side Caching

- Stores frequently requested data in Redis.
  
- Demonstrates cache hits and cache misses.
  
- Supports cache invalidation.
  
- Uses a configurable time-to-live (TTL) value.
  
- Reduces repeated data processing when cached results are available.

### 3. Asynchronous Background Job Processing

- Adds tasks to a BullMQ queue.
  
- Processes queued jobs using a separate worker process.
  
- Allows task status to be checked using a task ID.
  
- Separates long-running work from normal HTTP request handling.
  
- Provides a foundation for scalable asynchronous processing.

### 4. Interactive Dashboard

- Displays application and Redis connection status.
  
- Provides controls to fetch data and clear the cache.
  
- Includes a form for submitting background jobs.
  
- Displays API responses for easier testing.
  
- Uses a clean and responsive interface.

## Technology Stack

## Technology Stack

| Technology | Purpose                                           |
| ---------- | ------------------------------------------------- |
| HTML5      | Structures the dashboard                          |
| CSS3       | Provides styling and responsive layouts           |
| JavaScript | Handles frontend interactions and API requests    |
| Node.js    | Provides the server-side JavaScript runtime       |
| Express.js | Implements routes, middleware, and HTTP APIs      |
| Redis      | Provides in-memory data storage and caching       |
| BullMQ     | Manages background job queues                     |
| ioredis    | Provides Redis connectivity for Node.js           |
| dotenv     | Loads environment variables                       |
| Nodemon    | Restarts the development server when files change |
| Git        | Tracks source code changes                        |
| GitHub     | Hosts and manages the project repository          |


## Project Structure

Level4_Task8/
├── config/
│   └── redis.js
├── controllers/
│   └── apiController.js
├── middleware/
│   ├── requestId.js
│   ├── requestLogger.js
│   └── errorHandler.js
├── queues/
│   └── taskQueue.js
├── workers/
│   └── taskWorker.js
├── routes/
│   ├── taskRoutes.js
│   └── dataRoutes.js
├── services/
│   └── cacheService.js
├── public/
│   ├── index.html
│   ├── css/
│   │   └── style.css
│   └── js/
│       └── app.js
├── screenshots/
├── .env
├── .env.example
├── .gitignore
├── package.json
├── package-lock.json
├── server.js
└── README.md


*Note: Keep this tree consistent with your actual project. Remove any entries that do not exist and add any folders or files you have created.*

## Prerequisites

Before running the application, ensure you have installed:

- Node.js and npm
  
- Visual Studio Code or another code editor
  
- Redis server or Docker Desktop configured to run Redis
  
- Git (optional, for repository management)

## Installation and Setup

### Step 1: Clone the Repository


git clone <github.com/gundavarshini>

cd Level4_Task8

### Step 2: Install Dependencies


npm install

### Step 3: Configure Environment Variables

Create a `.env` file in the project root directory:


PORT=5000

REDIS_HOST=127.0.0.1

REDIS_PORT=6379

CACHE_TTL=60

NODE_ENV=development


Ensure the Redis host and port match your Redis configuration.

### Step 4: Start Redis

Start your Redis server before launching the application.

To verify that Redis is responding, run:

redis-cli ping


Expected response:

PONG

### Step 5: Start the Application Server

Open a terminal in the project directory and execute:

npm run dev

### Step 6: Start the Background Worker

Open a second terminal in the same project directory and execute:


npm run worker

Keep both terminals running. The Express server handles web requests, while the worker processes background jobs.

### Step 7: Open the Application

Open your browser and navigate to:

**Application Dashboard:** `http://localhost:5000`

**Health Check:** `http://localhost:5000/api/health`

## API Endpoints


| HTTP Method | Endpoint          | Description                                   |
| ----------- | ----------------- | --------------------------------------------- |
| GET         | `/api/health`     | Checks application server health              |
| GET         | `/api/data`       | Retrieves data and demonstrates Redis caching |
| DELETE      | `/api/data/cache` | Clears cached data                            |
| POST        | `/api/tasks`      | Submits a background job                      |
| GET         | `/api/tasks/:id`  | Retrieves the status of a background job      |

*These endpoints reflect the intended API design. Verify each endpoint against the implemented routes before publishing this README.*

## Background Job Examples

The background processing feature can be demonstrated using the following tasks:

| Task Name                | Description                                                |
| ------------------------ | ---------------------------------------------------------- |
| Generate Monthly Report  | Summarizes application activity and performance statistics |
| Send Email Notifications | Processes pending email notification jobs                  |
| Generate Sales Analytics | Calculates totals and prepares analytical summaries        |
| Export User Data         | Prepares application records for data export               |
| Clean Temporary Files    | Removes expired temporary data                             |
| Generate Invoice         | Creates an invoice for a completed transaction             |
These are illustrative examples; the worker processes only the jobs supported by your implemented job logic.

## Testing and Verification

### Middleware Testing

1. Open the dashboard.
  
2. Refresh the page or make multiple API requests.
  
3. Check the server terminal for request logs and request IDs.
  
4. Verify that errors are handled by the configured error middleware.

### Redis Caching Testing

1. Click **Fetch data** for the first request.
2. Click **Fetch data** again.
3. Verify that the response indicates a cache hit when cached data is available.
4. Click **Clear cache** and fetch the data again.

### Background Job Testing

1. Enter a task name and description in the dashboard.
   
2. Click **Submit background task**.
   
3. Check the response for a task ID.
   
4. Review the worker terminal to verify job processing.
   
5. Check the task status using the task ID.

## Screenshots

The following screenshots can demonstrate the application's functionality. Save your actual screenshots in the `screenshots/` folder and use the matching filenames.

### 1. Application Dashboard

<img width="1478" height="509" alt="image" src="https://github.com/user-attachments/assets/201256d6-09bc-42c4-8b7d-9db5526d0062" />


### 2. System overview 

<img width="1259" height="315" alt="image" src="https://github.com/user-attachments/assets/ff8b27cb-5afe-46c0-a24c-a1a0e07dc357" />


### 3. Redis Caching

<img width="559" height="658" alt="image" src="https://github.com/user-attachments/assets/8bfab3f9-67fa-482e-bbac-8726a11bceb0" />


### 4. Background Job Processor

<img width="537" height="739" alt="image" src="https://github.com/user-attachments/assets/8eff6052-2f77-4191-a865-08b06f60f2a9" />


### 5. Middleware and Server Logs


<img width="1229" height="419" alt="image" src="https://github.com/user-attachments/assets/1cba1c97-ac1d-451f-bcf1-8cbde66b0b67" />


*Replace these image paths with your actual screenshot files. GitHub will not display an image if the referenced file is missing.*

## Learning Outcomes

Through this project, I gained practical experience in:

- Developing backend applications using Node.js and Express.js.
  
- Implementing request-processing and error-handling middleware.
  
- Integrating Redis for server-side caching.
  
- Managing asynchronous tasks using BullMQ.
  
- Running and monitoring a separate background worker.
  
- Designing and testing REST API endpoints.
  
- Configuring environment variables and development scripts.
  
- Organizing a web application using modular project architecture.

## Future Enhancements

- Add authentication and role-based access control.
  
- Introduce retry policies and failed-job monitoring.
  
- Implement scheduled and recurring jobs.
  
- Add detailed queue metrics and cache monitoring.
  
- Integrate automated API tests.
  
- Implement production-oriented logging and monitoring.

## Security Considerations

- Exclude `.env` from version control.
  
- Never publish passwords, API keys, or other secrets.
  
- Use `.env.example` to document required configuration variables with sample values only.
  
- Validate incoming requests and return appropriate error responses.
  
- Restrict access to sensitive administrative operations in future versions.

## Conclusion

ServerOps demonstrates essential advanced server-side development concepts, including middleware, Redis caching, and asynchronous background job processing using BullMQ.

Developing this application provided practical exposure to backend architecture, caching strategies, queue-based processing, and API development.

**Successfully completed as part of the Cognifyz Technologies Full Stack Development Internship – Level 4, Task 8: Advanced Server-Side Functionality.**


### Connect

Thank you for visiting my project! I welcome feedback, suggestions, and opportunities to learn and contribute to real-world software development projects.
