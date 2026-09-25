# FarmConnect — Project Requirements

## 1. Project Overview

FarmConnect is an AI-powered digital agricultural marketplace designed to reduce unnecessary intermediaries in the agricultural supply chain.

The platform directly connects farmers and Farmer Producer Organizations (FPOs) with consumers and bulk buyers.

The system also provides logistics support, AI-based demand forecasting, and delivery route optimization.

---

## 2. Problem Statement

Multiple intermediaries between farmers and consumers can reduce the share of the final price received by farmers while increasing the price paid by consumers.

Farmers may also face difficulties in finding direct buyers, predicting future demand, managing inventory, and arranging efficient logistics.

Consumers and bulk buyers may have difficulty finding reliable agricultural suppliers at transparent prices.

FarmConnect aims to address these problems through a centralized digital marketplace.

---

## 3. Proposed Solution

FarmConnect provides a digital platform where:

- Farmers and FPOs can list agricultural products.
- Consumers can directly purchase products from farmers/FPOs.
- Bulk buyers can submit large quantity requirements.
- The platform can match bulk requirements with available farmer/FPO supply.
- Orders and payments can be managed digitally.
- Logistics and delivery information can be managed through the platform.
- AI-based demand forecasting can help estimate future product demand.
- Route optimization can help improve delivery efficiency.
- Dashboards provide useful information to different users.

---

## 4. Main Objectives

1. Connect farmers/FPOs directly with consumers and bulk buyers.
2. Reduce unnecessary supply-chain intermediaries.
3. Improve price transparency.
4. Help farmers reach more buyers.
5. Provide consumers with direct access to agricultural products.
6. Support bulk purchasing.
7. Improve logistics and delivery planning.
8. Forecast future demand using historical data.
9. Optimize delivery routes.
10. Provide useful analytics to farmers and administrators.

---

## 5. Target Users

### 5.1 Farmer / FPO

Farmers and Farmer Producer Organizations can:

- Create an account.
- Manage their profile.
- Add agricultural products.
- Set product prices.
- Specify available quantity.
- Update inventory.
- View incoming orders.
- Manage orders.
- View sales and earnings.
- View demand forecasts.
- Receive recommendations based on predicted demand.

### 5.2 Consumer

Consumers can:

- Create an account.
- Browse agricultural products.
- Search products.
- Filter products.
- View farmer/FPO information.
- View product price and availability.
- Add products to cart.
- Place orders.
- Make payments.
- Track orders.
- View order history.
- Submit reviews.

### 5.3 Bulk Buyer

Bulk buyers may include:

- Restaurants
- Hotels
- Supermarkets
- Hostels
- Canteens
- Food processing businesses
- Other institutional buyers

Bulk buyers can:

- Create an account.
- Search agricultural products.
- Specify required quantities.
- Submit bulk requirements.
- Find matching farmers/FPOs.
- Create bulk orders.
- Track bulk orders.

### 5.4 Administrator

Administrators can:

- Manage users.
- Verify farmers/FPOs.
- Manage products.
- Monitor orders.
- Monitor bulk orders.
- Monitor deliveries.
- Manage reported issues.
- View platform analytics.
- Monitor system activity.

---

# 6. Core Functional Modules

## 6.1 Authentication

The system shall provide:

- User registration.
- User login.
- Secure password storage.
- JWT-based authentication.
- Role-based access control.
- Protected APIs.

Supported roles:

- Farmer/FPO
- Consumer
- Bulk Buyer
- Administrator

---

## 6.2 Farmer/FPO Marketplace

Farmers/FPOs shall be able to:

- Create product listings.
- Update product listings.
- Delete product listings.
- Set prices.
- Specify available quantities.
- Specify product category.
- Specify location.
- View product sales.
- Manage inventory.

Example:

Product: Tomato

Price: ₹28/kg

Available Quantity: 500 kg

Location: Medak, Telangana

Quality: Grade A

---

## 6.3 Product Marketplace

Consumers and bulk buyers shall be able to:

- Browse products.
- Search products.
- Filter by category.
- Filter by price.
- Filter by location.
- View product details.
- View seller information.
- View product availability.

---

## 6.4 Cart and Orders

Consumers shall be able to:

- Add products to cart.
- Update quantities.
- Remove products.
- Checkout.
- Place orders.
- View order status.
- View order history.

Farmers shall be able to:

- View received orders.
- Accept/manage orders.
- Update order status.

---

## 6.5 Bulk Purchasing

Bulk buyers shall be able to specify:

- Product.
- Required quantity.
- Delivery location.
- Required delivery date.

The system shall identify suitable suppliers based on:

- Product availability.
- Quantity.
- Location.
- Seller status.

---

## 6.6 Payment

The platform should support digital payment processing.

The prototype will use a payment gateway in test/sandbox mode.

Payment status should be associated with the corresponding order.

---

## 6.7 Logistics Management

The system shall maintain:

- Pickup location.
- Delivery location.
- Order information.
- Delivery status.
- Assigned delivery information.

The system should support route planning for multiple deliveries.

---

## 6.8 Route Optimization

The system should generate optimized delivery routes using:

- Delivery locations.
- Pickup locations.
- Distance.
- Estimated travel time.
- Vehicle constraints where applicable.

The initial implementation will investigate:

- OpenStreetMap
- OSRM
- Google OR-Tools

The optimized route should be displayed visually on a map.

---

# 7. AI Demand Forecasting

The platform shall provide demand forecasting using historical sales/order data.

Potential input features include:

