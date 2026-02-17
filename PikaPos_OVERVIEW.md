# Restaurant POS System

A comprehensive Point of Sale (POS) system designed for restaurants and food service businesses, featuring real-time order management, inventory tracking, and multi-device synchronization.

## 🏗️ Architecture

### Frontend (React + TypeScript)
- **Framework**: React 18 with TypeScript
- **Styling**: TailwindCSS
- **State Management**: React Context API
- **Real-time**: Socket.IO Client
- **UI Components**: Custom components with Lucide React icons
- **Build Tool**: Vite

### Backend (Node.js + Express)
- **Runtime**: Node.js with ES Modules
- **Framework**: Express.js
- **Database**: PostgreSQL
- **Real-time**: Socket.IO
- **File Upload**: Multer
- **Error Tracking**: Sentry
- **Printing**: Thermal printer integration

## 🚀 Features

### Core POS Functionality
- **Order Management**: Real-time order taking and table management
- **Menu Management**: Categories, items, pricing, and inventory tracking
- **User Management**: Role-based access control (Admin, Staff)
- **Receipt Printing**: Automatic receipt and order ticket printing

### Advanced Features
- **Inventory Management**: Stock tracking, supplies, waste management, and automatic stock updates
- **Operational Day Management**: Configurable business day start hours (e.g., 5 AM)
- **Multi-device Sync**: Real-time synchronization across all connected devices
- **Reporting**: Advanced reports with sales, supplies, expenses, and profit calculations
- **Supplier Management**: Track suppliers, invoices, and purchase history
- **Worker Management**: Employee information and salary tracking

### Data Management
- **CSV Import/Export**: Menu items and data import functionality
- **Excel Export**: Advanced reporting with Excel export
- **Backup & Recovery**: Database setup and migration scripts
- **Audit Trail**: Complete history tracking for all transactions

## 📱 User Interface

### Main Screens
1. **Tables Screen**: Visual table layout and order management
2. **Sales Screen**: Sales history and transaction management
3. **Reports Screen**: Financial reports and analytics
4. **Menu Management**: Item and category management
5. **Stock Management**: Inventory and supply tracking
6. **Settings**: System configuration and user management

### Key UI Features
- **Responsive Design**: Works on tablets, desktops, and mobile devices
- **Real-time Updates**: Instant synchronization across all devices
- **Drag & Drop**: Table transfers and menu reordering
- **Dark/Light Mode**: Theme switching capability

## 🔧 Technical Implementation

### Database Schema
- **Users**: Authentication and role management
- **Sales**: Transaction records with dual bookkeeping
- **Menu Items**: Product catalog with inventory tracking
- **Stock Movements**: Inventory transaction history
- **Active Orders**: Real-time order state management
- **Settings**: System configuration
- **Suppliers**: Vendor management
- **Workers**: Employee management

### API Endpoints

#### Core Operations
- `POST /api/login` - User authentication
- `GET /api/bootstrap` - Initial data load
- `GET /api/sales` - Sales data with date filtering
- `POST /api/sales` - Create new sales transaction

#### Menu Management
- `GET /api/menu-items` - Retrieve menu items
- `POST /api/menu-items` - Create new menu item
- `PUT /api/menu-items/:id` - Update menu item
- `DELETE /api/menu-items/:id` - Soft delete menu item

#### Inventory
- `POST /api/stock/bulk-update` - Bulk stock updates
- `GET /api/stock/supply-history` - Supply history
- `POST /api/stock/waste` - Record waste/loss

#### Reports
- `GET /api/reports/advanced` - Advanced financial reports
- `GET /api/expenses` - Expense tracking

### Real-time Features

#### Socket.IO Events
- `client-order-update` - Real-time order synchronization
- `print-order-ticket` - Order ticket printing
- `print-sale-receipt` - Receipt printing
- `sale-finalized-from-server` - Sale notifications
- `active-orders-updated` - Order state broadcasts

## 🛠️ Development Setup

### Prerequisites
- Node.js 18+
- PostgreSQL 12+
- npm or yarn

### Installation
```bash
# Clone the repository
git clone <repository-url>
cd PikaPos

# Install dependencies
npm install

# Set up environment variables
cp .env.example .env.local
# Configure database connection and other settings

# Run database migrations
npm run db-setup

# Start development server
npm run dev
```

## 📊 Business Logic

### Operational Day Management
- Configurable start hour (default: 5 AM)
- Orders before start hour belong to previous business day
- Consistent across all reporting and sales functions

### Inventory Management
- **Stock Groups**: Shared inventory across related items
- **Automatic Updates**: Stock decreases on sales, increases on supplies
- **Weighted Average Cost**: Automatic cost calculation for supplies
- **Waste Tracking**: Record and track inventory loss
- **Supplier Management**: Track purchases and invoices

### Order Processing
- **Real-time Sync**: All devices see order changes instantly
- **Table Management**: Visual table layout with status indicators
- **Order Transfers**: Move orders between tables (full or partial)
- **Payment Processing**: Support for different payment methods
- **Receipt Generation**: Automatic fiscal and internal receipts

## 🔒 Security Features

- **Role-based Access Control**: Admin and staff roles
- **PIN Authentication**: Secure user login
- **Data Validation**: Input sanitization and validation
- **Error Tracking**: Sentry integration for error monitoring
- **Database Security**: Parameterized queries to prevent SQL injection

## 🖨️ Hardware Integration

- **Thermal Printers**: Order tickets and receipts
- **Kitchen Printers**: Separate printing for different areas
- **Bar Printers**: Bar area specific printing
- **Automatic Printing**: Configurable print triggers

## 📈 Reporting & Analytics

### Financial Reports
- **Sales Reports**: Daily, weekly, monthly, yearly sales data
- **Profit Analysis**: Calculate profit from sales, supplies, and expenses
- **Tax Reporting**: VAT and tax calculation support

### Inventory Reports
- **Stock Levels**: Current inventory status
- **Supply History**: Purchase tracking and costing
- **Waste Reports**: Inventory loss analysis
- **Movement History**: Complete inventory transaction log

## 🚀 Deployment

### Production Setup
```bash
# Build the application
npm run build

# Set production environment
export NODE_ENV=production

# Start the server
npm start
```

### Docker Support
- Dockerfile included for containerized deployment
- Environment-based configuration
- Database connection management

## 🔄 Data Flow

1. **Order Creation**: Staff create orders via tablet interface
2. **Real-time Sync**: Orders sync to all connected devices
3. **Kitchen Printing**: Order tickets print automatically
4. **Inventory Update**: Stock levels decrease in real-time
5. **Reporting**: Data available for business analytics

## 🎯 Target Users

- **Restaurant Owners**: Business analytics and reporting
- **Managers**: Staff management and inventory control
- **Waitstaff**: Order taking and table management
- **Kitchen Staff**: Order preparation and timing
- **Accountants**: Financial reporting and tax compliance

## 📋 Future Enhancements

- **Mobile App**: Native mobile application
- **Online Ordering**: Customer-facing ordering portal
- **Delivery Management**: Delivery tracking and management
- **Loyalty Programs**: Customer loyalty and rewards
- **Advanced Analytics**: AI-powered business insights
- **Multi-location Support**: Chain restaurant management

## 📞 Support

For technical support or questions:
- Check the documentation
- Review the error logs
- Contact the development team

---

*This POS system is designed to streamline restaurant operations, provide comprehensive business insights, and ensure compliance with local fiscal requirements.*
