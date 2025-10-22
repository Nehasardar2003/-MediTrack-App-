# Medicine Expiry Tracking System 💊

A comprehensive Flask-based web application for tracking medicine inventory, expiry dates, sales, and stock management with real-time alerts and reporting.

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Flask](https://img.shields.io/badge/Flask-2.3.3-green)
![SQLite](https://img.shields.io/badge/SQLite-Database-lightgrey)
![Bootstrap](https://img.shields.io/badge/Bootstrap-5.1.3-purple)

## 🌟 Features

### 🔐 Authentication & Security
- User registration and login system
- Password hashing with Werkzeug
- Alphanumeric password validation (8+ characters)
- Session-based authentication

### 💊 Medicine Management
- Add, edit, and delete medicines
- Categorization (Tablet, Syrup, Capsule, Ointment, etc.)
- Batch number tracking
- Price and quantity management
- Expiry date validation

### ⏰ Smart Alerts & Monitoring
- **Expiry Alerts**: Medicines expiring within 30 days
- **Low Stock Alerts**: Configurable threshold-based alerts
- **Expired Medicines**: Automatic tracking and separate reporting
- Real-time dashboard with overview statistics

### 📊 Stock & Sales Management
- Stock in/out transactions
- Sales recording with customer details
- Complete transaction history
- Stock value calculations in Indian Rupees (₹)

### 🔍 Advanced Search & Filtering
- Search medicines by name
- Filter by medicine categories
- Combined search and filter options

### 📈 Reporting & Analytics
- Dashboard with key metrics
- Sales history and reports
- Expired medicines report
- Stock value calculations

## 🚀 Quick Start

### Prerequisites
- Python 3.8 or higher
- pip (Python package manager)

### Installation

1. **Clone the repository**
git clone https://github.com/yourusername/medicine-expiry-tracker.git
cd medicine-expiry-tracker

2. **Create virtual environment (Recommended)**
python -m venv venv
# On Windows:
venv\Scripts\activate
# On Mac/Linux:
source venv/bin/activate

3. **Install dependencies**
pip install -r requirements.txt

4. **Run the application**
python app.py

5. **Access the application**
Open your browser and navigate to http://localhost:5000

First Time Setup
Register a new account

Login with your credentials

Start adding medicines to your inventory

### Project Structure
medicine-expiry-tracker/
├── app.py                 # Main Flask application
├── database.py           # Database configuration
├── models.py            # SQLAlchemy models
├── requirements.txt     # Python dependencies
├── templates/           # HTML templates
│   ├── base.html
│   ├── login.html
│   ├── signup.html
│   ├── dashboard.html
│   ├── medicines.html
│   ├── add_medicine.html
│   ├── edit_medicine.html
│   ├── sell_medicine.html
│   ├── sales.html
│   ├── transactions.html
│   └── expired_medicines.html
└── static/              # Static files
    ├── style.css
    └── script.js

🗄️ Database Schema
### Entities:
User: User accounts and authentication

Medicine: Medicine inventory with categories

Transaction: Stock movement history

Sale: Sales records with customer details

ExpiredMedicine: Automatic expired medicine tracking

🛠️ Technology Stack
Backend: Python, Flask, SQLAlchemy

Database: SQLite

Frontend: HTML5, CSS3, JavaScript, Bootstrap 5

Authentication: Flask-Login

Security: Werkzeug password hashing

🔧 Configuration
Environment Variables
Create a .env file for configuration:

env
SECRET_KEY=your-secret-key-here
DATABASE_URI=sqlite:///medicine_tracker.db
Default Categories
Tablet

Syrup

Capsule

Ointment

Injection

Drops

Inhaler

Cream

Gel

Powder

📊 Features in Detail
Dashboard
Total medicines count

Stock value in ₹

Today's sales

Expiring soon alerts

Low stock alerts

Expired medicines count

Medicine Management
Complete CRUD operations

Category-based organization

Batch number tracking

Expiry date validation

Low stock threshold setting

Sales & Transactions
Complete sales recording

Customer information tracking

Stock movement history

Financial reporting

Alerts System
Visual status indicators

Color-coded badges

Modal notifications

Dashboard summaries

🐛 Troubleshooting
Common Issues
Database errors after updates

bash
# Reset the database
python reset_db.py
Module not found errors

bash
# Reinstall dependencies
pip install -r requirements.txt
Port already in use

bash
# Use different port
python app.py --port 5001
Reset Database
bash
# Delete existing database and create new
python reset_with_sample.py
🤝 Contributing
Fork the repository

Create a feature branch (git checkout -b feature/AmazingFeature)

Commit your changes (git commit -m 'Add some AmazingFeature')

Push to the branch (git push origin feature/AmazingFeature)

Open a Pull Request

📝 License
This project is licensed under the MIT License - see the LICENSE file for details.

👥 Authors
Your Name - GitHub Profile

🙏 Acknowledgments
Flask community for excellent documentation

Bootstrap for responsive UI components

Font Awesome for icons

SQLAlchemy for ORM capabilities

📞 Support
If you have any questions or issues, please open an issue on GitHub or contact your-email@example.com
