# 🎨 Art Gallery Management System

A web-based Art Gallery Management System built using Laravel MVC architecture.

This project was developed as part of the Pixels’26 Course and represents my first backend project.

---

## 🚀 Project Overview

The system allows:

- Admin (Gallery Manager) to manage artworks and monitor purchases.
- Users (Buyers) to browse available artworks and purchase them securely.

All registered accounts are assigned the **User role by default**, while the **Admin account is created separately with predefined credentials**.

---

## 👩‍💼 Admin Features

- Full CRUD operations for artworks
- Upload artwork images
- Set price and available quantity
- View all purchase records:
  - Buyer name
  - Artwork title
  - Quantity
  - Total price
  - Purchase date

---

## 🛒 User Features

- Secure authentication using Laravel Breeze
- Browse all artworks
- Search artworks by title
- View artwork details:
  - Image
  - Description
  - Price
  - Available quantity
- Purchase artworks
- Automatic total price calculation
- Stock validation & sold-out protection

---

## 🧠 Business Rules

- A user cannot purchase more than available quantity.
- Artwork quantity updates automatically after each purchase.
- Sold-out artworks remain visible but cannot be purchased.
- Role-based redirection after login (Admin / User).

---

## 🗄 Database Structure

### Users
- id
- name
- email
- password
- role
- timestamps

### Artworks
- id
- title
- description
- price
- quantity
- image
- timestamps

### Purchases
- id
- user_id
- artwork_id
- quantity
- total_price
- date
- timestamps

### Relationships
- User → hasMany Purchases
- Artwork → hasMany Purchases
- Purchase → belongsTo User
- Purchase → belongsTo Artwork

---

## 🛠 Tech Stack

- Laravel (MVC Architecture)
- Eloquent ORM
- Blade Templates
- Laravel Breeze Authentication
- MySQL
- Form Request Validation

---
 👩‍💻 Author
 Menna ahmed 
ة
Backend Developer in progress 🚀
Built as part of Pixels’26 Course.
