# Task Management Application

A task management application that allows users to create, read, update, and delete tasks. The application uses Firebase for backend services including authentication and Firestore for database storage.

## Features

- User Authentication (Sign Up, Login, Logout)
- Create, Read, Update, Delete (CRUD) Tasks
- Real-time updates for tasks
- Responsive user interface

## Technologies Used

- Frontend: HTML, CSS, JavaScript (React)
- Backend: Firebase Authentication, Firebase Firestore
- Deployment: Firebase Hosting

## Getting Started

### Prerequisites

- Node.js and npm installed on your local machine.
- Firebase account and project setup.

### Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/yourusername/task-manager-app.git
    ```

2. Navigate to the project directory:

    ```bash
    cd task-manager-app
    ```

3. Install the dependencies:

    ```bash
    npm install
    ```

4. Create a Firebase project and set up Firebase Authentication and Firestore Database. Follow the [Firebase setup guide](https://firebase.google.com/docs/web/setup).

5. Create a `firebase.js` file in the `src` directory and configure it with your Firebase project's settings:

    ```javascript
    import { initializeApp } from "firebase/app";
    import { getAuth } from "firebase/auth";
    import { getFirestore } from "firebase/firestore";

    const firebaseConfig =  {
  apiKey: "AIzaSyA-EXAMPLE-API-KEY-1234567890",
  authDomain: "your-project-id.firebaseapp.com",
  projectId: "your-project-id",
  storageBucket: "your-project-id.appspot.com",
  messagingSenderId: "1234567890",
  appId: "1:1234567890:web:abcdefghijklmn"
};

    const app = initializeApp(firebaseConfig);
    const auth = getAuth(app);
    const db = getFirestore(app);

    export { auth, db };
    ```

6. Start the development server:

    ```bash
    npm start
    ```

7. Open your browser and navigate to `http://localhost:3000`.

## Deployment

1. Build the project:

    ```bash
    npm run build
    ```

2. Deploy to Firebase Hosting:

    ```bash
    firebase deploy
    ```

## Project Structure

```plaintext
task-manager-app/
├── public/
│   ├── index.html
│   └── style.css
├── src/
│   ├── components/
│   │   ├── Auth.js
│   │   ├── TaskList.js
│   │   ├── AddTask.js
│   │   └── EditTask.js
│   ├── firebase.js
│   ├── App.js
│   └── index.js
├── .gitignore
├── package.json
└── README.md
