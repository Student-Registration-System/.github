# Student Registration System

## Overview

The Student Registration System is a web and mobile application designed to manage student registrations efficiently. The system consists of a Laravel backend serving as the API and a Flutter frontend for an engaging user experience.

## Instructions for Running the Application

### Backend (Laravel):

1. **Setup Database:**
   - Create a MySQL database on your local machine named `student_registration_system`.

2. **Run Migrations:**
   - Execute the following commands in the Laravel backend project directory:
     ```bash
     php artisan migrate
     ```

3. **Start Development Server:**
   - Run the Laravel development server with the following command:
     ```bash
     php artisan serve --host=0.0.0.0 --port=8000
     ```

### Frontend (Flutter):

#### Before Running the Flutter App:

1. **Update API URLs:**
   - In the Flutter project, replace "localhost" with the local IP address of your machine in the following files:
     - In `form.dart`:
       ```dart
       final String apiUrl = "http://your_local_ip:8000/api/students/";
       ```
     - In `details.dart`:
       ```dart
       final response = await Dio().get('http://your_local_ip:8000/api/students');
       ```
     Replace `your_local_ip` with your actual IP address. Find it by running 'ipconfig' in a terminal on your machine.

2. **Database Configuration:**
   - Make sure you have created the MySQL database `student_registration_system` as mentioned in the backend instructions.

3. **Run the Flutter App:**
   - Execute the following command in the Flutter project directory:
     ```bash
     flutter run
     ```

## App Navigation:

- **Home Page:**
  - Upon running the app, you'll see two buttons:
    - "Register New Student": Click to register a new student with the provided details.
    - "View Registered Students": Click to view a list of all registered students.

- **View Registered Students:**
  - After registering students, you can view their details by clicking the "View Registered Students" button.
  - This will navigate to a page displaying a table with details of all registered students.
