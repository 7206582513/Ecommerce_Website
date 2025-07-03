
# 🛒 Ecommerce AI: Smart Product Recommendation Platform

Welcome to the **AI-Powered Ecommerce Platform** — a fully functional system built with FastAPI, Machine Learning, and NLP that recommends the right products to users based on their activity like views, cart, or wishlist.

This project is created for educational and hackathon purposes under the guidance of Rohit Arora (Tech Club Lead), and is designed to help juniors learn the fundamentals of recommendation systems in a production-like setup.

---

## 🚀 Project Features

| Module                   | Description                                                                 |
|--------------------------|-----------------------------------------------------------------------------|
| ✅ Personalized Recs      | Collaborative filtering using user/item similarity                         |
| 🔁 Cold Start Solution     | Recommend products for new users using demographics or content             |
| 🤖 Chat Assistant (Optional)| Ask product queries like “show me watches under ₹1000” using LLM (Groq API)|
| 🧠 NLP Keyword Search     | Users can search using keywords or tags                                    |
| 📊 Logs Everything        | Every user click tracked for analytics and training                        |

---

## 📁 Folder Structure

```
ecommerce_ai_project/
│
├── backend/                  → Main FastAPI backend + ML logic
│   ├── main.py              → API and server
│   ├── recommender.py       → Collaborative filtering models
│   ├── cold_start.py        → Handles new users/items (cold start)
│   ├── nlp_utils.py         → NLP search & keyword extraction
│   ├── db_models.py         → SQLAlchemy DB models
│   ├── product_utils.py     → Filter/sort/rank products
│   ├── chat_assistant.py    → Optional Groq API logic
│   └── utils.py             → Similarity metrics, helpers
│
├── frontend/
│   ├── templates/           → HTML Pages
│   │   ├── index.html       → Homepage
│   │   ├── product.html     → Product details
│   │   ├── results.html     → Recommendation display
│   │   └── chat.html        → Chat interface
│   ├── static/
│   │   ├── css/style.css    → Styles (Bootstrap/Tailwind)
│   │   ├── js/main.js       → JavaScript logic
│   │   └── images/          → Product/user images
│
├── data/
│   ├── users.csv            → Sample users (age, gender, location)
│   ├── products.csv         → Sample products (name, category, price)
│   └── interactions.csv     → Clicks, wishlist, cart, etc.
│
├── models/
│   └── collaborative_model.pkl → Trained similarity matrix/model
│
├── tests/
│   └── test_recommender.py  → Unit tests for recommendation logic
│
├── requirements.txt         → Python dependencies
├── .gitignore               → Ignored files like .env, logs, .pyc
└── README.md                → 📘 You're reading it!
```

---

## 🔧 Installation Guide

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/ecommerce_ai_project.git
cd ecommerce_ai_project
```

### 2. Setup Virtual Environment

```bash
python -m venv .venv
source .venv/bin/activate        # Linux/Mac
# OR
.venv\Scripts\activate           # Windows
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Start the Backend Server

```bash
cd backend
uvicorn main:app --reload
```

Access API at: [http://localhost:8000](http://localhost:8000)

### 5. Run Frontend

Open `frontend/templates/index.html` manually in browser. Or serve with Flask/Express if needed.

---

## 🧪 Sample Data Preview

### `users.csv`
| user_id | age | gender | location |
|---------|-----|--------|----------|
| U001    | 23  | F      | Delhi    |
| U002    | 31  | M      | Mumbai   |

### `products.csv`
| product_id | name         | category | price |
|------------|--------------|----------|-------|
| P101       | Jeans        | Fashion  | 1299  |
| P102       | Smart Watch  | Gadgets  | 1999  |

### `interactions.csv`
| user_id | product_id | action       | timestamp           |
|---------|------------|--------------|---------------------|
| U001    | P101       | view         | 2025-07-03 12:01:00 |
| U001    | P102       | add_to_cart  | 2025-07-03 12:03:12 |

---

## 📚 What Juniors Will Learn

- Collaborative Filtering (User & Item-based)
- Handling Cold Start with demographics and content
- Product ranking using similarity
- Tracking interaction logs
- Frontend integration with backend via FastAPI
- Bonus: Chatbot with Groq/OpenAI API (optional)

---

## ✨ Credits

| Name         | Role                      |
|--------------|---------------------------|
| **Rohit Arora** | Lead Developer / Mentor     |
| Junior Dev 1 | Frontend Developer         |
| Junior Dev 2 | API Integrator + Logger    |
| Junior Dev 3 | ML Tuner + Data Analyst    |

---

## 💬 Contact

If you’re stuck or want guidance, feel free to reach out to **Rohit Arora** via:
- WhatsApp group (ask first)
- 📞 Preferably call for quick explanation

---

## 🔥 Bonus Ideas

- Integrate Stripe or Razorpay for checkout simulation
- Add login/register system with Flask-Login
- Deploy with Railway, Vercel or Replit

---

> “This project isn’t just about code — it’s about building something real. Learn the why, not just the how.” – Rohit
