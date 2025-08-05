# 🍽️ Predicting Tomorrow’s Restaurant Orders (Without Knowing the Future!)

Imagine you're running a restaurant. Some days are super busy, and others are quiet. But what if you could **predict tomorrow’s order volume**, even if you don’t know *exactly* what will happen?

This project shows how to use **sample data from past days** — weather, day of the week, holidays, etc. — to predict how many orders you'll get **tomorrow**, even though tomorrow hasn't happened yet!

---

## 🤔 Why Is This Interesting?

You don’t know:
- Who will walk in tomorrow
- What dishes they'll order
- What exact time they'll come

But you do know:
- It's a **Saturday**
- The **weather forecast** says 35°C and sunny
- It's a **long weekend**
- Last few Saturdays were **super busy**

With this info, you can *predict* tomorrow's demand! 📈

---

## 📊 Dataset (Simplified)

Each row = one past day at your restaurant.

| Column | Description |
|--------|-------------|
| `day` | Monday, Tuesday, etc. |
| `date` | Date of record |
| `is_holiday` | Is it a holiday? |
| `weather` | Sunny, Rainy, Cloudy |
| `temp_celsius` | Temperature |
| `orders` | Total orders placed that day (target) ✅ |

> Note: We don’t use tomorrow’s actual data — we use similar past patterns to **guess** tomorrow.

---

## 🔮 Problem Statement

> Can we predict how many food orders we’ll get tomorrow, using weather, day of the week, and holiday info?

This helps restaurants:
- Plan how many ingredients to buy
- Decide how many staff to schedule
- Reduce waste and improve service

---

## 🧠 How the Prediction Works

1. **We train a model** using past days:
   - Sunny Saturdays = ~320 orders
   - Rainy Mondays = ~80 orders
2. **We give the model tomorrow’s info**:
   - Day: Saturday
   - Holiday: Yes
   - Weather: Sunny
   - Temp: 36°C
3. The model predicts:
