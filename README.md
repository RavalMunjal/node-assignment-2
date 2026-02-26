# E-Commerce Product API

This project is a REST API built using Express.js that manages product data for an e-commerce platform using an in-memory JSON array.

The API implements:

- 3 GET routes
- 1 POST route
- 3 PUT routes
- Proper REST principles
- Correct HTTP status codes

No database is used. All data is stored in memory.

---

## Tech Stack

- Node.js
- Express.js
- CORS
- Render (Deployment)
- Postman (API Documentation)

---

## Product Structure

Each product follows this structure:

{
  id: Number,
  name: String,
  category: String,
  price: Number,
  stock: Number,
  rating: Number
}

Example:

{
  "id": 1,
  "name": "Wireless Mouse",
  "category": "Electronics",
  "price": 799,
  "stock": 25,
  "rating": 4.3
}

---

## API Routes

### GET Routes

1. GET /products  
   Returns all products  
   Status: 200

2. GET /products/:id  
   Returns product by ID  
   Status: 200 (if found)  
   Status: 404 (if not found)

3. GET /products/category/:categoryName  
   Returns products by category  
   Status: 200  
   Returns empty array if none found

---

### POST Route

4. POST /products  
   Adds a new product  
   Auto-generates ID  
   Status: 201  
   Returns created product

Example Body:

{
  "name": "Bluetooth Speaker",
  "category": "Electronics",
  "price": 2999,
  "stock": 20,
  "rating": 4.6
}

---

### PUT Routes

5. PUT /products/:id  
   Replaces entire product except ID  
   Status: 200  
   Status: 404 if not found

6. PUT /products/:id/stock  
   Updates only stock value  
   Status: 200  
   Status: 404 if not found

7. PUT /products/:id/price  
   Updates only price value  
   Status: 200  
   Status: 404 if not found

---

## Live Deployment

Render URL:
https://node-assignment-2-tgkk.onrender.com

---

## Postman Documentation

Postman Link:
https://documenter.getpostman.com/view/50840903/2sBXcGFLPA

All 7 routes are documented with sample requests and responses.

---

## How To Run Locally

1. Clone the repository

git clone <your-repo-link>

2. Install dependencies

npm install

3. Start the server

node server.js

Server will run on:
http://localhost:3000

---

## Notes

- Data is stored in-memory
- No validation libraries used
- No authentication
- No database
- Uses correct HTTP status codes (200, 201, 404)
