# OnlineComplaintManagementSystem
The online complaint registration and management system is designed to streamline the process of submitting, managing and resolving complaints or issues. It aims to provide a centralized platform where users can easily register their complaints, track their progress, and communicate with the responsible agents. The system seeks to enhance the efficiency of complaint handling, ensure timely resolutions, and ultimately improve customer satisfaction by offering a transparent and structured approach to managing complaints.

## Features 
1. User Registration
3. Complaint Submission and categorization
4. Tracking and Notification
5. Security and Confidentiality to protect user information and complaint details
6. Resolution and Feedback to enhance the system and complaint handling

## Architecture

1. Frontend
   - The frontend architecture ensures a clean separation of concerns making application scalable and maintainable. Each user role(student, employee, admin) has its dedicated dashboard with specific functionalities, enhancing the user experience and managing the application's complexity efficiently..
   - The Routing is managed by react-router-dom in Frontend/App.js.
   - The local state management using useState for handling dynamic data like complaints.
   - Each dashboard and functionality is encapsulated in separate components (components based design)
   - The styling utilizes bootstrap/dist/css/bootstrap.min.css for consistent and responsive styling.

2. Backend
   - The backend architecture is built using Node.js and Express.js, with MongoDB as the database. It includes separate routes and controllers for handling complaints from students, employees, and admins. The main features include user authentication, complaint management, and secure data handling.
     
     2.1 Server setup (app.js):
       - Express App initializes the Express application.
       - Middleware includes CORS, JSON parsing, and custom error handling.
       - MongoDB connection: Connects to the MongoDB database using Mongoose.
       - Routes: Set up routes for students, complaints, and employees.
         
     2.2 Database (MongoDB) is used as the database, managed via Mongoose which provides a clear way to define and interact with MongoDB data models. The database schema includes collections for complaints, students and employees. The CRUD Operations performed are defined below:
         - Create: Insert new documents into the 'complaints', 'students' or 'employee' collections using Mongoose models.
         - Read: Queries can be based on fields like 'studentId', 'EmployeeId', or specific complaint IDs.
         - Update: For example, updating the status of a complaint or changing employee/student details.
         - Delete: deleting complaints or removing complaints from a student's or employee's list.
         * The complaints and students: Complaints are associated with students via 'studentId' field. This allows tracking of which student made each complaint.
         * Complaints and Employees: Employees are assigned complaints through 'assignedComplaints' field, linking them to specific complaints.
         * Validation: Mongoose schemas enforce datatypes and required fields, ensuring data integrity.
         * Error handling: Errors during database operations are caught and handled, ensuring that the application can respond efficiently to issues like validation and connection problems.
           
     2.3 Routes and controllers
         - Separate route files for different functionalities, e.g., studentRoutes, complaintRoutes, employeeRoutes. Each route file imports corresponding controllers and defines the endpoints.
         - Controllers handle the logic for each route, interacting with the database and processing the requests.

## Setup Instructions
 - Prerequisites: The software dependencies required are Node.js, Mongoose, CORS, Bcryptjs, and .env configuration file.

 - Installation:
   1. Frontend:
      * npm install dotenv : to install the dotenv package in order to load the required environment variables.
      * npx create-react-app . : in the current frontend directory to install the required dependencies and node modules for the react environment.
      * npm install react-bootstrap axios react-router-dom : to install the required modules used in the application.

   2. Backend:
      * npm install express : to install the express framework.
      * npm install cors mongoose bcrypt : for installing the required middleware(cors), library(mongoose, bcrypt).

- Running the application
  1. Frontend: npm start - to start the react environment.
  2. Backend: node app.js - to start the server at the local port.

## User Interface images


