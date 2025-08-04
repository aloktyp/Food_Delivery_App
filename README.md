# Food Ordering Web App (MERN Stack)

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage](#usage)
- [Screenshots](#screenshots)
- [API Documentation](#api-documentation)
- [Contributing](#contributing)
- [Contact](#contact)

## Introduction
This is a full-stack food ordering web application built using the MERN stack (MongoDB, Express, React, Node.js). The application consists of a customer-facing app for ordering food and an admin app for managing orders, menu items, and more.

## Features
- User authentication and authorization
- Browse food items
- Add items to the cart and place orders
- Stripe Payment Integration: Secure and reliable payment processing using Stripe.
- Order tracking
- Admin panel to manage menu items, orders

## Technologies Used
- **Frontend:** React.js, React Context API, React Router
- **Backend:** Node.js, Express.js
- **Payment Gateway:** Stripe
- **Database:** MongoDB
- **Authentication:** JWT (JSON Web Tokens)
- **Styling:** CSS

## Installation
### Prerequisites
- Node.js
- MongoDB

### Clone the Repository
```sh
git clone 
cd mern-food-delivery-app
```

## Deployment

This project is deployed on Render with the following services:

### Backend Deployment
- **Service Type:** Web Service
- **Root Directory:** `backend`
- **Build Command:** `npm install`
- **Start Command:** `npm run server`
- **Environment Variables:**
  - `JWT_SECRET`: Your JWT secret key
  - `STRIPE_SECRET_KEY`: Your Stripe secret key
  - `MONGODB_URI`: Your MongoDB connection string

### Frontend Deployment
- **Service Type:** Static Site
- **Root Directory:** `frontend`
- **Build Command:** `npm install && npm run build`
- **Publish Directory:** `dist`
- **Environment Variables:**
  - `VITE_BACKEND_URL`: `https://food-delivery-app-backend-sixo.onrender.com`

### Admin Deployment
- **Service Type:** Static Site
- **Root Directory:** `admin`
- **Build Command:** `npm install && npm run build`
- **Publish Directory:** `dist`
- **Environment Variables:**
  - `VITE_BACKEND_URL`: `https://food-delivery-app-backend-sixo.onrender.com`

## Backend Setup
Navigate to the backend directory:

```sh
cd backend

```
Install dependencies:

```sh
npm install
```

Create a .env file in the backend directory and add the following:

```sh
JWT_SECRET="your_jwt_secret"
STRIPE_SECRET_KEY=your_stripe_secret_key
```

Start the backend server:

```sh
npm run server
```
## Frontend Setup
Navigate to the frontend directory:

```sh

cd frontend
```

Install dependencies:
```sh

npm install
```

Start the frontend server:
```sh

npm run dev
```

## Admin App Setup

Navigate to the admin directory:
```sh

cd admin
```

Install dependencies:

```sh
npm install
```

Start the admin app :
```sh
npm run dev
```

## Usage

### Live Applications
- **Frontend (Customer App):** [https://food-delivery-app-frontend-xo7g.onrender.com](https://food-delivery-app-frontend-xo7g.onrender.com)
- **Admin Panel:** [https://food-delivery-app-admin-78z0.onrender.com](https://food-delivery-app-admin-78z0.onrender.com)
- **Backend API:** [https://food-delivery-app-backend-sixo.onrender.com](https://food-delivery-app-backend-sixo.onrender.com)

### Local Development
- Frontend: http://localhost:5173
- Admin: http://localhost:5174
- Backend: http://localhost:4000

### How to Use
1. Register as a new user or log in with existing credentials
2. Browse the menu, add items to the cart, and place an order
3. Pay using dummy visa card
4. Use the admin panel to manage orders, menu items


## API Documentation
The API endpoints for the backend can be documented using tools like Postman or Swagger. Include endpoints for user authentication, menu items, orders, and more.

## Contributing
Contributions are welcome! Please fork the repository and create a pull request with your changes. Make sure to follow the code style and include relevant tests.

## Contact
For any questions or suggestions, feel free to contact me.

Happy coding!

Feel free to customize this template according to your specific project details and requirements.




