

# V FOOD-ORDER-APP-MAS

## Project Overview

`V FOOD-ORDER-APP-MAS` is a comprehensive food ordering application that includes a **client-side** (Vue.js) for customers, an **admin panel** for restaurant management, and a **Node.js backend** with MongoDB integration. The project supports multiple features like product management, order processing, authentication, and Razorpay integration for payments.

## Project Structure

```
V FOOD-ORDER-APP-MAS/
├── .env                         # Environment variables
├── .gitignore                   # Git ignore file
├── babel.config.js              # Babel configuration
├── nodemon.json                 # Nodemon configuration
├── package.json                 # Project dependencies
├── README.md                    # Project documentation (this file)
├── vue.config.js                # Vue CLI configuration
│
├── client/                      # Frontend (Vue.js)
│   ├── public/                  # Static assets
│   └── src/                     # Vue.js source files
│
├── config/                      # Backend configuration
│   ├── admin.js                 # Admin configuration
│   ├── db.js                    # MongoDB connection
│   └── razorpay.js              # Razorpay integration
│
├── middleware/                  # Custom middleware
│   ├── auth.js                  # Authentication middleware
│   └── paginate.js              # Pagination helper
│
├── models/                      # Database models
│   ├── Order.js                 # Order model
│   ├── Product.js               # Product model
│   └── User.js                  # User model
│
├── routes/                      # Express routes
│   ├── admin/                   # Admin routes
│   ├── api/                     # API routes for client
│   └── auth/                    # Authentication routes
│
├── tests/                       # Test cases
│   ├── unit/                    # Unit tests
│   └── integration/             # Integration tests
│
└── server.js                    # Entry point for the backend
```

## Features

- **User Authentication**: JWT-based login and registration.
- **Admin Panel**: Product and order management.
- **Product Catalog**: Browse and search menu items.
- **Order Management**: Place orders, view order status.
- **Payment Integration**: Razorpay for secure transactions.
- **Pagination**: Efficient API responses with pagination.

## Installation

### Prerequisites

- **Node.js** (v14+)
- **MongoDB** (local or MongoDB Atlas)
- **Vue CLI** (for frontend)

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/V-FOOD-ORDER-APP-MAS.git
cd V-FOOD-ORDER-APP-MAS
```

### 2. Set Up Environment Variables

Create a `.env` file in the root directory:

```
# General
PORT=5000

# MongoDB
MONGODB_URI=your_mongodb_connection_string

# JWT Secret
JWT_SECRET=your_jwt_secret

# Razorpay
RAZORPAY_KEY_ID=your_razorpay_key_id
RAZORPAY_SECRET=your_razorpay_secret
```

### 3. Install Backend Dependencies

```bash
npm install
```

### 4. Run the Backend Server

```bash
npm start
# or
npm run dev   # For development with Nodemon
```

### 5. Navigate to the Client Folder and Install Frontend Dependencies

```bash
cd client
npm install
```

### 6. Start the Frontend Server

```bash
npm run serve
```

## API Endpoints

### Authentication

- **POST** `/auth/register`: Register a new user
- **POST** `/auth/login`: Login for existing users

### Products

- **GET** `/api/products`: Fetch all products with pagination
- **POST** `/admin/products`: Create a new product (Admin only)
- **PUT** `/admin/products/:id`: Update product details (Admin only)
- **DELETE** `/admin/products/:id`: Delete a product (Admin only)

### Orders

- **POST** `/api/orders`: Place a new order
- **GET** `/api/orders/:id`: Get order details by ID
- **GET** `/admin/orders`: Get all orders (Admin only)

### Payments

- **POST** `/api/payments/razorpay`: Create a Razorpay order

## MongoDB Setup

If you are using MongoDB locally, make sure MongoDB is running on your system:

```bash
mongod
```

For MongoDB Atlas, use your connection string in the `.env` file.



## Deployment

### Build for Production

```bash
cd client
npm run build
```

### Start Production Server

```bash
npm run start
```

![preview](https://github.com/user-attachments/assets/216cf036-9985-4f46-ad00-cebda4afd586)

## Technologies Used

- **Frontend**: Vue.js, Bootstrap
- **Backend**: Node.js, Express.js
- **Database**: MongoDB, Mongoose
- **Authentication**: JWT
- **Payment Gateway**: Razorpay
- **Testing**: Jest



