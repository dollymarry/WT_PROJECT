🌐 Local Service Booking & Tracking System

A full-stack MERN application that connects customers with nearby local service providers (Plumbing, Electrical, Cleaning, HVAC, Painting, etc.) with real-time booking, tracking, and in-app payments.

🚀 Features
👤 Customer

🏠 Browse available local services

🔍 View complete service details & pricing

📍 Location-based booking (15 KM radius matching)

💳 Secure in-app payment

📡 Real-time service tracking

⭐ Rate & review providers

📜 Booking history tracking

🧑‍🔧 Service Provider

📥 Receive nearby booking requests

✅ Accept or reject jobs

📊 Earnings dashboard

📅 Manage availability

🛠 Update service progress

🛡 Admin

👥 Manage customers & providers separately

✔ Approve provider registrations

📊 Monitor bookings & payments

🚨 Security monitoring & logs

📈 Dashboard analytics

⚙ System

🔐 JWT Authentication

🌍 Geospatial search using MongoDB

⚡ Real-time updates with Socket.IO

💰 Distance-based pricing calculation

📱 Fully responsive UI

🛠️ Tech Stack
Frontend:

React.js

React Router

Axios

Context API

Tailwind CSS

Socket.IO Client

Backend:

Node.js

Express.js

MongoDB with Mongoose

JWT Authentication

Socket.IO

Razorpay / Stripe (Payments)

Database:

MongoDB Atlas (Geospatial indexing enabled)

📋 Prerequisites

Before you begin, ensure you have:

Node.js (v16 or higher)

MongoDB (local or Atlas)

npm or yarn

Razorpay or Stripe account (for payments)

Google Maps API key (for location features)

🔧 Installation
1️⃣ Clone the repository
git clone https://github.com/yourusername/local-service-booking.git
cd local-service-booking
2️⃣ Install Dependencies
Backend
cd server
npm install
Frontend
cd ../client
npm install
🔐 Environment Variables
Server (server/.env)

Create a .env file inside the server folder:

NODE_ENV=development
PORT=5000

MONGO_URI=mongodb://localhost:27017/localservices
JWT_SECRET=your_super_secret_key
JWT_EXPIRE=30d

# Payment Gateway
RAZORPAY_KEY_ID=your_key_id
RAZORPAY_KEY_SECRET=your_secret

# OR Stripe
STRIPE_SECRET_KEY=your_stripe_secret

# Maps & Location
GOOGLE_MAPS_API_KEY=your_maps_key

CLIENT_URL=http://localhost:5173
Client (client/.env)

Create a .env file inside the client folder:

VITE_API_URL=http://localhost:5000/api
VITE_GOOGLE_MAPS_API_KEY=your_maps_key
🚀 Running the Application
Development Mode
Terminal 1 – Start MongoDB
mongod
Terminal 2 – Start Backend
cd server
npm run dev
Terminal 3 – Start Frontend
cd client
npm run dev

Application will run at:

http://localhost:5173
🏗 Production Build
cd client
npm run build

cd ../server
npm start
📁 Project Structure
local-service-booking/
├── client/                 # React Frontend
│   ├── public/
│   └── src/
│       ├── routes/
│       ├── pages/
│       │   ├── Landing/
│       │   ├── Auth/
│       │   ├── Customer/
│       │   ├── Provider/
│       │   └── Admin/
│       ├── components/
│       ├── context/
│       ├── services/
│       ├── hooks/
│       └── utils/
│
├── server/                 # Node Backend
│   ├── config/
│   ├── controllers/
│   ├── middleware/
│   ├── models/
│   ├── routes/
│   ├── services/
│   ├── sockets/
│   └── utils/
│
└── README.md
📡 API Endpoints
Authentication
POST   /api/auth/register
POST   /api/auth/login
GET    /api/auth/me
Services
GET    /api/services
GET    /api/services/:id
Booking
POST   /api/bookings/request
PUT    /api/bookings/:id/accept
PUT    /api/bookings/:id/status
GET    /api/bookings/user
Providers
GET    /api/providers/nearby
GET    /api/providers/profile
Payment
POST   /api/payment/create
POST   /api/payment/verify
Admin
GET    /api/admin/stats
GET    /api/admin/users
PUT    /api/admin/providers/:id/approve

🔐 Security Features

JWT Authentication

Role-based authorization

Password hashing with bcrypt

Protected API routes

Secure payment verification

CORS configuration

Environment variable protection

📱 Responsive Design

Optimized for:

Desktop

Laptop

Tablet

Mobile

🐛 Troubleshooting
MongoDB Connection Error

Ensure MongoDB is running

Verify MONGO_URI in .env

Port Already in Use
lsof -ti:5000 | xargs kill -9
Payment Not Working

Verify API keys

Check webhook configuration

🤝 Contributing

Fork the repository

Create feature branch

git checkout -b feature/YourFeature

Commit changes

git commit -m "Add new feature"

Push branch

git push origin feature/YourFeature

Open Pull Request

📄 License

This project is licensed under the MIT License.

👨‍💻 Author

Mohan
AI & Full Stack Developer
B.Tech (AI & ML)

🙏 Acknowledgments

React Documentation

Express.js Documentation

MongoDB Documentation

Socket.IO

Razorpay / Stripe

🚀 Transforming Local Services Digitally

Making service booking transparent, fast, and intelligent.
