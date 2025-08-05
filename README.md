# 🧠 IKYAM Workshop Notes - Prompt Engineering Techniques in Markdown

This guide contains all the major prompting techniques in **Markdown format**, ready to be used in documentation, GitHub repositories, workshops, or LMS platforms.

---

## 1. Zero-Shot Prompting

**Description:**
Ask the model to perform a task without giving it any examples.

**Syntax:**

```markdown
Write a brief explanation of SAP S/4HANA.
```

**Use Case:** General queries, definitions, open-ended tasks.

---

## 2. One-Shot Prompting

**Description:**
Provide a single example before the actual task to guide the model.

**Syntax:**

```markdown
Example:
User: "What is MRP in SAP?"
Response: "MRP stands for Material Requirements Planning. It ensures that materials are available for production."

Now answer:
User: "What is a movement type in SAP?"
```

**Use Case:** Demonstrating style or context before asking the model.

---

## 3. Few-Shot Prompting

**Description:**
Provide a few examples (typically 2–5) to help the model learn the task pattern.

**Syntax:**

```markdown
User: "Error ME012"
Response: "Missing vendor master data."

User: "Error M8379"
Response: "Serial number missing during GR."

User: "Error F5120"
Response: "..."
```

**Use Case:** Categorization, classification, or support-related predictions.

---

## 4. Chain-of-Thought Prompting

**Description:**
Encourage the model to reason step-by-step before producing an answer.

**Syntax:**

```markdown
Let’s reason step-by-step to understand the error:
1. Error: 'No pricing condition found.'
2. Is the pricing procedure assigned? Yes.
3. Are condition records maintained? No.
Answer: Maintain condition record for PB00.
```

**Use Case:** Debugging, troubleshooting, and explanations.

---

## 5. Role-Based Prompting

**Description:**
Assign the model a specific role or persona.

**Syntax:**

```markdown
You are a senior SAP consultant. Explain the purpose of T-Code ME21N.
```

**Use Case:** Simulation of expert behavior, role-playing, onboarding.

---

## 6. Instruction-Based Prompting

**Description:**
Use explicit, clear instructions for the model to follow.

**Syntax:**

```markdown
Write an apology email for delayed invoice processing. Keep it professional, under 100 words.
```

**Use Case:** Email writing, document generation, SAP letters.

---

## 7. ReAct (Reason + Act)

**Description:**
Model performs step-by-step reasoning and takes actions (like tool use).

**Syntax:**

```markdown
Question: What’s today’s USD to INR exchange rate?
Thought: I need to look it up.
Action: search("USD to INR exchange rate")
```

**Use Case:** AI agents, SAP copilots with API access.

---

## 8. Self-Consistency Prompting

**Description:**
Generate multiple outputs and select the most consistent result.

**Syntax:**

```markdown
Prompt the model multiple times with:
"Why does MRP skip material X?"

Collect responses → Compare → Select best.
```

**Use Case:** Reliable decision-making, QA automation.

---

## 9. Reflexion (Deliberate Prompting)

**Description:**
Ask the model to reflect on and correct its previous mistakes.

**Syntax:**

```markdown
Initial Output: “Pricing error is due to missing config.”
User Feedback: “Config is correct.”
Prompt: Reflect and revise your answer.
Corrected Output: “Condition record might be missing.”
```

**Use Case:** Auto-correction, debugging, intelligent assistants.

---

## 📌 Pro Tip

All techniques can be **combined** for more complex workflows. For example:

```markdown
Role: You are an SAP SD consultant.
Instruction: Analyze the pricing issue.
Chain of Thought: Step-by-step reasoning.
ReAct: Fetch condition types from SAP config DB.
```

---

## 📚 Additional Resources

* [OpenAI Prompt Engineering Guide](https://platform.openai.com/docs/guides/gpt)
* [LangChain Documentation](https://docs.langchain.com/)
* [SAP BTP + GenAI Use Cases](https://community.sap.com/topics/generative-ai)

---

## 🛠️ License

MIT License. Use freely and customize for your training or documentation.
