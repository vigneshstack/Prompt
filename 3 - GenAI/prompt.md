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
| Prompt Technique        | Use Case                                                                 | Similar Prompt Technique     | Key Difference                                                                 |
|---------------------------|-----------------------------------------------------------------------------|---------------------------------|----------------------------------------------------------------------------------|
| Zero-shot Prompting       | Quick answers without examples (e.g., translation, factual Q&A)            | One-shot, Few-shot             | No examples are provided                                                        |
| One-shot Prompting        | Tasks needing format guidance with a single example                        | Zero-shot, Few-shot            | Uses only one example to guide the model                                        |
| Few-shot Prompting        | Classification, structured outputs, or pattern learning                    | One-shot                        | Provides multiple examples (2–5)                                                |
| Chain-of-Thought (CoT)    | Step-by-step reasoning (math, logic, puzzles)                              | Self-consistency                | Model is explicitly guided to "think aloud"                                     |
| Self-Consistency          | Reliable answers in reasoning tasks by aggregating multiple CoT outputs    | Chain-of-Thought                | Picks the most common answer from multiple reasoning paths                      |
| ReAct (Reason+Act)        | Decision-making, tool use, or question-answering with external reasoning   | CoT                             | Interleaves reasoning and taking actions (e.g., search, calculation)            |
| Retrieval-Augmented (RAG) | Fact-based responses using external knowledge (e.g., search documents)     | ReAct                           | Augments prompt with real-time retrieved data                                   |
| Role Prompting            | Shaping model behavior (e.g., "Act as a doctor, lawyer, teacher")          | Instructional prompting         | Assigns a persona to influence tone and expertise                               |
| Instructional Prompting   | Directly tells the model what to do (e.g., "Summarize this paragraph")     | Zero-shot, Role prompting       | Explicit instructions without needing examples or persona context               |


## 🛠️ License

MIT License. Use freely and customize for your training or documentation.

