# Flutter Service Booking App

A full-stack mobile application built with **Flutter** and **FastAPI** that allows users to browse services, book appointments, and make online payments.  
This project demonstrates **real-world app architecture**, including authentication, CRUD operations, state management, caching, and payment integration.

---

## 🚀 Features

### User Features
- Sign up / Log in with **JWT authentication**
- Browse available services
- Book appointments with date and time selection
- Make secure online payments (eSewa / Stripe)
- View booking history
- Offline support with **local caching** using Hive

### Admin Features
- Create, update, and delete services
- Manage user bookings
- View payment status

### Technical Features
- **State Management:** Riverpod / BLoC
- **Backend:** FastAPI (REST API)
- **Database:** PostgreSQL
- **Caching:** 
  - Local: Hive (Flutter)  
  - Backend: Redis
- **Authentication:** JWT access & refresh tokens
- **Payment Gateway:** eSewa / Stripe
- **Error Handling:** Proper loading indicators, API errors, and empty states
- **Clean Architecture:** Separation of concerns (MVVM / Clean)

---

## 🏗️ Architecture

### Flutter (Frontend)


---

## 🗄️ Database Schema

### User
- `id` (PK)
- `email`
- `password` (hashed)
- `role` (User/Admin)

### Service
- `id` (PK)
- `name`
- `description`
- `price`
- `duration`

### Booking
- `id` (PK)
- `user_id` (FK)
- `service_id` (FK)
- `date`
- `status` (pending / paid / cancelled)

---

## 💾 Caching Strategy

### Flutter
- Hive for service lists, booking history, and token storage
- CachedNetworkImage for images
- Offline-first approach

### FastAPI
- Redis for frequently accessed services and bookings
- TTL-based cache invalidation
- Optimized API performance

---

## 💳 Payment Flow
1. User selects service & booking time
2. Flutter app requests payment intent from FastAPI
3. Payment is processed through eSewa / Stripe
4. Backend verifies payment and updates booking status
5. App reflects confirmation to the user

---

## 🛠️ Tech Stack

- **Frontend:** Flutter  
- **Backend:** FastAPI  
- **Database:** PostgreSQL  
- **Cache:** Hive (Flutter), Redis (FastAPI)  
- **Authentication:** JWT  
- **Payment Gateway:** eSewa / Stripe  
- **State Management:** Riverpod / BLoC  

---

## 🔧 Installation & Setup

### Backend (FastAPI)
```bash
git clone <repo-url>
cd backend
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
uvicorn app.main:app --reload


---

This README **hits all the portfolio points**: features, tech stack, architecture, caching, payments, and installation.  

If you want, I can **also make a version with diagram illustrations** showing **Flutter ↔ FastAPI ↔ Database ↔ Cache ↔ Payment**, which looks **super professional on GitHub**.  

Do you want me to do that next?

