# 🍔 Food Order System API

A robust Node.js-based food delivery application built with Express.js and MongoDB. This app is designed to manage customers, vendors, delivery users, orders, offers, and transactions. It features secure authentication, OTP notifications, and a comprehensive API—making it a scalable solution for food delivery services.

> **Learning Context:**  
This project was built by following the **"Node.js Beginner's Guide: Master the Basics with This Comprehensive Playlist!"** YouTube series, covering server setup, database integration, and full-stack API development.

---

## 🚀 Features

### 👤 Customer Management
- Signup, login, profile editing
- Account verification and OTP via SMS
- Cart management and order creation
- Apply discount offers

### 👨‍🍳 Vendor Operations
- Vendor registration and login
- Profile management
- Food item creation (with image upload)
- Order processing and offer management

### 🚴 Delivery User System
- Signup, login, profile updates
- Toggle availability status for order assignments

### 🛒 Shopping Functionality
- Search food items
- Discover top restaurants
- Check food availability by pincode
- Find foods deliverable within 30 minutes

### 💳 Order & Payment Processing
- Create and manage orders
- Process payments
- Track transactions and statuses

### 🎟️ Offer System
- Vendor-specific promocodes
- Set offer validity and minimum order value
- Apply and verify offers

### 🛠️ Admin Dashboard
- Manage vendors
- Verify delivery users
- Monitor transactions

---

## 🧱 Tech Stack

- **Backend:** Node.js, Express.js  
- **Database:** MongoDB with Mongoose  
- **Authentication:** JWT, bcrypt  
- **Notifications:** Twilio for SMS OTP  
- **Input Validation:** class-validator (with DTOs)  
- **File Uploads:** Multer (for images)  
- **Config:** .env for sensitive credentials

---

## 📁 Project Structure

- `controllers/` - Business logic for customer, vendor, shopping, delivery, and admin
- `routes/` - API endpoint definitions
- `models/` - Mongoose schemas (Customer, Vendor, Food, Order, etc.)
- `dto/` - Data Transfer Objects for validating inputs
- `utility/` - OTP generator, password encryption, and JWT functions
- `database/` - MongoDB connection setup
- `ExpressApp.ts` - Initializes middleware, static files, and routes

---

## ⚙️ Setup Instructions

### 1. Clone the Repository

```bash
git clone <repo-url>
cd food-delivery-platform
**2. Install Dependencies
bash
Copy
Edit
npm install
3. Configure Environment Variables
Create a .env file in the root directory with the following:

env
Copy
Edit
MONGO_URI=<your-mongodb-connection-string>
APP_SECRET=<your-jwt-secret>
TWILIO_ACCOUNT_SID=<your-twilio-account-sid>
TWILIO_AUTH_TOKEN=<your-twilio-auth-token>
TWILIO_PHONE_NUMBER=<your-twilio-phone-number>
4. Start the Server
bash
Copy
Edit
npm start
The API will be accessible at:
http://localhost:8000

Use tools like Postman to test the endpoints.

📌 Key API Endpoints
🧑 Customer
POST /customer/signup – Register a new customer

POST /customer/login – Login and receive JWT

POST /customer/cart – Add items to cart

POST /customer/create-order – Create a new order

GET /customer/offer/verify/:id – Verify offer by ID

🧑‍🍳 Vendor
POST /vendor/login – Login as vendor

POST /vendor/food – Add food item (with image)

GET /vendor/orders – Get vendor’s orders

POST /vendor/offer – Create a vendor-specific offer

🛍️ Shopping
GET /pincode – Check food availability by pincode

GET /search/:pincode – Search foods in specific area

GET /offers/:pincode – List all offers for a pincode

🚴 Delivery
POST /delivery/signup – Register delivery personnel

PUT /delivery/change-status – Update availability

🛠️ Admin
POST /admin/vendor – Create a new vendor

GET /admin/transactions – View all transactions

PUT /admin/delivery/verify – Approve a delivery user

🤝 Contributing
Contributions are welcome! To contribute:

Fork the repository

Create a new branch

bash
Copy
Edit
git checkout -b feature/YourFeature
Commit your changes

bash
Copy
Edit
git commit -m "Add YourFeature"
Push the branch

bash
Copy
Edit
git push origin feature/YourFeature
Open a Pull Request

📚 Learning Summary
This project helps reinforce the following Node.js concepts:

RESTful API design with Express

MongoDB data modeling with Mongoose

Token-based authentication (JWT)

Password hashing (bcrypt)

OTP-based verification via Twilio

Modular architecture with controllers and services

File handling and image uploads with Multer

Environment configuration for secure deployment**
