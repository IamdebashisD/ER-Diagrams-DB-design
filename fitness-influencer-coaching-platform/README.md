# 🏋️ Fitness Influencer Coaching Platform - ER Diagram

## 📌 Overview

This project represents the database design for a **Fitness Influencer Coaching Platform**, where trainers provide online coaching services to clients.

The system supports:

* Trainer–client relationships
* Coaching plans & subscriptions
* Session scheduling
* Progress tracking
* Payments management

---

## 🧠 Core Idea

Instead of creating separate tables for trainers and clients, we use a single **`users`** table and differentiate roles using a `role` field.

---

## 🗂️ Entities & Description

### 👤 Users

Stores all platform users (both trainers and clients).

**Key Attributes:**

* `id` (PK)
* `name`
* `email` (unique)
* `role` (trainer/client)
* `password_hash`
* `is_active`
* `created_at`

---

### 🔗 Trainer_Clients

Maps trainers to their clients (Many-to-Many relationship).

**Key Attributes:**

* `id` (PK)
* `trainer_id` (FK → users.id)
* `client_id` (FK → users.id)

---

### 📦 Plans

Represents coaching programs created by trainers.

**Key Attributes:**

* `id` (PK)
* `trainer_id` (FK → users.id)
* `name`
* `price`
* `description`
* `duration_days`

---

### 🧾 Subscriptions

Tracks which client purchased which plan.

**Key Attributes:**

* `id` (PK)
* `client_id` (FK → users.id)
* `plan_id` (FK → plans.id)
* `start_date`
* `end_date`
* `status`

---

### 📅 Sessions

Stores scheduled consultations or training sessions.

**Key Attributes:**

* `id` (PK)
* `trainer_id` (FK → users.id)
* `client_id` (FK → users.id)
* `session_date`
* `session_type`
* `status`

---

### 📝 Check-ins

Weekly or periodic updates submitted by clients.

**Key Attributes:**

* `id` (PK)
* `client_id` (FK → users.id)
* `checkin_date`
* `weight`
* `notes`

---

### 📊 Progress

Tracks detailed body measurements over time.

**Key Attributes:**

* `id` (PK)
* `client_id` (FK → users.id)
* `date`
* `weight`
* `body_fat`
* `chest`
* `waist`

---

### 🧠 Trainer Notes

Private notes added by trainers for clients.

**Key Attributes:**

* `id` (PK)
* `trainer_id` (FK → users.id)
* `client_id` (FK → users.id)
* `note`
* `created_at`

---

### 💳 Payments

Stores payment details for subscriptions.

**Key Attributes:**

* `id` (PK)
* `subscription_id` (FK → subscriptions.id)
* `amount`
* `status`
* `method`
* `payment_date`

---

## 🔗 Relationships Summary

* One **trainer** can have multiple **clients**
* One **client** can subscribe to multiple **plans**
* One **plan** can be purchased by multiple **clients**
* One **subscription** can have one or more **payments**
* One **trainer/client pair** can have multiple **sessions**
* One **client** can submit multiple **check-ins**
* One **client** can have multiple **progress records**

---

## 🎯 Key Design Decisions

* ✅ Single `users` table for scalability
* ✅ Separate `subscriptions` table for many-to-many (clients ↔ plans)
* ✅ Normalized structure (no data duplication)
* ✅ Time-based tracking (progress, check-ins, sessions)
* ✅ Clean separation of concerns

---

## 🚀 Conclusion

This ER design models a real-world online coaching platform with proper normalization, scalability, and clear relationships. It ensures flexibility for future features like diet plans, workout routines, and analytics.

---






