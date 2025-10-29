# 🎁 GoGifts Creations - Full-Stack E-Commerce Platform

A complete, production-ready e-commerce website featuring a modern HTML/CSS/JavaScript frontend with a powerful Node.js/Express backend, MongoDB database, email notifications, admin panel, and AI chatbot assistant.

![Version](https://img.shields.io/badge/version-2.0.0-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![Node](https://img.shields.io/badge/node-%3E%3D14.0.0-brightgreen.svg)
![MongoDB](https://img.shields.io/badge/database-MongoDB-green.svg)

---

## 🌟 Features Overview

### 🎨 Frontend Features
- ✅ **7 Complete Pages** - Home, Products, Product Detail, Cart, Checkout, About, Contact, Login/Register
- ✅ **Fully Responsive** - Beautiful design on mobile, tablet, and desktop
- ✅ **Pure HTML/CSS/JS** - No frameworks, lightweight and fast
- ✅ **Shopping Cart System** - Add/remove items, update quantities, localStorage persistence
- ✅ **User Authentication UI** - Login and registration with form validation
- ✅ **Product Search & Filters** - Real-time search and category filtering
- ✅ **Interactive Maps** - Google Maps integration on contact page
- ✅ **AI Chatbot** - Smart assistant for customer support (NEW! 🤖)
- ✅ **Toast Notifications** - User-friendly feedback messages
- ✅ **AED Currency** - Prices in UAE Dirhams

### ⚙️ Backend Features
- ✅ **RESTful API** - Clean, documented endpoints
- ✅ **MongoDB Database** - Persistent data storage for users, products, and orders
- ✅ **JWT Authentication** - Secure user authentication and authorization
- ✅ **Email Notifications** - Order confirmations sent to customers and admin via Nodemailer
- ✅ **Admin Panel** - Full dashboard for managing products, orders, and users
- ✅ **Password Hashing** - Secure password storage with bcrypt
- ✅ **Order Management** - Complete order lifecycle tracking
- ✅ **Product Management** - CRUD operations for products
- ✅ **Inventory Tracking** - Stock management system

---

## 📁 Project Structure

```
html-version/
├── Frontend Files
│   ├── index.html              # Home page with hero & featured products
│   ├── products.html           # Product catalog with filters
│   ├── product-detail.html     # Individual product view
│   ├── cart.html               # Shopping cart
│   ├── checkout.html           # Checkout form
│   ├── login.html              # Login/Register page
│   ├── about.html              # About us
│   ├── contact.html            # Contact form with Google Maps
│   ├── styles.css              # Main stylesheet
│   ├── script.js               # Frontend JavaScript
│   ├── config.js               # API configuration
│   │
│   ├── Chatbot (NEW!)
│   ├── chatbot.css             # Chatbot styles
│   ├── chatbot.js              # Chatbot functionality
│   └── CHATBOT_INTEGRATION.md  # Integration guide
│
└── backend/
    ├── server.js               # Express server entry point
    ├── package.json            # Dependencies
    ├── seedDatabase.js         # Database seeder
    │
    ├── config/
    │   └── db.js               # MongoDB connection
    │
    ├── models/
    │   ├── User.js             # User schema
    │   ├── Product.js          # Product schema
    │   └── Order.js            # Order schema
    │
    ├── routes/
    │   ├── auth.js             # Authentication routes
    │   ├── products.js         # Product routes
    │   ├── orders.js           # Order routes
    │   ├── contact.js          # Contact form route
    │   └── admin.js            # Admin routes
    │
    ├── services/
    │   └── emailService.js     # Email sending service
    │
    └── admin/
        ├── index.html          # Admin dashboard UI
        └── admin.js            # Admin JavaScript
```

---

## 🚀 Quick Start Guide

### Prerequisites

Before you begin, ensure you have the following installed:

- **Node.js** (v14 or higher) - [Download here](https://nodejs.org/)
- **MongoDB** - Local installation OR [MongoDB Atlas](https://www.mongodb.com/cloud/atlas) (free tier)
- **Email Account** - Gmail recommended for testing email notifications

### Step 1: Clone or Download

```bash
# Navigate to the html-version directory
cd html-version
```

### Step 2: Backend Setup

```bash
# Navigate to backend directory
cd backend

# Install dependencies
npm install

# Create environment configuration file
# Copy the example below or create .env manually
```

Create a `.env` file in the `backend/` directory:

```env
# Server Configuration
PORT=5000
NODE_ENV=development

# MongoDB Configuration
MONGODB_URI=mongodb://localhost:27017/gogifts
# OR for MongoDB Atlas:
# MONGODB_URI=mongodb+srv://username:password@cluster.mongodb.net/gogifts

# JWT Secret (change this to a random string)
JWT_SECRET=your-super-secret-jwt-key-change-this-in-production

# Email Configuration (Gmail example)
EMAIL_HOST=smtp.gmail.com
EMAIL_PORT=587
EMAIL_USER=your-email@gmail.com
EMAIL_PASS=your-app-specific-password
EMAIL_FROM=GoGifts Creations <your-email@gmail.com>

# Admin Configuration
ADMIN_EMAIL=admin@gogifts.com
ADMIN_PASSWORD=admin123
ADMIN_PANEL_USERNAME=admin
ADMIN_PANEL_PASSWORD=admin123

# Business Email (receives order notifications)
BUSINESS_EMAIL=owner@gogifts.com
```

**Important Email Setup Notes:**
- For Gmail, you need to create an [App Password](https://support.google.com/accounts/answer/185833)
- Don't use your regular Gmail password
- Enable 2-Step Verification first, then create App Password

```bash
# Seed the database with sample products
npm run seed

# Start the backend server
npm start
```

You should see:
```
✅ MongoDB connected successfully
🚀 Server running on port 5000
```

### Step 3: Frontend Setup

Open a new terminal window:

```bash
# Navigate back to html-version directory
cd html-version

# Option 1: Using Python (if installed)
python -m http.server 8000
# Then visit: http://localhost:8000

# Option 2: Using Node.js http-server
npx http-server -p 8000
# Then visit: http://localhost:8000

# Option 3: Using VS Code Live Server extension
# Just right-click on index.html and select "Open with Live Server"
```

### Step 4: Access the Application

- **Frontend**: http://localhost:8000
- **Backend API**: http://localhost:5000
- **Admin Panel**: http://localhost:5000/admin

**Admin Login Credentials:**
- Email: `admin@gogifts.com`
- Password: `admin123`

---

## 🤖 AI Chatbot Integration

The website includes a smart AI chatbot assistant! To add it to any page:

### Quick Integration

Add these 2 lines before the closing `</body>` tag:

```html
<link rel="stylesheet" href="chatbot.css">
<script src="chatbot.js"></script>
```

### Chatbot Features

- 💬 Answers product questions
- 📦 Provides shipping information
- 💰 Displays pricing in AED
- 📞 Shares contact details
- 🎯 Quick reply buttons
- 📱 Fully responsive
- ✨ Beautiful animations

See [CHATBOT_INTEGRATION.md](CHATBOT_INTEGRATION.md) for full documentation.

---

## 🎯 Page Descriptions

### 1. Home Page (`index.html`)
- Hero section with call-to-action
- Features showcase
- Featured products grid
- Newsletter signup
- Customer testimonials

### 2. Products Page (`products.html`)
- All products with images
- Search functionality
- Category filters
- Product ratings
- Add to cart buttons

### 3. Product Detail (`product-detail.html`)
- Large product images
- Detailed descriptions
- Quantity selector
- Related products
- Customer reviews

### 4. Shopping Cart (`cart.html`)
- Cart items list
- Quantity adjustment
- Remove items
- Order summary
- Free shipping calculator
- Proceed to checkout

### 5. Checkout (`checkout.html`)
- Shipping information form
- Billing information form
- Order summary
- Payment method selection
- Order placement (connects to backend)

### 6. Login/Register (`login.html`)
- Tab-based interface
- User registration form
- Login form
- Form validation
- JWT authentication

### 7. About Page (`about.html`)
- Company story
- Mission and values
- Team information
- Brand identity

### 8. Contact Page (`contact.html`)
- Contact form with validation
- Google Maps integration
- Business hours
- Contact information
- Social media links

---

## 🔌 API Documentation

### Base URL
```
http://localhost:5000/api
```

### Authentication Endpoints

#### Register User
```http
POST /api/auth/register
Content-Type: application/json

{
  "name": "John Doe",
  "email": "john@example.com",
  "password": "password123"
}
```

#### Login
```http
POST /api/auth/login
Content-Type: application/json

{
  "email": "john@example.com",
  "password": "password123"
}
```

### Product Endpoints

#### Get All Products
```http
GET /api/products
```

#### Get Single Product
```http
GET /api/products/:id
```

### Order Endpoints

#### Create Order
```http
POST /api/orders
Authorization: Bearer {token}
Content-Type: application/json

{
  "items": [
    {
      "product": "product_id",
      "quantity": 2,
      "price": 110
    }
  ],
  "shippingAddress": {
    "fullName": "John Doe",
    "email": "john@example.com",
    "phone": "1234567890",
    "address": "123 Main St",
    "city": "Dubai",
    "country": "UAE"
  },
  "totalAmount": 242
}
```

#### Get User Orders
```http
GET /api/orders
Authorization: Bearer {token}
```

### Contact Endpoint

#### Submit Contact Form
```http
POST /api/contact
Content-Type: application/json

{
  "name": "John Doe",
  "email": "john@example.com",
  "subject": "Question",
  "message": "Hello..."
}
```

### Admin Endpoints

See [backend/README.md](backend/README.md) for complete admin API documentation.

---

## 🎨 Customization Guide

### Changing Colors

Edit CSS variables in `styles.css`:

```css
:root {
  --primary-color: #db2777;      /* Main brand color */
  --primary-dark: #be185d;       /* Darker shade */
  --secondary-color: #ec4899;    /* Secondary color */
  --text-dark: #1f2937;          /* Dark text */
  --text-gray: #6b7280;          /* Gray text */
  --background: #ffffff;         /* Background */
  --border-color: #e5e7eb;       /* Borders */
}
```

### Changing Currency

The website uses **AED (UAE Dirham)**. To change currency:

1. Update all `AED` text in HTML files to your currency symbol
2. Update product prices in `backend/seedDatabase.js`
3. Update shipping thresholds in `cart.html` and `checkout.html`

### Adding Products

#### Option 1: Via Admin Panel (Recommended)
1. Go to http://localhost:5000/admin
2. Login with admin credentials
3. Navigate to "Products" tab
4. Click "Add New Product"
5. Fill in product details

#### Option 2: Via Database Seeder
Edit `backend/seedDatabase.js` and run:
```bash
npm run seed
```

### Changing Email Templates

Edit `backend/services/emailService.js` to customize email templates sent to customers.

---

## 🛠 Technologies Used

### Frontend
- **HTML5** - Semantic markup
- **CSS3** - Modern styling with Grid & Flexbox
- **JavaScript (ES6+)** - Vanilla JS, no frameworks
- **LocalStorage** - Client-side data persistence
- **Google Maps API** - Interactive maps

### Backend
- **Node.js** - JavaScript runtime
- **Express.js** - Web framework
- **MongoDB** - NoSQL database
- **Mongoose** - MongoDB ODM
- **JWT** - Authentication tokens
- **bcrypt** - Password hashing
- **Nodemailer** - Email sending
- **CORS** - Cross-origin resource sharing

---

## 📱 Responsive Design

The website is fully responsive with breakpoints:

- **Mobile**: < 768px
- **Tablet**: 768px - 1023px
- **Desktop**: ≥ 1024px

All pages are optimized for:
- ✅ iPhone/Android phones
- ✅ iPad/Tablets
- ✅ Laptops
- ✅ Desktop monitors

---

## 🔒 Security Features

- ✅ Password hashing with bcrypt
- ✅ JWT token authentication
- ✅ CORS protection
- ✅ Input validation
- ✅ SQL injection prevention (MongoDB)
- ✅ XSS protection
- ✅ Environment variables for secrets

---

## 🧪 Testing

### Test Backend Connection

1. Ensure backend is running on port 5000
2. Visit: http://localhost:5000/api/products
3. You should see JSON array of products

### Test Order Placement

1. Add items to cart on frontend
2. Proceed to checkout
3. Fill in shipping details
4. Click "Place Order"
5. Check console for success message
6. Check admin panel for new order
7. Check email for order confirmation

### Test Admin Panel

1. Visit: http://localhost:5000/admin
2. Login with admin credentials
3. Check orders, products, users tabs
4. Try updating order status
5. Try editing a product

---

## 📧 Email Notifications

When an order is placed, the system sends:

1. **Customer Email** - Order confirmation with details
2. **Admin Email** - New order notification

**Troubleshooting Email Issues:**
- Make sure EMAIL_USER and EMAIL_PASS are correct in .env
- For Gmail, use App Password (not regular password)
- Check spam folder
- Verify EMAIL_FROM format is correct

---

## 🐛 Troubleshooting

### Orders Not Saving?

✅ **Ensure backend is running** on port 5000
✅ **Check MongoDB connection** - should see "MongoDB connected" in terminal
✅ **Verify config.js** has correct API URL
✅ **Check browser console** for errors
✅ **Test API directly** using Postman or browser

### Email Not Sending?

✅ **Check .env file** has correct email credentials
✅ **Use App Password** for Gmail
✅ **Check terminal logs** for email errors
✅ **Verify EMAIL_FROM** format

### Admin Panel Not Loading?

✅ **Backend must be running** on port 5000
✅ **Visit** http://localhost:5000/admin (not localhost:8000)
✅ **Check credentials** in .env file

### Products Not Showing?

✅ **Run database seeder**: `npm run seed`
✅ **Check MongoDB** is running
✅ **Verify MONGODB_URI** in .env

---

## 📦 Database Schema

### User Model
- name (String)
- email (String, unique)
- password (String, hashed)
- createdAt (Date)

### Product Model
- name (String)
- price (Number)
- description (String)
- image (String)
- category (String)
- rating (Number)
- stock (Number)

### Order Model
- user (ObjectId ref User)
- items (Array)
- shippingAddress (Object)
- totalAmount (Number)
- status (String: pending/confirmed/shipped/delivered)
- createdAt (Date)

---

## 🌐 Browser Compatibility

✅ Chrome/Edge (latest)
✅ Firefox (latest)
✅ Safari (latest)
✅ Mobile browsers (iOS Safari, Chrome Mobile)

---

## 📄 Additional Documentation

- **Backend API**: [backend/README.md](backend/README.md)
- **Chatbot Guide**: [CHATBOT_INTEGRATION.md](CHATBOT_INTEGRATION.md)

---

## 🎓 Learning Resources

This project demonstrates:
- Full-stack web development
- RESTful API design
- MongoDB database operations
- User authentication with JWT
- Email integration
- Admin dashboard development
- Responsive web design
- Client-side state management

---

## 📝 License

Free to use for personal and commercial projects.

---

## 🤝 Support

For questions or issues:
- Check the troubleshooting section above
- Review the documentation files
- Contact: info@gogifts.com

---

## 🎉 Credits

**Built with ❤️ for GoGifts Creations**

Special thanks to:
- Unsplash for placeholder images
- Google Maps for location services
- MongoDB for database solutions
- Node.js & Express communities

---

## 🔄 Version History

### v2.0.0 (Current)
- ✅ Added AI Chatbot assistant
- ✅ Converted prices to AED currency
- ✅ MongoDB integration complete
- ✅ Email notifications working
- ✅ Admin panel fully functional
- ✅ Order system operational

### v1.0.0
- Initial release with basic e-commerce features

---

**Happy Selling! 🎁✨**
