Here’s a **MongoDB README.md for a Library Management System** you can directly use in your project 👇

---

# 📚 Library Management System (MongoDB)

A simple **Library Management System** built using **MongoDB** to manage books, users, and issue/return records.

---

## 🚀 Features

* Add, update, delete books
* Manage users (students/admin)
* Issue and return books
* Track due dates and availability
* Search books by title/author

---

## 🛠️ Tech Stack

* Database: MongoDB
* Backend: Node.js (optional)
* API Testing: Postman / Thunder Client

---

## 📂 Database Structure

### 1. 📘 Books Collection

```json
{
  "_id": ObjectId,
  "title": "The Alchemist",
  "author": "Paulo Coelho",
  "isbn": "1234567890",
  "availableCopies": 5,
  "totalCopies": 10,
  "category": "Fiction"
}
```

---

### 2. 👤 Users Collection

```json
{
  "_id": ObjectId,
  "name": "rakshita",
  "email": "rakshita@email.com",
  "role": "student",
  "issuedBooks": []
}
```

---

### 3. 📖 Transactions Collection

```json
{
  "_id": ObjectId,
  "userId": ObjectId,
  "bookId": ObjectId,
  "issueDate": "2026-05-01",
  "returnDate": "2026-05-10",
  "status": "issued"
}
```

---

## ▶️ Setup Instructions

### 1. Start MongoDB

```bash
mongod
```

---

### 2. Open Mongo Shell

```bash
mongosh
```

---

### 3. Create Database

```js
use libraryDB
```

---

## 📌 Basic Operations

### 📘 Add Book

```js
db.books.insertOne({
  title: "The Alchemist",
  author: "Paulo Coelho",
  isbn: "1234567890",
  availableCopies: 5,
  totalCopies: 10,
  category: "Fiction"
})
```

---

### 👤 Add User

```js
db.users.insertOne({
  name: "rakshita",
  email: "rakshita@email.com",
  role: "student",
  issuedBooks: []
})
```

---

### 📖 Issue Book

```js
db.transactions.insertOne({
  userId: ObjectId("USER_ID"),
  bookId: ObjectId("BOOK_ID"),
  issueDate: new Date(),
  returnDate: null,
  status: "issued"
})

db.books.updateOne(
  { _id: ObjectId("BOOK_ID") },
  { $inc: { availableCopies: -1 } }
)
```

---

### 🔄 Return Book

```js
db.transactions.updateOne(
  { _id: ObjectId("TRANSACTION_ID") },
  { $set: { status: "returned", returnDate: new Date() } }
)

db.books.updateOne(
  { _id: ObjectId("BOOK_ID") },
  { $inc: { availableCopies: 1 } }
)
```

---

### 🔍 Search Books

```js
db.books.find({ title: "The Alchemist" })
```

---

## 📁 Project Structure

```
library-management/
│── models/
│── routes/
│── controllers/
│── config/
│── app.js
│── package.json
│── README.md
```

---

## ⚙️ Environment Variables

Create `.env` file:

```
MONGO_URI=mongodb://localhost:27017/libraryDB
```

---

## 🧪 Run Project

```bash
node app.js
```

---

## 📌 Future Improvements

* Add authentication (JWT)
* Fine calculation for late return
* Admin dashboard
* Book reservation system




MIT License
<img width="1590" height="766" alt="Screenshot_5-5-2026_15149_127 0 0 1" src="https://github.com/user-attachments/assets/7f76c51d-6ec2-406b-bb99-033dbe09573f" />


<img width="1585" height="765" alt="Screenshot_5-5-2026_151432_127 0 0 1" src="https://github.com/user-attachments/assets/78cd721c-f279-4057-9268-b5f0b711e204" />


<img width="1587" height="768" alt="Screenshot_5-5-2026_151519_127 0 0 1" src="https://github.com/user-attachments/assets/505eed30-81db-4eae-a75d-0a748da56fcc" />






