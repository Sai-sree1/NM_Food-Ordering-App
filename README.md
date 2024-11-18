
# MERN-RESTAURANT-APP

## Project Overview
**MERN-RESTAURANT-APP** is a comprehensive full-stack restaurant application built using Next.js (a React framework), Node.js, Express.js, and MongoDB. The project includes a server setup with Node.js for backend functionality and TailwindCSS for modern and responsive styling. 

## Project Structure
```
MERN-RESTAURANT-APP/
├── .env                         # Environment variables
├── .gitignore                   # Git ignore file
├── README.md                    # Project documentation (this file)
│
├── backend/                     # Backend (Node.js, Express.js)
│   ├── config/                  # Backend configuration
│   ├── controllers/             # Route controllers
│   ├── models/                  # Database models (MongoDB)
│   ├── routes/                  # API routes
│   └── server.js                # Entry point for the backend
│
├── frontend/                    # Frontend (Next.js)
│   ├── public/                  # Static assets
│   ├── pages/                   # Next.js pages
│   ├── components/              # Reusable components
│   ├── styles/                  # CSS and Tailwind styles
│   └── next.config.js           # Next.js configuration
```

## Features
- **User Authentication**: Secure login and registration with JWT.
- **Product Catalog**: Browse and search for restaurant menu items.
- **Order Management**: Place and track orders.
- **Admin Panel**: Manage menu items and orders.
- **Responsive Design**: Modern UI with TailwindCSS.
- **Database Management**: MongoDB for storing product and order details.
  
## Installation

### Prerequisites
- **Node.js** (v14+)
- **MongoDB** (local or MongoDB Atlas)
- **Next.js** (for frontend)

### 1. Clone the Repository
```bash
git clone https://github.com/your-repository-link/MERN-Restaurant-App.git
cd MERN-RESTAURANT-APP
```

### 2. Set Up Environment Variables
Create a `.env` file in the root directory:

```plaintext
# General
PORT=5000

# MongoDB
MONGODB_URI=your_mongodb_connection_string

# JWT Secret
JWT_SECRET=your_jwt_secret
```

### 3. Install Backend Dependencies
```bash
cd backend
npm install
```

### 4. Run the Backend Server
```bash
npm start
# or
npm run dev   # For development with Nodemon
```

### 5. Navigate to the Frontend Folder and Install Dependencies
```bash
cd ../frontend
npm install
```

### 6. Start the Frontend Server
```bash
npm run dev
```

## API Endpoints

### Authentication
- **POST** `/api/auth/register`: Register a new user
- **POST** `/api/auth/login`: Login for existing users

### Products
- **GET** `/api/products`: Fetch all products
- **POST** `/api/products`: Create a new product (Admin only)
- **PUT** `/api/products/:id`: Update product details (Admin only)
- **DELETE** `/api/products/:id`: Delete a product (Admin only)

### Orders
- **POST** `/api/orders`: Place a new order
- **GET** `/api/orders/:id`: Get order details by ID
- **GET** `/api/admin/orders`: Get all orders (Admin only)

## MongoDB Setup
For a local setup, ensure MongoDB is running:

```bash
mongod
```

For **MongoDB Atlas**, use your connection string in the `.env` file.

## Deployment

### Build for Production
```bash
cd frontend
npm run build
```

### Start Production Server
```bash
npm run start
```

## Output

![Screenshot (19)](https://github.com/user-attachments/assets/86183ed7-91a5-4304-a408-2629ccd919c3)
![Screenshot (18)](https://github.com/user-attachments/assets/2b5a6be8-e5ee-4041-b739-3fb09b7a8cc7)
![Screenshot (21)](https://github.com/user-attachments/assets/006e230a-b651-47d8-939e-b827800a3377)
![Screenshot (20)](https://github.com/user-attachments/assets/c5b0b2f8-7da1-43b6-95f2-4634ac267013)


## Technologies Used
- **Frontend**: Next.js, TailwindCSS
- **Backend**: Node.js, Express.js
- **Database**: MongoDB, Mongoose
- **Authentication**: JWT
- **Testing**: Jest







