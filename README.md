# Café & Restaurant POS System

A comprehensive Point of Sale (POS) system built for cafés and restaurants with React.js frontend and Node.js backend.

## 🎯 Features

### Core Features
- **Income & Expense Tracking** - Add and view financial entries with filtering
- **Inventory Management** - Track stock with low-stock alerts
- **Payment Processing** - Handle cash, card, and QR payments with discounts
- **Sales Reports** - Daily and monthly sales overview with profit analysis
- **Café & Food Ordering** - Customizable orders with add-ons and options
- **Remote Dashboard** - Role-based access (Admin/Staff)
- **Loyalty Points System** - Customer points management

### Technical Features
- **Mock Database** - JSON/in-memory data structure ready for MySQL migration
- **REST API** - Complete backend API with authentication
- **Responsive Design** - Mobile-friendly interface
- **Role-based Access** - Admin and Staff permissions
- **Real-time Updates** - Live inventory and order tracking

## 🚀 Quick Start

### Prerequisites
- Node.js (v14 or higher)
- npm or yarn

### Installation

1. **Clone and setup the project:**
   ```bash
   git clone <repository-url>
   cd SAAS-POS
   npm run install-all
   ```

2. **Start the development servers:**
   ```bash
   npm run dev
   ```

   This will start:
   - Backend server on http://localhost:5000
   - Frontend development server on http://localhost:3000

### Demo Login Credentials

- **Admin Access:**
  - Username: `admin`
  - Password: `admin123`

- **Staff Access:**
  - Username: `staff`
  - Password: `staff123`

## 📁 Project Structure

```
SAAS-POS/
├── server/                 # Node.js Express backend
│   ├── index.js           # Main server file with all routes
│   └── package.json       # Backend dependencies
├── client/                # React TypeScript frontend
│   ├── src/
│   │   ├── components/    # React components
│   │   ├── contexts/      # React contexts (Auth)
│   │   ├── services/      # API service functions
│   │   └── index.css      # TailwindCSS styles
│   └── package.json       # Frontend dependencies
├── package.json           # Root package with dev scripts
└── README.md              # This file
```

## 🏗️ Architecture

### Backend (Node.js + Express)
- **Mock Database**: In-memory arrays simulating database tables
- **JWT Authentication**: Token-based auth with role management
- **RESTful API**: Complete CRUD operations for all entities
- **Modular Design**: Easy to migrate to MySQL with Sequelize/Prisma

### Frontend (React + TypeScript)
- **Component Architecture**: Reusable UI components
- **Context API**: Global state management for authentication
- **React Router**: Client-side routing with protected routes
- **TailwindCSS**: Utility-first CSS framework
- **Axios**: HTTP client with interceptors

## 🛠️ Development

### Available Scripts

#### Root Level
- `npm run dev` - Start both frontend and backend concurrently
- `npm run install-all` - Install dependencies for all projects
- `npm run server` - Start only the backend server
- `npm run client` - Start only the frontend development server

#### Backend (`server/`)
- `npm start` - Start production server
- `npm run dev` - Start development server with nodemon

#### Frontend (`client/`)
- `npm start` - Start development server
- `npm run build` - Build for production
- `npm test` - Run tests

### API Endpoints

#### Authentication
- `POST /api/auth/login` - Login with username/password

#### Products
- `GET /api/products` - Get all products (with category filter)
- `GET /api/products/low-stock` - Get low stock products
- `POST /api/products` - Create new product (Admin only)
- `PUT /api/products/:id` - Update product (Admin only)

#### Transactions
- `GET /api/transactions` - Get transactions (with filters)
- `POST /api/transactions` - Create new transaction

#### Income/Expenses
- `GET /api/income-expenses` - Get income/expense entries
- `POST /api/income-expenses` - Create new entry

#### Orders
- `GET /api/orders` - Get all orders
- `POST /api/orders` - Create new order
- `PUT /api/orders/:id/status` - Update order status

#### Customers
- `GET /api/customers` - Get all customers
- `GET /api/customers/search` - Search by phone/member card
- `POST /api/customers` - Create new customer
- `PUT /api/customers/:id/points` - Update loyalty points

#### Reports
- `GET /api/reports/sales-summary?period=daily|monthly` - Get sales summary

## 🎨 UI Components

### Main Views
- **Dashboard** - Overview with key metrics and quick actions
- **POS Terminal** - Product selection, cart, and payment processing
- **Orders** - Order management and status tracking
- **Inventory** - Product management with stock tracking
- **Income/Expense** - Financial tracking with filtering
- **Reports** - Sales analytics and summaries (Admin only)
- **Customers** - Customer and loyalty management

### Key Features
- **Product Customization** - Coffee sizes, sugar levels, food add-ons
- **Payment Processing** - Multiple payment methods with discounts
- **Customer Lookup** - Search by phone or member card
- **Loyalty Points** - Automatic earning and redemption
- **Low Stock Alerts** - Real-time inventory monitoring

## 🔧 Configuration

### Environment Variables

Create a `.env` file in the server directory:

```env
PORT=5000
JWT_SECRET=your-super-secret-jwt-key-change-in-production
```

Create a `.env` file in the client directory:

```env
REACT_APP_API_URL=http://localhost:5000/api
```

## 📱 Mobile Support

The application is fully responsive and works on:
- Desktop computers
- Tablets
- Mobile phones
- Touch screen POS terminals

## 🔒 Security Features

- JWT token authentication
- Role-based access control
- Protected API routes
- Input validation
- CORS configuration

## 🚀 Deployment

### Backend Deployment
1. Set production environment variables
2. Run `npm start` in the server directory
3. Ensure proper firewall and security configurations

### Frontend Deployment
1. Update API URL in environment variables
2. Run `npm run build` in the client directory
3. Serve the `build` folder using a web server

## 🔄 Migration to Production Database

The codebase is structured to easily migrate from mock data to a real database:

1. **Install ORM**: Add Sequelize or Prisma
2. **Replace Mock Data**: Convert in-memory arrays to database models
3. **Update API Logic**: Replace direct array manipulation with ORM queries
4. **Environment Configuration**: Add database connection settings

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## 📄 License

This project is licensed under the MIT License.

## 📞 Support

For support and questions, please create an issue in the repository.

---

**Note**: This is a development version with mock data. For production use, implement proper database integration and security measures.