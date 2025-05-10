# 📘 Schema Overview

This schema defines the core structure for an Airbnb-like booking system, built using Prisma and designed for PostgreSQL. It includes models and relationships that represent users, properties, bookings, payments, reviews, and messaging — all key components in a real-world short-term rental platform.

---

## Entity Descriptions

### User

Represents both guests and hosts. Users can book properties, host listings, leave reviews, and send messages. The `role` field defines if the user is a `guest`, `host`, or `admin`.

### Property

Represents a rental listing posted by a host. Each property has details such as location, description, and price per night. A user can host multiple properties.

### Booking

Records a reservation made by a guest for a specific property, including the booking dates, total price, and status (`pending`, `confirmed`, or `canceled`).

### Payment

Linked to a booking, it tracks the payment amount, date, and method (`credit_card`, `paypal`, `stripe`).

### Review

Guests can leave reviews on properties they've stayed at, including a rating and comment.

### Message

Users can send and receive direct messages, facilitating communication between guests and hosts.

---

## Relationships Summary

- One **User** can own many **Properties**
- One **User** can make many **Bookings**
- One **Booking** is linked to one **Property** and one **User**
- One **Booking** has one **Payment**
- One **Property** can have many **Reviews**
- **Messages** are exchanged between two **Users** (sender and recipient)

---

## 🖼 ER Diagram

![ERD](./erd.svg)
