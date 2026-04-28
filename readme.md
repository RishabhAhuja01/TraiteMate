# TraitMate — All-In-One Personality Predictor

## Overview

TraitMate is a full-stack personality quiz application built with a React frontend and a Node.js/Express backend. Users can sign up, log in, take personality quizzes, save their results, and view their score breakdowns.

The source code is located in the `source code` folder, with separate `Backend` and `frontend` projects.

## Features

- User authentication with email/password registration and login
- JWT-based protected API routes
- Quiz result saving and retrieval from MongoDB
- Multiple quiz categories:
  - Work Personality
  - Family Life
  - Social Personality
  - Romantic Personality
- Result visualization using pie charts
- Responsive React user interface with route-based navigation

## Project Structure

- `source code/Backend`
  - Express API server
  - Authentication controllers
  - Quiz result controllers
  - MongoDB models for users and quiz results
- `source code/frontend`
  - React app created with Create React App
  - Components for homepage, login/signup, quiz selection, quiz flow, and results
  - React Router for navigation

## Backend API Endpoints

- `POST /api/auth/register` — register a new user
- `POST /api/auth/login` — log in and receive a JWT
- `POST /api/quiz/results` — save a quiz result (authenticated)
- `GET /api/quiz/results` — fetch saved quiz results for the current user (authenticated)

## Backend Setup

1. Open a terminal and navigate to the backend folder:

```powershell
cd "source code\Backend"
```

2. Install dependencies:

```powershell
npm install
```

3. Create a `.env` file in `source code\Backend` with at least the following values:

```env
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
```

4. Start the backend server:

```powershell
npm start
```

The backend server will run on `http://localhost:5000` by default.

## Frontend Setup

1. Open a terminal and navigate to the frontend folder:

```powershell
cd "source code\frontend"
```

2. Install dependencies:

```powershell
npm install
```

3. Start the frontend development server:

```powershell
npm start
```

The frontend app will run on `http://localhost:3000` by default.

## Usage

1. Open the app in your browser at `http://localhost:3000`.
2. Register a new account or log in with existing credentials.
3. Select a quiz category.
4. Answer the quiz questions.
5. View your personality result and saved history.

## Notes

- The frontend stores the authentication token and user data in local storage.
- Quiz results are saved to MongoDB and retrieved for the authenticated user.
- The app uses `chart.js` and `react-chartjs-2` to display result percentages visually.

## Authors

- Rishabh Ahuja
- Sarthak Bansal
- Rajat Singh
- Prashant Sheoran

---

> This README was generated for the project located in `source code`.
