# 📚 Library Management System

A web-based **Library Management System** built using **Django** and **Django REST Framework**. This project helps manage library operations such as user accounts, book inventory, and borrowing/return transactions.

<img width="1080" height="1080" alt="photo-collage png (2)" src="https://github.com/user-attachments/assets/65438bbb-73c2-4bc6-948c-d39a35408356" />



---

## 🚀 Features

* 👤 User Authentication (Register/Login)
* 📖 Book Inventory Management
* 🔄 Borrow & Return Transactions
* 🧾 API Support with Serializers
* 🗄️ SQLite Database Integration
* 🌐 Basic HTML Templates for UI

---

## 🏗️ Project Structure

```
Library_Management_System/
│
├── accounts/          # User authentication & management
├── inventory/         # Book inventory management
├── transactions/      # Borrow/return operations
├── Library_Management_System/  # Main project settings
├── db.sqlite3         # Database
├── manage.py
└── db_connector.py
```

---

## ⚙️ Technologies Used

* Python
* Django
* Django REST Framework
* SQLite
* HTML (Templates)

---

## 🔧 Installation & Setup

### 1. Clone the repository

```bash
git clone <your-repo-url>
cd Library_Management_System
```

### 2. Create virtual environment

```bash
python -m venv venv
```

### 3. Activate virtual environment

**Windows:**

```bash
venv\Scripts\activate
```

**Mac/Linux:**

```bash
source venv/bin/activate
```

### 4. Install dependencies

```bash
pip install django djangorestframework
```

### 5. Apply migrations

```bash
python manage.py migrate
```

### 6. Run the server

```bash
python manage.py runserver
```

### 7. Open in browser

```
http://127.0.0.1:8000/
```

---

## 📌 Apps Overview

### 👤 Accounts App

* User registration & login
* Templates: `log.html`, `reg.html`
* Handles authentication logic

### 📚 Inventory App

* Add, update, delete books
* View available books
* Template: `inv.html`

### 🔄 Transactions App

* Manage borrowing and returning books
* Tracks user-book interactions

---

## 🔌 API Endpoints (Sample)

| Method | Endpoint   | Description       |
| ------ | ---------- | ----------------- |
| GET    | /books/    | Get all books     |
| POST   | /books/    | Add new book      |
| POST   | /login/    | User login        |
| POST   | /register/ | User registration |

---

## 🗃️ Database

* Default: **SQLite**
* File: `db.sqlite3`

---

## 🧪 Testing

Run tests using:

```bash
python manage.py test
```

---

## 📌 Future Improvements

* Add JWT Authentication
* Improve UI (React/Angular frontend)
* Add search & filter functionality
* Role-based access (Admin/User)
* Email notifications

---

## 🤝 Contributing

Contributions are welcome! Feel free to fork this repo and submit a pull request.

---

## 📄 License

This project is open-source and available under the MIT License.

---

## 👨‍💻 Author

Developed as a Django-based library management solution for learning and practical use.

---

💡 *Tip: Replace `<your-repo-url>` with your actual GitHub repository link.*






