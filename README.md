E-Commerce Application
Description
This is a full-stack e-commerce application built using the MERN stack (MongoDB, Express, React, Node.js). The application includes user authentication, product listing, and a shopping cart functionality. Additionally, it supports product management for admin users and order management.

Features
User registration and login with JWT authentication
Product listing with detailed view
Shopping cart management
Admin functionality for product management (add, update, delete)
Order management (create, view order history, order details)
Product search and filtering
Persistent shopping cart using local storage
Technologies Used
Backend: Node.js, Express, MongoDB
Frontend: React, Redux, React Router
Authentication: JWT (JSON Web Token)
State Management: Redux
Installation
Prerequisites
Node.js and npm
MongoDB
Backend Setup
Clone the repository:

bash
Copy code
git clone https://github.com/your-username/e-commerce-app.git
cd e-commerce-app
Install backend dependencies:

bash
Copy code
cd server
npm install
Create a .env file in the server directory and add the following environment variables:

env
Copy code
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
Start the backend server:

bash
Copy code
npm run dev
Frontend Setup
Install frontend dependencies:

bash
Copy code
cd client
npm install
Start the frontend server:

bash
Copy code
npm start
API Endpoints
User Authentication
POST /api/users/register: Register a new user
POST /api/users/login: Authenticate a user and return a JWT
Product Management
GET /api/products: Retrieve a list of products
GET /api/products/:id: Retrieve details of a specific product
POST /api/products: Add a new product (admin only)
PUT /api/products/:id: Update an existing product (admin only)
DELETE /api/products/:id: Delete a product (admin only)
Shopping Cart
GET /api/cart: Retrieve the user's shopping cart
POST /api/cart: Add an item to the cart
DELETE /api/cart/:id: Remove an item from the cart
Order Management
POST /api/orders: Create a new order
GET /api/orders/myorders: Retrieve the logged-in user's orders
GET /api/orders/:id: Retrieve details of a specific order
PUT /api/orders/:id/pay: Update order to paid
Frontend Components
AuthForm: Registration and login forms
ProductList: Display a list of products
ProductDetail: Display details of a selected product
Cart: Display the user's shopping cart and allow item removal
SearchBox: Search for products
State Management
State management is handled using Redux. The main store configuration can be found in client/src/store.js.

Reducers
cartReducer: Manages the state of the shopping cart
userLoginReducer, userRegisterReducer: Manage user authentication state
productListReducer, productDetailsReducer: Manage product list and product details state
Actions
User Actions: src/actions/userActions.js
Product Actions: src/actions/productActions.js
Cart Actions: src/actions/cartActions.js
Running the Application
Start the backend server:

bash
Copy code
cd server
npm run dev
Start the frontend server:

bash
Copy code
cd client
npm start
Contributing
Fork the repository
Create a new branch (git checkout -b feature-branch)
Make your changes
Commit your changes (git commit -m 'Add some feature')
Push to the branch (git push origin feature-branch)
Open a pull request
License
This project is licensed under the MIT License.
