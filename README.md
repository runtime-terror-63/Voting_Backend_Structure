
# 🗳️ Voting_Backend_Structure

This is a **backend application** for a simple voting system where users can vote for candidates. It supports user authentication, candidate management, and vote casting, with role-based access control for admin and users.

---

## 🚀 Features

- 🔐 User signup and login using Aadhar Card Number and password
- 📋 View list of candidates
- 🗳️ One-time vote per user
- 🛡️ Admin can:
  - ➕ Add candidates
  - ✏️ Update candidates
  - ❌ Delete candidates
- 🚫 Admin **cannot** vote

---

## 🛠️ Tech Stack

- Node.js
- Express.js
- MongoDB
- JWT (JSON Web Tokens)

---

## 📦 Installation

```bash
git clone https://github.com/runtime-terror-63/Voting_Backend_Structure.git
cd Voting_Backend_Structure
npm install
```

##.env

```bash
JWT_SECRET=
PORT=
MONGODB_URL_LOCAL=
```

## 📡 API Endpoints

### 🔐 Authentication

- `POST /signup`  
  ➤ Sign up a user

- `POST /login`  
  ➤ Log in a user and receive JWT

---

### 👤 User Profile

- `GET /user/profile`  
  ➤ Get user profile info

- `PUT /user/profile/password`  
  ➤ Change user password

---

### 🧑‍💼 Candidates

- `GET /candidate`  
  ➤ Get list of candidates

- `POST /candidate` _(Admin only)_  
  ➤ Add a new candidate

- `PUT /candidate/:id` _(Admin only)_  
  ➤ Update candidate by ID

- `DELETE /candidate/:id` _(Admin only)_  
  ➤ Delete candidate by ID

---

### 🗳️ Voting

- `POST /candidate/vote/:id`  
  ➤ Vote for a candidate (User only, one vote per user)

- `GET /candidate/voted/count`  
  ➤ Get total votes for each candidate

