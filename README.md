🎉 Event Management Web Application
A web-based Event Management System developed as a Final Year Project. This application allows users to explore upcoming events, view event details, and register for events online. It also provides an admin panel for authorized administrators to manage events and monitor registrations.
📌 Table of Contents
- About the Project
- Project Objectives
- Features
- Technologies Used
- Project Structure
- System Requirements
- Installation and Setup
- Firebase Configuration
- How to Run the Project
- Admin Access and Security
- Database Structure
- Future Enhancements
- Project Author
- License
📖 About the Project
The Event Management Web Application is designed to simplify event organization and participant registration.

Users can log in, explore available events, view event information, and register for events through a simple web interface. An admin panel allows authorized administrators to create, update, and delete events and manage registrations.

The application uses Firebase services for authentication and database management.
🎯 Project Objectives
- Develop a user-friendly event management platform.
- Provide secure user authentication.
- Display upcoming events and event details.
- Simplify online event registration.
- Provide an admin dashboard for event management.
- Store and manage event and registration information efficiently.
✨ Features
👤 User Module
- User login and authentication.
- View upcoming events.
- Browse events through the home page and calendar.
- View event details.
- Register for events.
- Access event information easily.
🔐 Admin Module
- Admin authentication.
- Admin dashboard.
- Add new events.
- Edit existing events.
- Delete events.
- View participant registrations.
- Manage event information.
🔥 Firebase Integration
- Firebase Authentication.
- Cloud Firestore database.
- Cloud-based data storage.
- Authentication and access control.
🛠️ Technologies Used
Technology	Purpose
HTML5	Website structure
CSS3	User interface and styling
JavaScript	Application functionality
Firebase Authentication	User authentication
Cloud Firestore	Database management
Firebase Hosting	Deployment (if configured)
Git and GitHub	Version control and project hosting


📂 Project Structure
Event-Management-System/
│
├── index.html                 # Login page
├── home.html                  # Home page and event calendar
├── event-details.html         # Event details page
├── register.html              # Event registration page
├── admin.html                 # Admin dashboard
│
├── styles/
│   ├── style.css              # User page styling
│   └── admin.css              # Admin panel styling
│
├── js/
│   ├── script.js              # User page interactions
│   ├── admin.js               # Admin panel functionality
│   └── auth.js                # Authentication logic
│
├── images/
│   ├── background.jpg
│   └── logo.png
│
├── firebase/
│   └── firebase-config.js     # Firebase initialization
│
└── README.md                  # Project documentation
💻 System Requirements
- Operating System: Windows, Linux, or macOS
- Code Editor: Visual Studio Code (recommended)
- Browser: Google Chrome, Microsoft Edge, or Firefox
- Internet connection
- Firebase account
- Git (for version control)
⚙️ Installation and Setup
Step 1: Clone the Repository
Replace the sample URL with your GitHub repository URL.
git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
Step 2: Open the Project Folder
cd Event-Management-System
Open the folder in Visual Studio Code.
Step 3: Configure Firebase
1. Open the Firebase Console.
2. Create a Firebase project.
3. Register a Web App in the project.
4. Enable Email/Password sign-in under Authentication, if used by the application.
5. Create a Cloud Firestore database.
6. Copy the Firebase web app configuration.
7. Add the configuration to firebase/firebase-config.js.
Step 4: Install Live Server
In Visual Studio Code, install the Live Server extension if you do not already have a local development server.
🔥 Firebase Configuration
The following is an example for a project using Firebase's browser ES modules. Use the Firebase SDK version and import style that match your application.

Add your Firebase configuration to firebase/firebase-config.js:
import { initializeApp } from
  "https://www.gstatic.com/firebasejs/10.12.0/firebase-app.js";

import { getAuth } from
  "https://www.gstatic.com/firebasejs/10.12.0/firebase-auth.js";

import { getFirestore } from
  "https://www.gstatic.com/firebasejs/10.12.0/firebase-firestore.js";

const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_PROJECT_ID.firebaseapp.com",
  projectId: "YOUR_PROJECT_ID",
  storageBucket: "YOUR_STORAGE_BUCKET",
  messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
  appId: "YOUR_APP_ID"
};

const app = initializeApp(firebaseConfig);

export const auth = getAuth(app);
export const db = getFirestore(app);
Important: Replace all placeholder values with your own Firebase web app configuration. This example assumes your JavaScript files use compatible ES module imports. Do not upload service account private keys or other server credentials to GitHub.
▶️ How to Run the Project
1. Complete the Firebase setup.
2. Open the project folder in Visual Studio Code.
3. Start Live Server from index.html.
4. The application should open in your browser.
5. Sign in using an account configured for your application.
If your project uses a different local server or build process, follow that setup instead.
🔐 Admin Access and Security
The application includes an admin panel intended only for authorized administrators.

For secure access:
- Authenticate users with Firebase Authentication.
- Assign administrator roles using trusted server-side code or Firebase Admin SDK custom claims.
- Enforce permissions with Firestore Security Rules.
- Protect event creation, editing, deletion, and registration-management operations.
- Validate user input before processing it.
Security note: Hiding the admin page or checking a role only in browser JavaScript does not secure admin data. Access must also be enforced by Firebase Security Rules or a trusted backend.
🗄️ Suggested Firestore Database Structure
The following is a suggested structure. Adjust collection names and fields to match your actual implementation.
users Collection
Field	Description
userId	Firebase Authentication user ID
name	User's name
email	User's email address
role	User role, such as user or admin


events Collection
Field	Description
eventName	Name of the event
description	Event description
eventDate	Event date
eventTime	Event time
venue	Event location
imageUrl	Event image location, if used


registrations Collection
Field	Description
userId	ID of the registered user
eventId	ID of the selected event
registrationDate	Date of registration
status	Registration status, if implemented


Testing
Test the application before deployment:
- Check user login and logout.
- Verify that event details load correctly.
- Test event registration and input validation.
- Check that authorized admins can manage events.
- Confirm that ordinary users cannot perform admin operations.
- Verify Firestore Security Rules using the Firebase Rules testing tools.
   Future Enhancements
- Email confirmation after registration.
- Event cancellation notifications.
- QR-code-based event check-in.
- Event search and filtering.
- Downloadable event tickets.
- Attendance tracking and reports.
- Online payment integration.
Name: Keziahreu
Project Title: Event Management Web Application
Project Type: Final Year Project
Technologies: HTML, CSS, JavaScript, Firebase
GitHub: https://github.com/keziahre

LicenseThis project was developed for academic and educational purposes as part of a Final Year Project.
If you find this project useful, consider giving the repository a star!
