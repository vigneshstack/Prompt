🏠 House Price Prediction Using Linear Regression

This mini-project demonstrates how we can **predict house prices** based on **house size (in square feet)** using a simple **linear regression model**.

---

## 📊 Dataset Overview

We use a **very basic dataset** of past house sales to train the model:

| Index | Size (sqft) | Price ($1000s) |
|-------|-------------|----------------|
| 0     | 500         | 100            |
| 1     | 750         | 150            |
| 2     | 1000        | 200            |
| 3     | 1250        | 250            |
| 4     | 1500        | 300            |
| 5     | 1750        | 350            |
| 6     | 2000        | 400            |

✅ **Pattern**: As size increases, price increases linearly.  
💡 This is a perfect use case for **linear regression**.

---

## 📈 What’s Plotted

### 1️⃣ Scatter Plot – House Size vs Price
![Plotted](https://github.com/vigneshstack/Prompt/blob/main/prediction/sizeprice.png)

This graph simply shows the **original data points**.

- X-axis: House size in square feet
- Y-axis: Price in $1000s
- Each blue dot = one house sale

📌 This visual helps confirm that the relationship between size and price is **linear**.

---

### 2️⃣ Regression Plot – Model Prediction

This graph adds:
- 🔵 Original data points (blue)
- 🔴 A **regression line** (red) learned by the model
- 🟢 A **prediction point** for a 1600 sqft house

📍 The model learns the pattern:
> Every additional 250 sqft increases the price by ~$50,000

📌 Based on this, it predicts:
 🏡 **1600 sqft → ~$320,000**

---

## 🤖 How It’s Predicted

1. **Model Used**: Linear Regression  
2. **Feature**: House size (in sqft)  
3. **Target**: Price (in $1000s)  
4. **Training**: Model is trained on past data  
5. **Prediction**: We ask the model to estimate price for a 1600 sqft house

---
![Regression](https://github.com/vigneshstack/Prompt/blob/main/prediction/regression.png)

## 🧠 Create a Model in Real-Time with Teachable Machine

Teachable Machine by Google is a fast, easy-to-use web tool that lets you create machine learning models without writing any code.

In this session, we'll build an **image recognition model** live, in real-time!

---

### 📸 What We'll Do:
1. Upload or capture images from your webcam
2. Label them into categories (e.g., "Happy Face", "Sad Face", "No Mask", "With Mask")
3. Train the model instantly in your browser
4. Test the model live — see real-time predictions!
5. Export your model for use in apps or websites

---

### 🔗 Link to Get Started:
👉 [Train an Image Model Now](https://teachablemachine.withgoogle.com/train/image)




