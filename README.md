# Hospital-Management-System
A Java-based console application that helps manage a hospital's basic operations, such as adding/viewing patients and doctors, and booking appointments. Built using JDBC and MySQL, this project is designed for learning and demonstration purposes.

## 🏥 Hospital Management System

A simple **Java console-based application** designed to manage core hospital operations efficiently. The system allows the user to:

- Add and view patient records
- View doctor details and their specializations
- Book appointments between patients and doctors
- Ensure no double-booking of doctors on the same date

This project is built using **Java**, connected to a **MySQL** database using **JDBC** (Java Database Connectivity). It's a great mini-project for students and beginners looking to understand how database-backed applications work.

# 🏥 Hospital Management System

---

## 📋 Features

- Add a new patient
- View all patients
- View all doctors
- Book an appointment
- Check doctor availability
- MySQL database integration using JDBC

---

## 🛠️ Technologies Used

- Java
- JDBC (Java Database Connectivity)
- MySQL
- Maven (Optional)
- Console-based UI

---

## 🧱 Database Schema

### 📄 patients

| Column     | Type         | Description             |
|------------|--------------|-------------------------|
| id         | INT (PK)     | Auto-increment ID       |
| name       | VARCHAR(100) | Patient's name          |
| age        | INT          | Patient's age           |
| gender     | VARCHAR(10)  | Male/Female/Other       |
| contact    | VARCHAR(15)  | Contact number          |

### 📄 doctors

| Column        | Type         | Description             |
|---------------|--------------|-------------------------|
| id            | INT (PK)     | Auto-increment ID       |
| name          | VARCHAR(100) | Doctor's name           |
| specialization | VARCHAR(100)| Medical specialization  |

### 📄 appointments

| Column          | Type | Description |
|-----------------|------|-------------|
| id              | INT (PK) | Auto-increment ID |
| patient_id      | INT (FK) | Refers `patients(id)` |
| doctor_id       | INT (FK) | Refers `doctors(id)` |
| appointment_date| DATE     | Date of appointment |
| *Constraints*   | -        | UNIQUE(doctor_id, appointment_date) |

---

## 🚀 How to Run

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/hospital-management-system.git
   cd hospital-management-system
