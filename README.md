# Fitness and Workout Management System

A **Fitness and Workout Management System** that provides functionalities for managing users, workout plans, exercises, nutrition plans, and client progress. The system supports role-based dashboards for Admin, Trainers, Nutritionists, and Clients, enabling seamless interaction and fitness goal tracking.

## Table of Contents
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Setup Instructions](#setup-instructions)
- [APIs](#apis)
- [Usage](#usage)
- [Future Enhancements](#future-enhancements)

---

## Features
- **Admin Panel**: Manage users, workout plans, exercises, nutrition plans, and client progress.
- **Role-Based Access Control (RBAC)**: Admin, Trainer, Client (User), and Nutritionist roles with tailored access.
- **Workout Plan Management**: Trainers can create and manage customizable workout plans.
- **Nutrition Plan Management**: Nutritionists can recommend personalized diet plans.
- **Client Progress Tracking**: Clients can track workouts, progress, and milestones.
- **Exercise Database**: A comprehensive list of exercises categorized by muscle group, equipment, and type.
- **Class Management**: Trainers and gym managers can schedule and manage fitness classes.
- **Subscription and Payment Management**: Manage user subscriptions and track payment history.
- **Health and Fitness Challenges**: Create and manage fitness challenges for users to participate in.
- **Mobile App Compatibility**: Ensure access across desktop, tablet, and mobile platforms.

---

## Technologies Used
### Backend
- **.NET (C#)**: RESTful API development.
- **SQL Server**: Relational database for managing user data, workout plans, progress, and more.
- **Entity Framework Core**: ORM for database interaction.
- **JWT Authentication**: For secure access and role-based permissions.

### Frontend
- **Angular 18**: Frontend for managing users, workout plans, and nutrition.
- **Tailwind CSS**: For responsive and modern UI design.

### Other Tools
- **SQL Server**: Database management for storing and managing data.
- **Entity Framework Core**: ORM for database interaction.

---


## Setup Instructions
### Prerequisites
1. **.NET SDK (C#)**: For backend development.
2. **SQL Server**: Database management system.
3. **Node.js and npm**: For frontend development.
4. **Angular CLI**: For building and running the Angular application.


### Backend Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/fitness-backend.git
   cd fitness-backend
      ```
2. Configure SQL Server connection in appsettings.json:
   ```:
    "DefaultConnection": "Server=<your-server>;Database=FitnessDB;User Id=<your-username>;Password=<your-password>;"
   ```
3. Install the necessary NuGet packages:
   ```bash
   dotnet restore
   ```
4. Build and run the backend application:
  ```bash
  dotnet build
  dotnet run
   ```

### Frontend Setup
1. Navigate to the frontend folder:
   ```bash
   cd -frontend
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Run the development server:
   ```bash
   ng serve
   ```
   The application will be available at `http://localhost:4200`.


---

## APIs

### Auth APIs
- **POST /api/Auth/login**: To login.
- **POST /api/Auth/register**: To register a new user.
- **GET /api/Auth/getData**: To get user data.

### Challenges APIs
- **GET /api/Challenges**: Fetch all challenges.
- **POST /api/Challenges**: Create a new challenge.
- **GET /api/Challenges/{challengeId}**: Fetch a specific challenge by ID.
- **PUT /api/Challenges/{challengeId}**: Update a challenge by ID.
- **DELETE /api/Challenges/{id}**: Delete a challenge by ID.

### FitnessClass APIs
- **GET /api/FitnessClass**: Fetch all fitness classes.
- **POST /api/FitnessClass**: Add a new fitness class.
- **GET /api/FitnessClass/{id}**: Fetch a fitness class by ID.
- **PUT /api/FitnessClass/{id}**: Update a fitness class by ID.
- **DELETE /api/FitnessClass/{id}**: Delete a fitness class by ID.

### MealPlans APIs
- **GET /api/MealPlans**: Fetch all meal plans.
- **POST /api/MealPlans**: Add a new meal plan.
- **GET /api/MealPlans/{userId}**: Fetch meal plans for a specific user by user ID.
- **PUT /api/MealPlans/{mealPlanId}**: Update a meal plan by ID.
- **DELETE /api/MealPlans/{mealPlanId}**: Delete a meal plan by ID.

### Message APIs
- **GET /api/Message/{senderId}**: Fetch messages by sender ID.
- **POST /api/Message**: Send a new message.

### Payment APIs
- **GET /api/Payment**: Fetch all payment records.
- **POST /api/Payment**: Add a new payment record.
- **GET /api/Payment/{id}**: Fetch a payment record by ID.
- **PUT /api/Payment/{id}**: Update a payment record by ID.
- **DELETE /api/Payment/{id}**: Delete a payment record by ID.

### ProgressTracking APIs
- **GET /api/ProgressTracking/my-progress**: Fetch progress of the current user.
- **POST /api/ProgressTracking/update-progress**: Update progress tracking.

### Subscription APIs
- **GET /api/Subscription**: Fetch all subscription records.
- **POST /api/Subscription**: Create a new subscription.
- **GET /api/Subscription/{id}**: Fetch a subscription by ID.
- **PUT /api/Subscription/{id}**: Update a subscription by ID.
- **DELETE /api/Subscription/{id}**: Delete a subscription by ID.

### User APIs
- **GET /api/User**: Fetch all users.
- **POST /api/User**: Add a new user.
- **GET /api/User/{id}**: Fetch a user by ID.
- **PUT /api/User/{id}**: Update a user by ID.
- **DELETE /api/User/{id}**: Delete a user by ID.

### Workout APIs
- **POST /api/Workout/WorkoutPlan**: Create a new workout plan.
- **GET /api/Workout**: Fetch all workout sessions.
- **GET /api/Workout/WorkoutPlan/{planId}**: Fetch a specific workout plan by ID.
- **PUT /api/Workout/WorkoutPlan/{planId}**: Update a workout plan by ID.
- **DELETE /api/Workout/WorkoutPlan/{planId}**: Delete a workout plan by ID.

### WorkoutCategory APIs
- **GET /api/WorkoutCategory**: Fetch all workout categories.
- **POST /api/WorkoutCategory**: Add a new workout category.
- **GET /api/WorkoutCategory/{id}**: Fetch a workout category by ID.
- **PUT /api/WorkoutCategory/{id}**: Update a workout category by ID.
- **DELETE /api/WorkoutCategory/{id}**: Delete a workout category by ID.

---

## Usage
1. Launch the backend server (`https://localhost:7039`).
2. Run the Angular frontend (`http://localhost:4200`).
3. Access the admin panel to manage challenges, fitness classes, meal plans, subscriptions, and other features.

---

## Future Enhancements
1. **User Authentication and Roles**: Separate admin and user privileges to restrict access to sensitive endpoints.
2. **Real-Time Notifications**: Implement notifications for progress updates, meal plan changes, and workout schedules.
3. **Analytics Dashboard**: Provide insights on user activity, progress tracking, subscriptions, and payments.
4. **Mobile Responsiveness**: Improve the user interface to ensure optimal usability on mobile devices.


