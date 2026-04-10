# 🏢 Smart Elevator Control System ERD

## Overview

This project is a database design for a smart elevator system used in large buildings. It manages elevators, floor requests, ride assignments, and maintenance tracking.

---


## Main Entities

* **Buildings** – stores building details
* **Floors** – floors inside each building
* **Elevators & Shafts** – elevators and their positions
* **Floor Requests** – requests made by users (up/down)
* **Ride Assignments** – which elevator handles a request
* **Ride Logs** – completed elevator trips
* **Status Logs** – current status of elevators
* **Maintenance Logs** – repair and maintenance history

---


## Key Relationships

* One building has many floors and elevators
* One elevator serves multiple floors (via mapping table)
* One floor can be served by multiple elevators
* One request is assigned to one elevator
* One elevator completes many rides
* Maintenance and status are tracked separately

---


## 🚀 Output

ER diagram created using Eraser and exported for submission.
