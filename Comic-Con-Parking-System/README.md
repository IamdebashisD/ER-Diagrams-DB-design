# 🚗 Comic-Con Parking System ERD
### Overview

This project represents a database design for a multi-zone parking system used during a large event like Comic-Con. It handles vehicle entry, parking allocation, sessions, and payments.

### Core Entities
- Vehicles
- Parking Zones & Spots
- Spot Categories (VIP, Staff, EV, etc.)
- Parking Tickets
- Parking Sessions
- Payments

### Key Relationships
- A vehicle can have multiple parking sessions
- A parking spot can be reused across multiple sessions
- Each session is linked to one vehicle, one spot, and one ticket
- Zones contain multiple parking spots
- Payments are linked to parking sessions

### Highlights
- Supports multi-zone and multi-level parking
- Tracks entry and exit via parking sessions
- Handles reserved parking categories
- Clean and normalized design

###  Output

ER diagram created using Eraser and exported for submission.