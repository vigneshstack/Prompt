# What is Machine Learning?

**Machine Learning (ML)** is a subset of Artificial Intelligence (AI) that enables computers to learn patterns from data and make decisions or predictions without being explicitly programmed.

ML is broadly categorized into:
- **Supervised Learning** – learning from labeled data
- **Unsupervised Learning** – finding hidden patterns in unlabeled data
- **Reinforcement Learning** – learning through trial and error

---
| **Input (A)**               | **Output (B)**              | **Application**          |
|----------------------------|-----------------------------|--------------------------|
| email                      | spam? (0/1)                 | spam filtering           |
| audio                      | text transcripts            | speech recognition       |
| English                    | Chinese                     | machine translation      |
| ad, user info              | click? (0/1)                | online advertising       |
| image, radar info          | position of other cars      | self-driving car         |
| image of phone             | defect? (0/1)               | visual inspection        |
| sequence of words          | the next word               | chatbot / language model |

---
# Predicting House Prices Using Linear Regression

One classic use case of ML is **predicting house prices** based on features like:

- Square footage

We use **Linear Regression**, a type of Supervised ML algorithm, to find the best-fit line that relates these features (inputs) to the house price (output). Once trained, the model can predict prices for new, unseen houses.

House Price Prediction Using Linear Regression

This mini-project demonstrates how we can **predict house prices** based on **house size (in square feet)** using a simple **linear regression model**.

---

## Dataset Overview

We use a **very basic dataset** of past house sales to train the model:

| Index | Size (sqft)       | Price ($1000s) |
|-------|-------------------|----------------|
| 0     | 500               | 100            |
| 1     | 750               | 150            |
| 2     | 1000              | 200            |
| 3     | 1250              | 250            |
| 4     | 1500              | 300            |
| 5     | 1750              | 350            |
| 6     | 2000              | 400            |

**Pattern**: As size increases, price increases linearly.  
This is a perfect use case for **linear regression**.

---

##  What’s Plotted

### 1️⃣ Scatter Plot – House Size vs Price
![Plotted](https://github.com/vigneshstack/Prompt/blob/main/images/sizeprice.png)

This graph simply shows the **original data points**.

- X-axis: House size in square feet
- Y-axis: Price in $1000s
- Each blue dot = one house sale

This visual helps confirm that the relationship between size and price is **linear**.

---

### 2️⃣ Regression Plot – Model Prediction
![Regression](https://github.com/vigneshstack/Prompt/blob/main/images/regression.png)

This graph adds:

- 🔵 Original data points (blue)
- 🔴 A **regression line** (red) learned by the model
- 🟢 A **prediction point** for a 1600 sqft house

The model learns the pattern:
> Every additional 250 sqft increases the price by ~$50,000

 Based on this, it predicts:
  **1600 sqft → ~$320,000**

---

##  How It’s Predicted

1. **Model Used**: Linear Regression  
2. **Feature**: House size (in sqft)  
3. **Target**: Price (in $1000s)  
4. **Training**: Model is trained on past data  
5. **Prediction**: We ask the model to estimate price for a 1600 sqft house

---
