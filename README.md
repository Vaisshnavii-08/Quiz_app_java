# Online Quiz Application


## 📌 Overview
This is a Java-based **Online Quiz Application** built using **JavaFX** for the GUI and **MySQL** for backend data persistence. The app supports **user authentication**, **role-based access control** (Admin/User), **quiz creation and participation**, and **result tracking**.

---

## 🎯 Features

### 👥 User Authentication
- Login & Signup with password hashing
- Role selection: **Admin** or **User**
- Session-based redirection (AdminDashboard / UserDashboard)

### 🧑‍💼 Admin Features
- Create quizzes with multiple questions
- View all registered users
- View quiz results of all users

### 🙋‍♂️ User Features
- Take quizzes available in the system
- View personal quiz scores

### 📋 Quiz Features
- Multiple-choice questions (MCQs)
- Score calculation upon quiz submission
- Stores results in the database

---

## 🧰 Tech Stack

| Layer        | Technology    |
|--------------|----------------|
| Programming Language | Java 21 (OpenJDK) |
| GUI Framework | JavaFX SDK 21.0.7 |
| Database     | MySQL |
| IDE          | VS Code / IntelliJ |
| Build Tool   | `javac` (manual compilation) |
| JDBC Driver  | `mysql-connector-j.jar` |

---

## ⚙️ Project Structure

```
Quiz_app/
├── LoginPage.java
├── SignupPage.java
├── AdminDashboard.java
├── UserDashboard.java
├── QuizManager.java
├── TakeQuiz.java
├── ViewResults.java
├── ViewUsers.java
├── DBConnection.java
├── Quiz.java
├── Question.java
├── utils/
│   └── PasswordUtil.java
├── assets/
│   └── (icons/images if any)
└── resources/
    └── schema.sql
```

---

## 🛠️ Setup Instructions

### 1. 🧩 Prerequisites
- Java JDK 21 installed
- JavaFX SDK 21.0.7 extracted
- MySQL Server running locally
- `mysql-connector-j.jar` available

### 2. 🏗️ Database Setup
1. Create a MySQL database named `quiz_app`.
2. Execute the SQL file `schema.sql` in MySQL Workbench or CLI.

```bash
mysql -u root -p < schema.sql
```

### 3. 📦 Build & Run

#### Compile
```bash
javac --module-path "C:\javafx-sdk-21.0.7\lib" --add-modules javafx.controls,javafx.fxml -cp ".;mysql-connector-j.jar" *.java
```

#### Run
```bash
java --module-path "C:\javafx-sdk-21.0.7\lib" --add-modules javafx.controls,javafx.fxml -cp ".;mysql-connector-j.jar" LoginPage
```

> 🔁 Replace path and filenames if needed for your system.

---

## 👩‍💻 Roles

| Role   | Username | Password | Permissions |
|--------|----------|----------|-------------|
| Admin  | admin    | admin123 | Create quizzes, view users & results |
| User   | user     | user123  | Take quizzes, view personal results |

> Note: You can also sign up as Admin or User via SignupPage.

---

