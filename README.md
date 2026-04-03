<div align="center">
  <h1>🥗 NutriGuide AI</h1>
  <p><strong>Smart Diet & Meal Recommendation System</strong></p>
  
  [![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
  [![Node.js](https://img.shields.io/badge/Node.js-18+-339933?logo=node.js&logoColor=white)](https://nodejs.org)
  [![React](https://img.shields.io/badge/React-18-61DAFB?logo=react&logoColor=white)](https://reactjs.org)
  [![Python](https://img.shields.io/badge/Python-3.8+-3776AB?logo=python&logoColor=white)](https://python.org)
  [![MongoDB](https://img.shields.io/badge/MongoDB-6.0-47A248?logo=mongodb&logoColor=white)](https://www.mongodb.com)
  [![ML Accuracy](https://img.shields.io/badge/ML%20Accuracy-99.87%25-success)](ml-service/README.md)

  <p>A full-stack AI-powered nutrition platform that provides personalized meal recommendations using machine learning trained on 230K+ real recipes.</p>

  **Developed by Akanksha — 2nd Year CSE Student**

  [Features](#-features) • [Project Structure](#-project-structure) • [Tech Stack](#-technology-stack) • [Installation](#-installation--setup) • [API Docs](#-api-documentation)
</div>

---

## 👩‍💻 About the Developer

Hi! I'm **Akanksha**, a 2nd year Computer Science Engineering student. I built **NutriGuide AI** as a personal project to explore full-stack web development combined with machine learning.

This project helped me learn and apply:
- Building REST APIs with Node.js & Express
- Designing frontend UIs using React and Tailwind CSS
- Training and deploying ML models with Python & Scikit-learn
- Connecting a NoSQL database (MongoDB) to a real-world application
- Integrating a separate ML microservice with a main backend

---

## 📖 About the Project

**NutriGuide AI** is an AI-powered nutrition and meal planning web application. It takes your personal health data (age, weight, height, activity level, fitness goal) and uses a machine learning model to give you a personalized daily calorie target and meal recommendations.

The project is divided into 3 services that work together — a React frontend, a Node.js backend, and a Python ML service.

---

## ✨ Features

- 🤖 **ML-Powered Calorie Predictions** — Gradient Boosting model with 99.87% accuracy, trained on 230K+ real recipes from Kaggle
- 🔐 **Secure Authentication** — JWT-based login & registration with role-based access (Admin / User)
- 👤 **Health Profiles** — Set your age, weight, height, activity level, and fitness goal
- 🍽️ **500+ Meal Database** — Search and filter meals by calories, protein, dietary preferences (vegan, keto, gluten-free)
- 📊 **Progress Tracking** — Log meals daily and visualize your nutrition trends with charts
- 🛡️ **Admin Dashboard** — Manage users and the meal database

---

## 📁 Project Structure

```
NutriGuide/
├── backend/                    # Node.js + Express.js Backend API
│   ├── controllers/            # Business logic for each route
│   │   ├── auth.controller.js
│   │   ├── user.controller.js
│   │   ├── meal.controller.js
│   │   ├── nutrition.controller.js
│   │   ├── progress.controller.js
│   │   └── admin.controller.js
│   ├── models/                 # MongoDB Schemas
│   │   ├── User.model.js
│   │   ├── Meal.model.js
│   │   └── Progress.model.js
│   ├── routes/                 # API route definitions
│   │   ├── auth.routes.js
│   │   ├── user.routes.js
│   │   ├── meal.routes.js
│   │   ├── nutrition.routes.js
│   │   ├── progress.routes.js
│   │   └── admin.routes.js
│   ├── middleware/             # Auth, validation, error handling
│   │   ├── auth.middleware.js
│   │   ├── validation.middleware.js
│   │   └── error.middleware.js
│   ├── seeds/                  # Database seed data
│   │   ├── seed.js
│   │   └── meals_seed.json
│   ├── server.js               # Main Express server entry point
│   ├── .env.example
│   └── package.json
│
├── frontend/                   # React + Vite Frontend
│   ├── src/
│   │   ├── components/         # Reusable UI components
│   │   │   ├── Layout.jsx
│   │   │   ├── PrivateRoute.jsx
│   │   │   └── AdminRoute.jsx
│   │   ├── pages/              # All app pages
│   │   │   ├── LandingPage.jsx
│   │   │   ├── LoginPage.jsx
│   │   │   ├── RegisterPage.jsx
│   │   │   ├── DashboardPage.jsx
│   │   │   ├── MealsPage.jsx
│   │   │   ├── ProgressPage.jsx
│   │   │   ├── AnalyticsPage.jsx
│   │   │   ├── ProfilePage.jsx
│   │   │   └── AdminDashboard.jsx
│   │   ├── services/           # API call functions
│   │   ├── store/              # Zustand global state
│   │   ├── utils/              # Axios config & helpers
│   │   ├── App.jsx             # Routes & app setup
│   │   └── main.jsx            # Entry point
│   ├── index.html
│   ├── tailwind.config.js
│   ├── vite.config.js
│   └── package.json
│
├── ml-service/                 # Python Flask ML Service
│   ├── app.py                  # Flask API for predictions
│   ├── train_model.py          # Train the ML model
│   ├── train_model_with_real_data.py
│   ├── train_meal_recommendation.py
│   ├── preprocess_data.py      # Data preprocessing pipeline
│   ├── create_meal_database.py
│   ├── models/                 # Saved trained model files
│   │   ├── meal_index.json
│   │   ├── model_stats.json
│   │   └── recommendation_stats.json
│   ├── requirements.txt
│   └── README.md
│
├── datasets/                   # Raw nutrition datasets (CSV)
│   ├── nutrition.csv
│   └── processed_meals.csv
│
└── README.md
```

---

## 🚀 Technology Stack

### Frontend
| Library | Purpose |
|--------|---------|
| React 18 | UI framework |
| Vite | Build tool & dev server |
| Tailwind CSS | Styling |
| React Router DOM | Page routing |
| Zustand | Global state management |
| Axios | HTTP requests |
| Recharts | Data visualization charts |
| Framer Motion | Animations |
| React Hook Form | Form handling |
| React Hot Toast | Notifications |

### Backend
| Library | Purpose |
|--------|---------|
| Node.js + Express.js | Server & API |
| MongoDB + Mongoose | Database & ODM |
| JWT | Authentication |
| bcryptjs | Password hashing |
| Helmet | Security headers |
| express-rate-limit | Rate limiting |
| Morgan | HTTP logging |
| CORS | Cross-origin support |

### ML Service
| Library | Purpose |
|--------|---------|
| Python + Flask | ML API server |
| Scikit-learn | ML models (Gradient Boosting, Random Forest) |
| Pandas + NumPy | Data processing |
| Joblib | Model serialization |

---

## 🤖 Machine Learning Model

The ML model predicts your **daily calorie needs** based on your personal health data.

**Model:** Gradient Boosting Regressor  
**Dataset:** Food.com Recipes (Kaggle) — 230,286 recipes  
**Accuracy:** 99.87% (Test R² = 0.9987, MAE = 5.62 calories)

### Input Features (14 total)

| Feature | Description |
|--------|-------------|
| Age | User's age in years |
| Gender | Male / Female |
| Height | In centimeters |
| Weight | In kilograms |
| BMI | Calculated from height & weight |
| BMR | Basal Metabolic Rate (Mifflin-St Jeor) |
| Activity Level | Sedentary → Very Active (0–4) |
| Fitness Goal | Lose / Maintain / Gain (0–2) |
| + 6 engineered features | BMI×Age, Weight/Height, BMR×Activity, etc. |

### Model Comparison

| Model | Test MAE | Test R² |
|-------|----------|---------|
| **Gradient Boosting** ✅ | **5.62 cal** | **0.9987** |
| Random Forest | 6.75 cal | 0.9976 |
| Ridge Regression | 47.40 cal | 0.9897 |
| Linear Regression | 47.43 cal | 0.9896 |

---

## 🛠️ Installation & Setup

### Prerequisites
- Node.js v18+
- Python 3.8+
- MongoDB (local or Atlas)
- npm

---

### Step 1 — Backend Setup

```bash
cd backend

# Install dependencies
npm install

# Create environment file
cp .env.example .env
# Edit .env: set MONGODB_URI, JWT_SECRET, ML_SERVICE_URL, FRONTEND_URL

# Start backend (runs on port 5000)
npm run dev
```

---

### Step 2 — ML Service Setup

```bash
cd ml-service

# Create virtual environment
python3 -m venv venv
source venv/bin/activate        # Linux/macOS
# OR: venv\Scripts\activate     # Windows

# Install dependencies
pip install -r requirements.txt

# Train the model (first time only)
python train_model.py

# Start ML service (runs on port 5001)
python app.py
```

---

### Step 3 — Frontend Setup

```bash
cd frontend

# Install dependencies
npm install

# Create environment file
cp .env.example .env
# Set: VITE_API_URL=http://localhost:5000/api

# Start frontend (runs on port 5173)
npm run dev
```

---

### Step 4 — Seed the Database (Optional)

```bash
cd backend
npm run seed
```

This loads 500+ real meals into MongoDB.

---

### All 3 Services Running

| Service | URL |
|---------|-----|
| Frontend | http://localhost:5173 |
| Backend API | http://localhost:5000 |
| ML Service | http://localhost:5001 |

---

## 🔐 API Documentation

**Base URL:** `http://localhost:5000/api`

### Auth Routes

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/auth/register` | Create new account |
| POST | `/auth/login` | Login & get JWT token |

### User Routes *(requires token)*

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/users/dashboard` | Get user dashboard data |
| PUT | `/users/profile` | Update profile info |

### Nutrition Routes *(requires token)*

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/nutrition/recommendations` | Get AI calorie & macro targets |
| POST | `/nutrition/meal-plan` | Generate meal plan for a date |

### Meal Routes

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/meals` | Search meals (filter by category, calories) |
| GET | `/meals/search/recommendations` | Get meals matching calorie target |

### Progress Routes *(requires token)*

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/progress/today` | Get today's nutrition log |
| POST | `/progress/log-meal` | Log a meal |
| PUT | `/progress/update-weight` | Update weight |

---

## 🗃️ Database Schema

### User
```js
{
  name, email, password (hashed),
  age, gender, height, weight, bmi,
  activityLevel, fitnessGoal,
  dailyCalorieTarget,
  macronutrients: { protein, carbs, fats },
  dietaryPreferences: [],
  allergies: [],
  role: "user" | "admin"
}
```

### Meal
```js
{
  name, description, category,
  nutrition: { calories, protein, carbohydrates, fats, fiber, sugar },
  dietaryTags: [],
  allergens: [],
  ingredients: [],
  prepTime, cookTime
}
```

### Progress
```js
{
  user: ObjectId,
  date,
  weight,
  nutrition: { calories, protein, carbohydrates, fats },
  meals: [{ mealId, mealName, servings, calories, consumedAt }],
  compliance: { calorieCompliance, macroCompliance }
}
```

---

## 📄 License

This project is licensed under the MIT License. 

---

<div align="center">
  <p>Built with ❤️ by <strong>Akanksha</strong> — 2nd Year CSE</p>
  <p><em>NutriGuide AI — Empowering healthier lives through AI and technology</em></p>
</div>