- Product.
- Date.
- Quantity sold.
- Location.
- Historical demand.
- Price.
- Seasonal information.

The forecasting system should produce future demand estimates.

Example:

Product: Tomato

Predicted demand for next 7 days:

- Day 1: 198 kg
- Day 2: 205 kg
- Day 3: 212 kg
- Day 4: 208 kg
- Day 5: 220 kg
- Day 6: 215 kg
- Day 7: 230 kg

The forecast should be displayed on the farmer dashboard.

---

# 8. Data Strategy

During development, the system may use:

1. Synthetic demonstration data.
2. Public datasets where their use is permitted.
3. Data generated from application transactions.

Synthetic data must be clearly identified as synthetic/demo data.

The system should not claim that synthetic data represents real-world agricultural measurements.

As the platform accumulates real transaction data, historical order information can become a source for future forecasting models.

---

# 9. Price Transparency

The platform should provide transparent product pricing.

Where reliable reference-price data is available, the system may display comparison information such as:

- Farmer/listed price.
- Marketplace price.
- Reference/estimated consumer price.

Any estimated or calculated comparison should be clearly labelled.

---

# 10. Notifications

The system may provide notifications for:

- New orders.
- Order status changes.
- Payment status.
- Delivery updates.
- Bulk order responses.
- Important farmer alerts.

---

# 11. Reviews and Ratings

Consumers may be able to review products and sellers after completed orders.

The system should prevent unauthorized users from creating reviews for orders they did not complete.

---

# 12. Admin Analytics

The administrator dashboard should provide information such as:

- Total users.
- Total farmers/FPOs.
- Total consumers.
- Total bulk buyers.
- Total products.
- Total orders.
- Completed orders.
- Pending orders.
- Sales/transaction value.
- Product demand.
- Active deliveries.

---

# 13. Non-Functional Requirements

## Performance

The application should respond quickly under normal usage.

## Security

The system should implement:

- Password hashing.
- JWT authentication.
- Role-based authorization.
- Input validation.
- Secure API endpoints.
- Environment variables for secrets.
- Proper error handling.

## Scalability

The system should use separated frontend, backend, database, and ML components so that individual components can be improved independently.

## Usability

The interface should be:

- Simple.
- Responsive.
- Mobile-friendly.
- Easy to navigate.

## Reliability

The application should handle API failures and invalid input gracefully.

---

# 14. Proposed Technology Stack

## Frontend

- React
- Vite
- Tailwind CSS
- Recharts
- Leaflet

## Backend

- Node.js
- Express.js
- REST APIs
- JWT
- bcrypt

## Database

- PostgreSQL

## Machine Learning

- Python
- FastAPI
- Pandas
- NumPy
- Scikit-learn
- Appropriate time-series forecasting approach

## Maps and Routing

- OpenStreetMap
- Leaflet
- OSRM
- Google OR-Tools

## Payment

- Razorpay test/sandbox environment

## Development Tools

- Git
- GitHub
- VS Code
- Postman

---

# 15. High-Level Architecture


Users
  |
  v
React Frontend
  |
  v
Node.js + Express Backend
  |
  +-------------------+
  |                   |
  v                   v
PostgreSQL       Python ML Service
                     |
                     v
              Demand Forecasting

Backend
  |
  +--> Maps / OSRM
  |
  +--> OR-Tools
  |
  +--> Payment Gateway

# 16. Initial Database Entities

The planned database entities include:

Users
Farmers
FPOs
Consumers
Bulk Buyers
Products
Categories
Inventory
Orders
Order Items
Bulk Orders
Payments
Deliveries
Routes
Forecasts
Reviews
Notifications

The final database schema will be designed before backend implementation.

# 17. Development Phases
Phase 1 — Planning
Requirements
Architecture
Database design
API design
UI planning
Phase 2 — Authentication
Registration
Login
JWT
Role-based authorization
Phase 3 — Marketplace
Products
Inventory
Search
Filters
Product details
Phase 4 — Orders
Cart
Checkout
Orders
Order status
Phase 5 — Bulk Marketplace
Bulk requirements
Supplier matching
Bulk orders
Phase 6 — Payments
Payment gateway
Payment verification
Payment status
Phase 7 — Logistics
Delivery management
Maps
Route planning
Phase 8 — AI
Dataset preparation
Data preprocessing
Demand forecasting
Forecast API
Dashboard visualization
Phase 9 — Administration
Admin dashboard
Verification
Analytics
Monitoring
Phase 10 — Testing and Deployment
Backend testing
Frontend testing
API testing
Security testing
Deployment
Documentation

# 18. MVP Scope

The initial working version should prioritize:

Authentication
Farmer product management
Marketplace
Consumer orders
Bulk buyer requirements
Basic logistics
Demand forecasting prototype
Route optimization prototype
Admin dashboard

Advanced features can be added after the core system is stable.

# 19. Success Criteria

The project will be considered successful when a complete demonstration can show:

Farmer/FPO
→ Lists product

Consumer
→ Finds product
→ Places order
→ Completes payment

Bulk Buyer
→ Creates bulk requirement
→ Finds suitable suppliers

System
→ Manages delivery
→ Generates optimized route

Historical order data
→ Feeds demand forecasting
→ Produces future demand estimates

Admin
→ Monitors the entire platform

# 20. Project Principle

The project should prioritize solving the agricultural supply-chain problem rather than simply creating an e-commerce interface.

Every major feature should be connected to one of the following goals:

Better farmer market access
Price transparency
Lower supply-chain inefficiency
Better buyer access
Better demand planning
More efficient logistics