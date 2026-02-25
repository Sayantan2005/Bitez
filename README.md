# 🍔 Bitez – MERN Stack Food Delivery Platform

Bitez is a full-stack food delivery web application built using the MERN stack.  
It allows users to order food from nearby shops, track deliveries in real-time, and make secure payments.

---

## 🚀 Features

### 👤 User
- User Registration & Login (JWT Authentication)
- Browse Shops by City
- Add to Cart
- Place Orders (COD / Online Payment)
- Live Delivery Tracking
- Rate Food Items (1–5 stars)

### 🏪 Shop Owner
- Add / Update / Delete Food Items
- Manage Orders
- View Earnings

### 🚴 Delivery Boy
- Accept Orders
- Live Location Sharing (Geolocation API + Socket.io)
- Order Status Update

---

## 🛠 Tech Stack

### Frontend
- React.js
- Redux Toolkit
- Axios
- Tailwind CSS
- Recharts
- Socket.io Client

### Backend
- Node.js
- Express.js
- MongoDB
- Mongoose
- JWT Authentication
- Socket.io
- Razorpay (Online Payment)

---

## 📁 Project Structure
Bitez/
│
├── backend/
│ ├── controllers/
│ ├── models/
│ ├── routes/
│ ├── middleware/
│ ├── config/
│ └── server.js
│
├── frontend/
│ ├── src/
│ ├── components/
│ ├── pages/
│ └── App.js
│
└── README.md


---

## ⚙️ Installation & Setup

### 1️⃣ Clone the Repository
git clone https://github.com/Sayantan2005/Bitez.git
cd Bitez

### 2️⃣ Backend Setup
cd backend
npm install
npm run dev

### 3️⃣ Frontend Setup
cd frontend
npm install
npm start

---

## 🌍 Real-Time Features

- Live Delivery Tracking using Geolocation API
- Real-time updates with Socket.io
- Order status synchronization

---

## 📊 Advanced Functionalities

- Order analytics dashboard
- Ratings & review system
- Secure authentication using JWT
- Protected routes (Admin / Delivery Boy)

---

## 🎯 Future Improvements

- Add Admin Panel
- Add Push Notifications
- Add Payment History

---

## 👨‍💻 Author

**Sayantan Sarkar**
---

## 📌 Note

node_modules and .env files are not included in this repository.
Install dependencies using `npm install` before running the project.

## 📁 Project Structure
