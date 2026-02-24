# 🌐 Local Service Booking & Tracking System



---

## 🚀 Overview

Local Service Booking & Tracking System is a full-stack MERN application that connects customers with nearby local service providers such as plumbers, electricians, cleaners, painters, and HVAC technicians.

It supports real-time booking, geolocation-based provider matching (15KM radius), live tracking, secure payments, and an admin monitoring panel.

---

## 🧩 Features

### 👤 Customer
- Browse services
- View full service details
- Location-based booking
- Distance-based pricing
- Secure in-app payment
- Real-time service tracking
- Rating & review system
- Booking history

### 🧑‍🔧 Provider
- Receive nearby service requests
- Accept / reject bookings
- Update job status
- Manage availability
- Earnings dashboard

### 🛡 Admin
- Manage customers
- Manage providers
- Approve providers
- Monitor payments
- View security logs
- System analytics dashboard

---

## 🛠 Tech Stack

### Frontend
- React.js
- React Router
- Axios
- Context API
- Tailwind CSS
- Socket.IO Client

### Backend
- Node.js
- Express.js
- MongoDB with Mongoose
- JWT Authentication
- Socket.IO
- Stripe / Razorpay Integration

### Database
- MongoDB Atlas (Geospatial indexing enabled)

---

## 📁 Project Structure
```
local-service-booking/
├── client/
│ ├── public/
│ └── src/
│ ├── routes/
│ ├── pages/
│ │ ├── Landing/
│ │ ├── Auth/
│ │ ├── Customer/
│ │ ├── Provider/
│ │ └── Admin/
│ ├── components/
│ ├── context/
│ ├── services/
│ ├── hooks/
│ └── utils/
│
├── server/
│ ├── config/
│ ├── controllers/
│ ├── middleware/
│ ├── models/
│ ├── routes/
│ ├── services/
│ ├── sockets/
│ └── utils/
│
└── README.md

```
---

## 🔐 Environment Variables

### Server (.env)
```
NODE_ENV=development
PORT=5000
MONGO_URI=mongodb://localhost:27017/localservices
JWT_SECRET=your_secret_key
JWT_EXPIRE=30d

RAZORPAY_KEY_ID=your_key
RAZORPAY_KEY_SECRET=your_secret

GOOGLE_MAPS_API_KEY=your_maps_key
CLIENT_URL=http://localhost:5173
```
### Client (.env)
```
VITE_API_URL=http://localhost:5000/api
VITE_GOOGLE_MAPS_API_KEY=your_maps_key
```

---

## 🔧 Installation

### 1️⃣ Clone Repository
```
git clone https://github.com/yourusername/local-service-booking.git
cd local-service-booking
```
---

### 2️⃣ Install Dependencies

Backend:
```
cd server
npm install
```

Frontend:
```
cd ../client
npm install
```

---

## 🚀 Running the Application

### Start MongoDB
```
mongod
```

### Start Backend
```
cd server
npm run dev
```

### Start Frontend
```
cd client
npm run dev
```

Open:
```
http://localhost:5173
```
---

## 📡 Core API Endpoints

### Authentication

POST /api/auth/register
POST /api/auth/login
GET /api/auth/me


### Services

GET /api/services
GET /api/services/:id


### Booking

POST /api/bookings/request
PUT /api/bookings/:id/accept
PUT /api/bookings/:id/status
GET /api/bookings/user

### Providers
GET /api/providers/nearby


### Payment
POST /api/payment/create
POST /api/payment/verify


### Admin
GET /api/admin/stats
GET /api/admin/users
PUT /api/admin/providers/:id/approve


---

---

## 🔐 Security Features

- JWT Authentication  
- Role-based access control  
- Password hashing (bcrypt)  
- Secure payment verification  
- CORS configuration  
- Protected routes  
- Environment variable protection  

---

## 📱 Responsive Design

Optimized for:

- Desktop  
- Laptop  
- Tablet  
- Mobile  

---

## 🤝 Contributing

1. Fork repository  
2. Create branch  
