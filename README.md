# company-profile-management-app


A full-stack web application that allows users to **register**, **log in**, create a **company profile**, and upload a **company logo** and **banner** using **Cloudinary**.

---

## 🚀 Features

✅ **User Authentication** – Secure register/login using JWT  
✅ **Company Profile CRUD** – Create and update company details  
✅ **Logo & Banner Upload** – Cloudinary image hosting  
✅ **Social Links Support** – Store links (Twitter, LinkedIn, etc.) in JSON  
✅ **Responsive Frontend** – Built with React for easy interaction  

---

## 🏗️ Tech Stack

| Layer      | Technology |
|------------|------------|
| **Frontend** | React, Axios |
| **Backend**  | Node.js, Express |
| **Database** | PostgreSQL |
| **Cloud Storage** | Cloudinary |
| **Auth**     | JWT (JSON Web Token) |

---

## 📂 Project Structure
company-project-folder/
├─ backend/
│ ├─ src/
│ │ ├─ controllers/ # Express route handlers
│ │ ├─ models/ # PostgreSQL queries
│ │ ├─ services/ # Cloudinary integration
│ │ └─ server.js # Main backend entry point
│ └─ .env # Environment variables
├─ frontend/
│ ├─ src/
│ │ ├─ App.jsx # React main component
│ │ └─ companyapi.js # API calls to backend
│ └─ package.json
└─ README.md # You are here

---

## ⚡ Setup Instructions

### 1️⃣ Prerequisites
- **Node.js** v18+  
- **PostgreSQL** running locally  
- **Cloudinary** account (for image uploads)

### 2️⃣ Clone the Repository

git clone https://github.com/<your-username>/company-project.git
cd company-project-folder

### 3️⃣ Backend Setup

Create a .env file inside backend/:
PORT=5000


DB_HOST=localhost
DB_PORT=5432
DB_USER=postgres
DB_PASSWORD=your_db_password
DB_NAME=company_db


JWT_SECRET=supersecret
JWT_EXPIRES_IN=90d


CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret
CLOUDINARY_FOLDER=company_module

### Install dependencies and start the server:

cd backend
npm install
npm run dev   # or: node src/server.js

### 4️⃣ Database

Run the SQL to create the company_profile table:


CREATE TABLE IF NOT EXISTS company_profile (

    owner_id        INT UNIQUE NOT NULL,

    company_name    TEXT NOT NULL,
    
    address         TEXT,
    
    city            TEXT,
    
    state           TEXT,
    
    country         TEXT,
    
    postal_code     TEXT,
    
    website         TEXT,
    
    company_logo_url TEXT,
    
    company_banner_url TEXT,
    
    industry        TEXT,
    
    founded_date    DATE,
    
    description     TEXT,
    
    social_links    JSONB,
    
    updated_at      TIMESTAMP DEFAULT NOW()
);

### 5️⃣ Frontend Setup

cd frontend
npm install
npm run dev   # Starts Vite/React dev server

### 💡 Usage

Register → Create a user account.

Login → Get a JWT token stored in localStorage.

Create Company → Fill out company details and save.

Upload Logo/Banner → Select an image to upload to Cloudinary.

Update Profile → Edit fields and re-save.


### ✅ Internship Notes

This project was built as part of an internship task to demonstrate:

Full-stack development (React + Node.js + PostgreSQL)

Image uploading and third-party integration (Cloudinary)

Secure API authentication (JWT)

### 📜 License

This project is for educational/internship use.
Feel free to fork and extend it

### 👤 Author

Your Name
📧 chinthala.shivani0@gmail.com

🔗 LinkedIn(https://www.linkedin.com/in/chinthala-shivani-2a67272a2)
 | [GitHub](https://github.com/Shivani9chinthala)
