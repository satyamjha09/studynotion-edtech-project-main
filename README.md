StudyNotion Edtech Project
The StudyNotion Edtech Project is a comprehensive e-learning platform that allows users to learn through structured courses. It offers features for students, instructors, and administrators to manage learning materials, progress tracking, and ratings. Below is an overview of the project:

Project Features
User Management:

User registration and authentication.
Role-based access control (e.g., Admin, Instructor, Student).
Course Management:

Course creation: Instructors can create and manage courses, including descriptions, pricing, and thumbnails.
Content structure: Courses are divided into sections, and each section has multiple subsections (videos, articles, etc.).
Tags: Courses are categorized using tags for better discoverability.
Learning Experience:

Video-based content delivery.
A progress tracking feature for enrolled courses.
A "What You Will Learn" section highlighting course objectives.
Ratings and Reviews:

Students can rate and review courses.
Average ratings displayed on the course page.
Enrollment System:

Students can enroll in courses.
A student enrollment list for instructors.
Search and Recommendation:

Search functionality for courses.
Tag-based recommendations for related content.
Admin Dashboard:

Manage users, courses, and content.
View reports and analytics on course performance.
Database Schema
The project uses a MongoDB database with the following schemas:

User Schema:

Fields: Name, email, password, role (Admin/Instructor/Student), and enrollment details.
Profile Schema:

Fields: Gender, contact number, date of birth, about section.
Course Schema:

Fields: Course name, description, instructor (reference to User), price, thumbnail, tags, student enrollments, and ratings.
Section and Subsection Schemas:

Section: Contains the name of the section and references to subsections.
Subsection: Contains titles, time duration, video URLs, and descriptions.
Course Progress Schema:

Fields: Course ID, completed videos (reference to Subsection).
Rating and Review Schema:

Fields: User (reference to User), rating, review text.
OTP Schema:

Fields: Email, OTP, and timestamp for password recovery or account verification.
Tag Schema:

Fields: Tag name, description, and associated courses.
Technology Stack
Frontend: React.js with Tailwind CSS for styling and interactivity.
Backend: Node.js with Express.js for RESTful APIs.
Database: MongoDB for storing user and course data.
Authentication: JSON Web Tokens (JWT) and bcrypt.js for secure user login and password storage.
Cloud Services:
Cloudinary for managing media files (e.g., thumbnails and videos).
Email services for sending OTPs.
Setup Instructions
Clone the Repository:

bash
Copy code
git clone <repository-url>
cd StudyNotion
Install Dependencies:

bash
Copy code
npm install
Configure Environment Variables: Create a .env file and include:

makefile
Copy code
MONGO_URI=<your_mongo_db_connection_string>
JWT_SECRET=<your_jwt_secret>
CLOUDINARY_CLOUD_NAME=<your_cloudinary_cloud_name>
CLOUDINARY_API_KEY=<your_cloudinary_api_key>
CLOUDINARY_API_SECRET=<your_cloudinary_api_secret>
Run the Application:

Backend: npm start in the root directory.
Frontend: npm start in the client directory.
Use Cases
For Students:

Discover and enroll in courses.
Track learning progress.
Provide ratings and reviews for completed courses.
For Instructors:

Create and manage courses.
View student enrollment and feedback.
For Admins:

Manage users, courses, and reports.
This project combines features of popular edtech platforms like Udemy and Coursera, focusing on a seamless and engaging learning experience for users
