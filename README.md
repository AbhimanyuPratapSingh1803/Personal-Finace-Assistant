# 💰 Personal Finance Assistant

A **full-stack MERN application** that helps users manage their personal finances by tracking income, expenses, receipts, and generating insightful analytics.

---
## 🎥 Demo Video
Watch the complete Application walkthrough here : https://bit.ly/3K0FAGY

---

## ✨ Features

### 🔐 Authentication
- Secure **JWT-based login and registration**
- Passwords hashed with **bcrypt**

### 📊 Finance Management
- Add, view, filter, and delete **income & expense transactions**
- Categorize expenses (Food, Travel, Utilities, etc.)
- **Date range filters** to view transactions and analytics

### 📂 Receipt Handling
- Upload **PDF receipts** to auto-extract transactions
- (Planned) OCR support for images (JPG/PNG)

### 📈 Analytics Dashboard
- **Category breakdown** (Pie chart)
- **Monthly income vs expenses** (Bar chart)
- **Spending trends** (Line chart)
- **Summary cards** with totals

### 📱 Responsive UI
- Built with **Tailwind CSS**
- Optimized for both mobile and desktop users

### 🔮 Future Enhancements
- Budget setting & tracking
- Multi-currency support
- Export to CSV/PDF
- Email reminders/notifications

---

## 🛠 Tech Stack

### Frontend
- ⚛ **React** (UI framework)
- ⚡ **Vite** (fast dev server & bundler)
- 🎨 **Tailwind CSS** (utility-first CSS)
- 📊 **Chart.js + react-chartjs-2** (analytics visualisation)
- 🔗 **Axios** (API client)
- 🗓 **date-fns** (date handling)
- 🎯 **Lucide React** (icons)

### Backend
- 🟢 **Node.js** (runtime)
- 🚀 **Express.js** (backend framework)
- 🍃 **MongoDB** (NoSQL database)
- 📦 **Mongoose** (ODM)
- 🔐 **JWT (jsonwebtoken)** (auth tokens)
- 🛡 **bcryptjs** (password hashing)
- 🌐 **CORS** (cross-origin handling)
- ✅ **express-validator** (input validation)

---

## 📂 File Structure

```
Personal-Finace-Assistant/
├── Backend/
│   ├── models/
│   │   ├── User.js            # User schema & model
│   │   └── Transaction.js     # Transaction schema & model
│   ├── routes/
│   │   ├── auth.js            # Login & register routes
│   │   ├── transactions.js    # CRUD for transactions
│   │   ├── analytics.js       # Finance analytics endpoints
│   │   └── categories.js      # Predefined categories
│   ├── middleware/
│   │   └── auth.js            # JWT authentication middleware
│   ├── utils/
│   │   └── constants.js       # Static data & constants
│   ├── server.js              # Express server entry point
│   ├── seed.js                # Seed DB with sample data
│   └── package.json
│
└── Frontend/
    ├── src/
    │   ├── components/
    │   │   ├── Dashboard.jsx        # Dashboard with charts & summary
    │   │   ├── Analytics.jsx        # Analytics visualisation
    │   │   ├── TransactionList.jsx  # List & filter transactions
    │   │   ├── AuthForm.jsx         # Login/Signup form
    │   │   └── Navigation.jsx       # Navbar & routing
    │   ├── services/
    │   │   └── api.js               # Axios API service
    │   ├── App.jsx                  # Root component
    │   └── index.css                # Global Tailwind styles
    └── package.json
```

---

## ⚡ Functionality Overview

### Backend
- **Authentication**: JWT-based login/registration with hashed passwords  
- **Transaction Management**: CRUD APIs for income & expenses  
- **Analytics**: Endpoints to calculate monthly trends, category splits, and summaries  
- **Receipt Handling**: PDF upload & parsing (OCR support planned)  

### Frontend
- **Login/Register** UI connected with backend APIs  
- **Dashboard** with summary cards & analytics charts  
- **Transactions Page** with filtering & CRUD options  
- **Responsive Navigation** with protected routes  
- **API Service Layer** for clean frontend-backend communication  

---

## 🔧 Getting Started

### Prerequisites
- Node.js (>= 18)
- MongoDB (local or MongoDB Atlas)
- npm or yarn

### Backend Setup

```bash
cd Personal-Finance-Assistant/Backend
npm install
```

Create a `.env` file:

```
PORT=5000
MONGODB_URI=mongodb://localhost:27017/personal-finance
JWT_SECRET=your-secret-key
```

Run backend:

```bash
npm run dev    # development
npm start      # production
```

### Frontend Setup

```bash
cd Personal-Finance-Assistant/Frontend
npm install
npm run dev
```

Frontend runs at 👉 `http://localhost:5173`  
Backend runs at 👉 `http://localhost:5000`

---

## 📡 API Endpoints

### Auth
- `POST /api/auth/register` → Register a new user  
- `POST /api/auth/login` → Login user  

### Transactions
- `GET /api/transactions` → Get all transactions  
- `POST /api/transactions` → Create transaction  
- `GET /api/transactions/range` → Get transactions in a date range  
- `DELETE /api/transactions/:id` → Delete transaction  

### Analytics
- `GET /api/analytics/categories` → Expense breakdown by category  
- `GET /api/analytics/monthly` → Monthly income vs expense  
- `GET /api/analytics/trends` → Spending trends  
- `GET /api/analytics/summary` → Summary  

### Categories
- `GET /api/categories` → Fetch predefined categories  

### Receipts
- `POST /api/receipt/upload-receipt` → Upload & parse receipt (PDF)  
- `GET /api/receipt/receipt/:filename` → Download receipt  

---

## 🛠 Development Notes
- Tokens expire in **7 days**  
- Passwords hashed with **bcrypt**  
- Input validation via **express-validator**  
- **CORS** enabled for frontend communication  
- Frontend uses **Axios interceptors** for auth headers  

---
