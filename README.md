
# 🛍️ AI-Powered Product Recommendation System for E-commerce

Welcome to the AI Recommendation Engine project built by [Team Tech Club]! This system recommends the most relevant products to users based on their behavior — like viewing, adding to cart, or purchasing products.

## 💡 Project Overview

This is a smart product recommendation system for an e-commerce platform (focused on fashion/women’s products). It uses **collaborative filtering** and **user interaction logs** to suggest personalized items during:

- 🔍 Product Search  
- ❤️ Wishlist 
- 🛒 Add to Cart  
- 📦 Order Completion

We built this system to simulate how real-world e-commerce giants like Amazon, Myntra, etc., serve smart product recommendations to users.

## 🧠 Features of the System

✔️ Track user interactions like **view**, **add to cart**, **wishlist**, **purchase**  
✔️ Store interactions with **timestamps**  
✔️ Use **machine learning** to recommend top-N products  
✔️ Solve **cold start** using **popularity-based fallback**  
✔️ Show recommendations in real-time

## 📂 Folder Structure

```
ecommerce_ai/
│
├── datasets/                  # Synthetic datasets for users, items, and interactions
│   ├── users.csv
│   ├── products.csv
│   └── interactions.csv
│
├── backend/
│   ├── app.py                 # Main FastAPI server
│   ├── recommender.py         # ML recommendation engine (collaborative filtering logic)
│   ├── logger.py              # Logs user actions on click
│   └── database.py            # Data storage layer (SQLite)
│
├── frontend/
│   ├── index.html             # Sample product UI
│   └── main.js                # Fetches and displays recommendations
│
├── notebooks/
│   └── recommender_training.ipynb  # Jupyter notebook to train & test models
│
├── README.md
└── requirements.txt
```

## 🔧 Tech Stack

- **Backend**: Python + FastAPI  
- **Frontend**: HTML + JS (can be upgraded with React)  
- **Database**: SQLite / PostgreSQL  
- **ML Model**: Cosine similarity-based collaborative filtering  
- **Logging**: API-based interaction logging for every click

## 📊 Dataset Structure

| Dataset       | Description                         |
|---------------|-------------------------------------|
| `users.csv`   | User ID, location, age, gender      |
| `products.csv`| Product ID, category, brand, price  |
| `interactions.csv` | User, Product, Action (view/add/purchase), Timestamp |

## 🚀 How It Works (Architecture)

```
User Interaction (clicks/views/adds)
        ⬇
Main Website (Frontend)
        ⬇
API Call to /log_interaction
        ⬇
Interaction Logger → Store in DB
        ⬇
ML Model (Collaborative Filtering)
        ⬇
Fetch top-N products
        ⬇
Show recommendations
```

## 🧪 How to Run the Project

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/ecommerce_ai.git
cd ecommerce_ai
```

### 2. Create a Virtual Environment

```bash
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate
```

### 3. Install Requirements

```bash
pip install -r requirements.txt
```

### 4. Start Backend Server

```bash
cd backend
uvicorn app:app --reload
```

### 5. Open Frontend

Just open `frontend/index.html` in your browser.

## 📚 Learning Objectives for Juniors

1. Understand how real product recommendation systems work  
2. Learn how to build collaborative filtering using Python  
3. Learn backend APIs and data logging using FastAPI  
4. Work with interaction datasets  
5. Build full-stack applications in a team

## 🙋 Contribution Guide

If you're working in a group:
- Person 1 → Backend API + FastAPI logging
- Person 2 → ML recommender logic (cosine similarity)
- Person 3 → Frontend UI + display recommended products

You can test locally with different user interactions and analyze how the model recommends changes!

## 🏁 Future Enhancements

- Add user login/signup and persistent profiles  
- Store interaction logs in real-time to PostgreSQL  
- Add deep learning recommendation (e.g., Matrix Factorization)  
- Better cold-start handling using item content (category, brand)

## 🤝 Credits

Built by **Rohit Arora** (Lead, Tech Club) and junior team members as a learning project to understand **AI in production-level recommender systems**.
