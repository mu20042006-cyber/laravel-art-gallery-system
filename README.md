<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

# 🎨 Art Gallery Management System

A Laravel-based web application built using MVC architecture.

This project was developed as part of the **Pixels’26 Course** and represents my **first backend project**.

---

## 🚀 Project Overview

The Art Gallery Management System allows:

- **Admin (Gallery Manager)** to manage artworks and monitor purchases.
- **Users (Buyers)** to browse artworks and purchase them securely.

All new registered accounts are automatically assigned the **User role** by default.  
The **Admin account is created separately with predefined credentials** to control access to management features.

---

## 👩‍💼 Admin Features

- Full CRUD operations for artworks  
- Upload artwork images  
- Set price and available quantity  
- View all purchase records including:
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
- View artwork details (image, description, price, quantity)  
- Purchase artworks  
- Automatic total price calculation  
- Prevent purchasing more than available stock  
- Sold-out artworks remain visible but cannot be purchased  

---

## 🧠 Business Logic

- Quantity validation before purchase  
- Automatic stock update after each purchase  
- Role-based redirection after login (Admin / User)  
- Foreign key relationships with proper constraint handling  

---

## 🗄 Database Structure

### Users
- id  
- name  
- email  
- password  
- role  
- created_at  
- updated_at  

### Artworks
- id  
- title  
- description  
- price  
- quantity  
- image  
- created_at  
- updated_at  

### Purchases
- id  
- user_id  
- artwork_id  
- quantity  
- total_price  
- date  
- created_at  
- updated_at  

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
