# 🏥 Clinic Appointment & Diagnostics ERD

## 📌 Overview

This project represents a database design for a clinic system that manages appointments, consultations, diagnostic tests, reports, and payments.

---

## 🧱 Core Entities

* Patients
* Doctors (with specialties)
* Appointments
* Consultations
* Tests
* Reports
* Payments

---

## 🔗 Key Relationships

* A patient can book multiple appointments
* A doctor can handle multiple appointments
* An appointment may result in a consultation
* A consultation can have multiple tests
* Each test generates a report
* Payments are linked to appointments

---

## 🎯 Highlights

* Clear separation between appointment and consultation
* Proper handling of many-to-many (consultation ↔ tests)
* Normalized and scalable design

---

## 🚀 Output

ER diagram created using Eraser and exported as an image for submission.
