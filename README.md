# Firebase Authentication App

This project is a simple Android application that implements user authentication using Firebase Authentication. The app allows users to register with email and password, log in, and be redirected to a home screen after successful authentication.

---

## Features
- **User Registration:** Users can register with an email and password.
- **User Login:** Login with previously registered credentials.
- **Home Screen:** After logging in, users are redirected to a welcome screen.

---

## Technologies Used
- **Language:** Kotlin
- **User Interface:** XML
- **Backend-as-a-Service:** Firebase Authentication
- **IDE:** Android Studio

---

## Initial Setup
### Prerequisites
- Android Studio installed
- Firebase account

### Setup Steps
1. **Clone the Repository:**
   ```bash
   git clone https://github.com/usuario/firebase-auth-app.git
   cd firebase-auth-app
   ```

2. **Configure Firebase:**
   - In the Firebase Console, create a new project.
   - Add an Android app to the project using the app package name.
   - Download the `google-services.json` file and place it in the `app/` folder.

3. **Add Dependencies:**
   In the `build.gradle` file (app-level):
   ```gradle
   implementation 'com.google.firebase:firebase-auth-ktx:21.3.0'
   ```
   In the `build.gradle` file (project-level):
   ```gradle
   classpath 'com.google.gms:google-services:4.3.15'
   ```
   Make sure to apply the plugin at the end of the `build.gradle` file (app-level):
   ```gradle
   apply plugin: 'com.google.gms.google-services'
   ```

4. **Sync the Project:**
   Sync the project in Android Studio to ensure all dependencies are resolved.

---

## Project Structure
### Main Files
- **`MainActivity.kt`:** Handles user registration and login.
- **`HomeActivity.kt`:** Displays the home screen after successful authentication.
- **`activity_main.xml`:** Layout for the login/registration screen.
- **`activity_home.xml`:** Layout for the home screen.

### Layouts
- **`activity_main.xml`:** Contains fields for email, password, and buttons for login and registration.
- **`activity_home.xml`:** Displays a welcome message to the user.

---

## Running the Project
1. Open the project in Android Studio.
2. Connect a physical device or start an emulator.
3. Click **Run** to execute the application.

---

## Possible Issues
### Issue: "FirebaseApp not initialized"
**Solution:** Ensure the `google-services.json` file is in the correct folder and the `com.google.gms.google-services` plugin is applied.

### Issue: "Unresolved reference: onCreate"
**Solution:** Ensure all Activity classes inherit from `AppCompatActivity` and have the `onCreate` method overridden.
