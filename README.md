# 🧠 IKYAM Prompt Engineering Techniques Workshop

Welcome to the **Prompt Engineering Techniques Workshop**!  
This repository contains examples and explanations of powerful prompting techniques used to improve Large Language Model (LLM) interactions, especially for business, technical, and enterprise use cases like **SAP ERP**, **AI copilots**, **chatbots**, and **automation workflows**.

---

## 🚀 Contents

| # | Technique | Description |
|---|-----------|-------------|
| 1 | [Zero-Shot](#1-zero-shot) | Ask without giving examples |
| 2 | [One-Shot](#2-one-shot) | Give 1 example before asking |
| 3 | [Few-Shot](#3-few-shot) | Give a few examples for pattern learning |
| 4 | [Chain-of-Thought](#4-chain-of-thought) | Guide reasoning step-by-step |
| 5 | [Role-Based](#5-role-based) | Define persona or expertise |
| 6 | [Instruction-Based](#6-instruction-based) | Give clear, detailed task instructions |
| 7 | [ReAct](#7-react-reason--act) | Combine reasoning with actions (e.g., tool use) |
| 8 | [Self-Consistency](#8-self-consistency) | Generate multiple answers and choose the best |
| 9 | [Reflexion](#9-reflexion-deliberate-prompting) | Reflect on past errors and retry |

---

## 1. Zero-Shot

**📌 Description:**  
Ask a question directly without giving any prior example.

**📦 Example Prompt:**
```text
Generate a summary of the benefits of SAP S/4HANA over ECC.
