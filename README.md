# 🎓 My Dashboard — Student Learning Platform

A modern, full-stack student dashboard built with **Next.js 15**, **TypeScript**, and **Tailwind CSS**. Features AI-powered mentorship, course tracking, leaderboard, and complete authentication flow.

---

## ✨ Features

### 🔐 Authentication
- **Register** with First, Middle & Last Name, Phone (country-wise validation), Email, Password with live validation rules, Google reCAPTCHA
- **Login** with Email or Phone toggle, Remember Me (persists across logout), Show/Hide password, Forgot Password
- **Forgot Password** via EmailJS — sends real reset link to user's email
- **Logout** confirmation modal with remembered credentials preserved

### 📊 Dashboard
- Personalized welcome — **"Welcome"** for new users, **"Welcome Back"** for returning users
- Edit Profile modal to update display name
- Stats cards — Total Points, Courses Done, Global Rank
- Recent Activity timeline with "View All" modal

### 📚 Courses
- Course cards with progress bars, instructor info, difficulty level
- Search by course name
- Filter by category — All, Web Dev, DSA, AI/ML
- Study material PDF links

### 🏆 Leaderboard
- Top 3 podium cards with special styling for Rank #1
- Full global standings table with streaks and points

### 🤖 AI Code Mentor (Chatbot)
- Floating chatbot powered by **Groq API** (Llama 3.1)
- Hinglish responses — friendly and technical
- Personalized with user's name

---

## 🛠️ Tech Stack

| Technology | Usage |
|---|---|
| Next.js 15 | Framework (App Router) |
| TypeScript | Type Safety |
| Tailwind CSS | Styling |
| Groq SDK | AI Chatbot (Llama 3.1) |
| EmailJS | Forgot Password emails |
| Google reCAPTCHA | Bot Protection |
| react-phone-input-2 | International Phone Input |

---

## 📁 Project Structure
mydashboard/
├── app/
│   ├── page.tsx                  # Dashboard
│   ├── register/
│   │   └── page.tsx              # Registration Page
│   ├── login/
│   │   └── page.tsx              # Login Page
│   ├── forgot-password/
│   │   └── page.tsx              # Forgot Password Page
│   ├── courses/
│   │   └── page.tsx              # Courses Page
│   ├── leaderboard/
│   │   └── page.tsx              # Leaderboard Page
│   ├── api/
│   │   └── chat/
│   │       └── route.ts          # Groq AI API Route
│   └── components/
│       ├── sidebar.tsx           # Sidebar Navigation
│       └── AIChatbot.tsx         # AI Chatbot Component
├── .env.local                    # Environment Variables (never commit!)
├── public/
└── package.json

---

## 🚀 Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/your-username/mydashboard.git
cd mydashboard
```

### 2. Install dependencies
```bash
npm install
```

### 3. Setup environment variables

Create a `.env.local` file in the root directory:
```dotenv
# Groq AI (Free) — https://console.groq.com
GROQ_API_KEY=your_groq_api_key

# EmailJS — https://www.emailjs.com
NEXT_PUBLIC_EMAILJS_SERVICE_ID=your_service_id
NEXT_PUBLIC_EMAILJS_TEMPLATE_ID=your_template_id
NEXT_PUBLIC_EMAILJS_PUBLIC_KEY=your_public_key
```

### 4. Run the development server
```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

---

## 🔑 Environment Variables Guide

| Variable | Where to get |
|---|---|
| `GROQ_API_KEY` | [console.groq.com](https://console.groq.com) → Free signup → Create API Key |
| `NEXT_PUBLIC_EMAILJS_SERVICE_ID` | [emailjs.com](https://emailjs.com) → Email Services → Your Service |
| `NEXT_PUBLIC_EMAILJS_TEMPLATE_ID` | EmailJS → Email Templates → Your Template |
| `NEXT_PUBLIC_EMAILJS_PUBLIC_KEY` | EmailJS → Account → Public Key |

---

## ⚠️ Important Notes

- **Never commit `.env.local`** to GitHub — it's already in `.gitignore`
- **Google reCAPTCHA** sitekey in the code is for `localhost` — update it for production domain at [google.com/recaptcha](https://www.google.com/recaptcha)
- This project uses **localStorage** for session management — suitable for demo/learning projects

---

## 📸 Pages Overview

| Page | Route |
|---|---|
| Dashboard | `/` |
| Register | `/register` |
| Login | `/login` |
| Forgot Password | `/forgot-password` |
| Courses | `/courses` |
| Leaderboard | `/leaderboard` |

---

## 🙏 Credits

Built with ❤️ by **Sreyansh Verma**

- [Next.js](https://nextjs.org)
- [Tailwind CSS](https://tailwindcss.com)
- [Groq](https://groq.com)
- [EmailJS](https://emailjs.com)
- [Google reCAPTCHA](https://www.google.com/recaptcha)