MERN Stack E-commerce Web Application
Project Overview

This is a full-stack E-commerce web application built using the MERN stack (MongoDB, Express.js, React.js, Node.js).
The application allows users to browse products, add them to a shopping cart, and place orders. Admins can manage products, view orders, and monitor users.

Features
User Features

User registration and login with JWT-based authentication

Browse products with categories, search, and filters

View product details with images, price, and description

Add, remove, and update items in shopping cart

Place orders and view order history

Admin Features

Add, update, and delete products

View all orders and update order status

Manage users and monitor activity

Technologies Used
Layer	Technology
Frontend	React.js, React Router, Redux / Context API
Backend	Node.js, Express.js
Database	MongoDB, Mongoose
Authentication	JWT, bcrypt
Styling	CSS / TailwindCSS / Bootstrap
Payment Integration	Stripe / PayPal (optional)
Project Structure
mern-ecommerce/
│
├── backend/
│   ├── models/       # Database schemas
│   ├── routes/       # API routes
│   ├── controllers/  # Business logic
│   └── server.js     # Entry point for backend
│
└── frontend/
    ├── src/
    │   ├── components/  # Reusable UI components
    │   ├── pages/       # Application pages (Home, Product, Cart)
    │   ├── redux/       # State management (Redux)
    │   └── App.js       # Main frontend entry

Installation and Setup
Backend

Navigate to backend folder:

cd backend


Install dependencies:

npm install


Create a .env file and add:

MONGO_URI=<your_mongodb_connection_string>
JWT_SECRET=<your_jwt_secret_key>


Start the backend server:

npm run dev

Frontend

Navigate to frontend folder:

cd frontend


Install dependencies:

npm install


Start the frontend server:

npm start

API Endpoints
Users

POST /api/users/register – Register new user

POST /api/users/login – User login

GET /api/users/profile – Get user profile (protected)

Products

GET /api/products – Get all products

GET /api/products/:id – Get single product details

POST /api/products – Add product (admin only)

PUT /api/products/:id – Update product (admin only)

DELETE /api/products/:id – Delete product (admin only)

Orders

POST /api/orders – Create a new order

GET /api/orders/myorders – Get logged-in user orders

GET /api/orders – Get all orders (admin only)

Future Enhancements

Payment gateway integration (Stripe / PayPal)

Product reviews and ratings

Wishlist functionality

Real-time notifications for orders

Responsive mobile-first design
