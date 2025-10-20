<div align="center">

# 💊 MediTrack-App

### *Your Smart Medicine Management Companion*

[![Python](https://img.shields.io/badge/Python-3.7+-blue.svg)](https://www.python.org/downloads/)
[![Flask](https://img.shields.io/badge/Flask-2.0+-green.svg)](https://flask.palletsprojects.com/)
[![SQLite](https://img.shields.io/badge/SQLite-3-lightgrey.svg)](https://www.sqlite.org/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

**Never let your medicines expire again!** MediTrack-App is an intelligent web application that helps you track medicine expiry dates and sends timely alerts, ensuring your family's health and safety.

[Features](#-key-features) • [Demo](#-demo) • [Installation](#-installation) • [Usage](#-how-to-use) • [Contributing](#-contributing)

---

</div>

## 🎯 Why MediTrack-App?

Have you ever found expired medicine in your cabinet? Or wondered if that pain reliever is still safe to use? **MediTrack-App** solves these problems by:

- 🔔 **Alerting you** before medicines expire
- 📊 **Organizing** your entire medicine cabinet digitally
- 💰 **Saving money** by preventing medicine waste
- 🏥 **Ensuring safety** by tracking expiry dates automatically
- 👨‍👩‍👧‍👦 **Protecting your family** from expired medications

## ✨ Key Features

<table>
<tr>
<td width="50%">

### 📝 Easy Medicine Entry
Add medicines in seconds with an intuitive form. Simply enter the medicine name, type (tablet, syrup, injection), and expiry date.

</td>
<td width="50%">

### 📅 Smart Expiry Tracking
Visual dashboard showing all your medicines with color-coded alerts based on expiry status.

</td>
</tr>
<tr>
<td width="50%">

### 🚨 Automated Alerts
Get instant visual warnings for medicines that are:
- ⚠️ Expiring soon (within 30 days)
- 🔴 Already expired
- ✅ Safe to use

</td>
<td width="50%">

### 💾 Persistent Storage
All your data is safely stored in a local SQLite database. Your medicine list survives system restarts.

</td>
</tr>
<tr>
<td width="50%">

### 🎨 Clean Interface
Beautiful, responsive design that works on desktop, tablet, and mobile devices.

</td>
<td width="50%">

### ⚡ Lightning Fast
Built with Flask for quick loading and smooth performance, even with hundreds of medicines.

</td>
</tr>
</table>

## 🖼️ Demo

*Coming Soon: Screenshots of the application interface*

## 🛠️ Technology Stack

<div align="center">

| Technology | Purpose | Version |
|------------|---------|---------|
| 🐍 **Python** | Backend Programming | 3.7+ |
| 🌶️ **Flask** | Web Framework | 2.0+ |
| 🗄️ **SQLite** | Database | 3.x |
| 🎨 **HTML/CSS/JS** | Frontend Interface | HTML5/CSS3/ES6 |

</div>

## 📦 Installation

### Prerequisites

Before you begin, ensure you have the following installed:
- ✅ Python 3.7 or higher ([Download here](https://www.python.org/downloads/))
- ✅ pip (comes with Python)
- ✅ Git ([Download here](https://git-scm.com/downloads))

### Step-by-Step Setup

#### 1️⃣ Clone the Repository

```bash
git clone https://github.com/niks1503/MediTrack-App.git
cd MediTrack-App
```

#### 2️⃣ Create a Virtual Environment

**Why?** This keeps your project dependencies isolated and organized.

**On macOS/Linux:**
```bash
python3 -m venv venv
source venv/bin/activate
```

**On Windows:**
```bash
python -m venv venv
.\venv\Scripts\activate
```

*You should see `(venv)` appear in your terminal prompt.*

#### 3️⃣ Install Dependencies

```bash
pip install Flask
```

*Optional: For better experience, also install:*
```bash
pip install python-dateutil
```

#### 4️⃣ Initialize the Database

```bash
python init_db.py
```

✅ **Success!** You should see a message confirming database creation.

## 🚀 How to Use

### Starting the Application

1. **Activate your virtual environment** (if not already active)
   ```bash
   # macOS/Linux
   source venv/bin/activate
   
   # Windows
   .\venv\Scripts\activate
   ```

2. **Run the Flask app**
   ```bash
   python app.py
   ```

3. **Open your browser**
   
   Navigate to: `http://127.0.0.1:5000/` or `http://localhost:5000/`

### Using the Application

#### Adding a Medicine

1. Click on **"Add New Medicine"** button
2. Fill in the form:
   - **Medicine Name:** e.g., "Aspirin"
   - **Medicine Type:** Tablet, Syrup, Injection, Capsule, etc.
   - **Expiry Date:** Select from calendar
3. Click **"Save"** or **"Add Medicine"**

#### Viewing Your Medicine List

- Your dashboard displays all medicines in an organized table
- Color-coded alerts help you quickly identify:
  - 🟢 **Green:** Safe (expires in 30+ days)
  - 🟡 **Yellow:** Warning (expires in 7-30 days)
  - 🔴 **Red:** Critical (expired or expires in < 7 days)

#### Managing Medicines

- **Edit:** Click the edit icon to update medicine details
- **Delete:** Click the delete icon to remove a medicine
- **Search:** Use the search bar to quickly find specific medicines

## 📁 Project Structure

```
MediTrack-App/
│
├── 📄 app.py                 # Main Flask application (routes & logic)
├── 📄 init_db.py             # Database initialization script
├── 🗄️ database.db            # SQLite database (auto-created)
│
├── 📁 static/                # Static files
│   ├── 🎨 css/              # Stylesheets
│   ├── 📜 js/               # JavaScript files
│   └── 🖼️ images/           # Images and icons
│
├── 📁 templates/             # HTML templates
│   ├── 🏠 index.html        # Main dashboard
│   ├── ➕ add.html          # Add medicine form
│   └── ✏️ edit.html         # Edit medicine form
│
└── 📄 README.md              # You are here!
```

## 🎓 How It Works

### The Flow

```
User Opens Browser → Flask Server → SQLite Database
       ↓                    ↓              ↓
  View Dashboard ← Get Medicine Data ← Query Database
       ↓
  Add Medicine → Save to Database → Update Dashboard
       ↓
  Check Alerts ← Calculate Days to Expiry ← Current Date
```

### Alert System Logic

```python
Days Until Expiry:
├── > 30 days  → ✅ Safe (Green)
├── 7-30 days  → ⚠️ Warning (Yellow)
├── < 7 days   → 🚨 Critical (Orange)
└── Expired    → ❌ Expired (Red)
```

## 🤝 Contributing

We love contributions! Here's how you can help make MediTrack-App even better:

### Ways to Contribute

- 🐛 **Report Bugs:** Found an issue? [Open an issue](https://github.com/niks1503/MediTrack-App/issues)
- 💡 **Suggest Features:** Have an idea? We'd love to hear it!
- 📝 **Improve Documentation:** Help others understand the project better
- 💻 **Submit Code:** Fix bugs or add new features

### Contribution Process

1. **Fork** the repository
2. **Create** a feature branch
   ```bash
   git checkout -b feature/AmazingFeature
   ```
3. **Commit** your changes
   ```bash
   git commit -m 'Add some AmazingFeature'
   ```
4. **Push** to the branch
   ```bash
   git push origin feature/AmazingFeature
   ```
5. **Open** a Pull Request

## 🗺️ Roadmap

Future enhancements we're planning:

- [ ] 📧 Email notifications for expiring medicines
- [ ] 📱 SMS alerts via Twilio integration
- [ ] 👥 Multi-user support with authentication
- [ ] 📊 Analytics dashboard with usage statistics
- [ ] 🔄 Medicine reorder reminders
- [ ] 📥 Import/Export medicine lists (CSV/Excel)
- [ ] 🌙 Dark mode
- [ ] 🌐 Multi-language support
- [ ] 📱 Mobile app (React Native)
- [ ] 🔔 Push notifications

## ❓ FAQ

<details>
<summary><b>Is my data secure?</b></summary>
<br>
Yes! All data is stored locally on your machine in an SQLite database. Nothing is sent to external servers.
</details>

<details>
<summary><b>Can I access this from multiple devices?</b></summary>
<br>
Currently, the app runs locally. However, you can deploy it to a cloud server for multi-device access.
</details>

<details>
<summary><b>What happens if I delete a medicine by mistake?</b></summary>
<br>
Currently, deletion is permanent. We recommend backing up your database.db file regularly. A trash/undo feature is planned for future releases.
</details>

<details>
<summary><b>Can I customize the alert thresholds?</b></summary>
<br>
Not yet, but this is a planned feature! Currently, alerts trigger at 30, 7, and 0 days before expiry.
</details>

## 📞 Support

Need help? Here's how to reach us:

- 📧 **Email:** Open an issue on GitHub
- 💬 **Discussions:** [GitHub Discussions](https://github.com/niks1503/MediTrack-App/discussions)
- 🐛 **Bug Reports:** [GitHub Issues](https://github.com/niks1503/MediTrack-App/issues)

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

</div>
