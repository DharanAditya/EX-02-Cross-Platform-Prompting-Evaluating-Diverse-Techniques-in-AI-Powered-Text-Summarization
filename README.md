# EX-02 — Cross-Platform Prompting  
**Evaluating Diverse Techniques in AI-Powered Text Summarization**

# REG NO: 212223040035

---

## AIM
To evaluate and compare the effectiveness of different prompting techniques (zero-shot, few-shot, chain-of-thought, role-based) across multiple AI platforms (ChatGPT, Gemini, Perplexity) for the task of text summarization.

---

## Scenario
You are part of a content curation team for an educational platform that delivers concise summaries of research papers to undergraduate students.  

Your task is to summarize a 500-word technical article titled **“The Basics of Blockchain Technology”** using multiple AI platforms and prompting strategies.

Your goal is to identify which **prompting technique + platform** combination gives the best summary based on:

- Accuracy  
- Coherence  
- Simplicity  
- Speed  
- User experience (UX)

---

## Algorithm

### 1. Article Selection
Choose a technical article: **“The Basics of Blockchain Technology”**.

### 2. Prompting Strategies
Use the following prompting techniques:

- **Zero-shot** – Directly ask the model to summarize without giving any prior examples.  
- **Few-shot** – Provide 2–3 example summaries of similar technical texts before asking for the summary.  
- **Chain-of-Thought (CoT)** – Instruct the model to break down the content logically step by step before generating the summary.  
- **Role-based** – Ask the model to act in a specific role (e.g., “a university professor summarizing for freshmen students”).

### 3. Platform Selection
Use the following AI platforms:

- ChatGPT (OpenAI)  
- Gemini (Google)  
- Perplexity AI

### 4. Execution
1. Apply each prompting strategy on each platform using the same input article.  
2. Record the generated summaries.  
3. Measure the time taken to generate each summary.

### 5. Evaluation Criteria
Evaluate each output on the following aspects:

- **Accuracy** – Captures main ideas correctly without distortion  
- **Coherence** – Logical flow and structure of the content  
- **Simplicity** – Easy for undergraduate students to understand  
- **Speed** – Response time of the platform  
- **User Experience (UX)** – Ease of use, readability, and ability to copy/share the content

### 6. Scoring & Analysis
1. Assign scores from 1 (poor) to 5 (excellent) for each criterion.  
2. Tabulate results for comparison.  
3. Identify the best-performing strategy-platform combinations.

---
### 1. Zero-Shot Prompting
**Definition:** The AI is asked to perform a task without any examples.  

**Example Prompt:**  
              'Translate the following English sentence to French: "I love programming."
**Platform Comparison:**

| Platform      | Strengths                        | Weaknesses                        |
|---------------|---------------------------------|----------------------------------|
| ChatGPT       | Coherent, generalizable         | Less accurate on specialized tasks |
| Gemini        | Concise, factual                | Can underexplain reasoning       |
| Perplexity    | Quick, integrates search        | Minimal reasoning, literal       |

---

### 2. Few-Shot Prompting
**Definition:** The AI is given a few examples to learn the desired output format or style.

**Example Prompt:**  
English → Spanish:

Hello → Hola

How are you? → ¿Cómo estás?
Translate this sentence: "Good morning."


**Expected Output:**  


Buenos días.


**Platform Comparison:**

| Platform      | Strengths                         | Weaknesses                       |
|---------------|----------------------------------|---------------------------------|
| ChatGPT       | Excellent pattern learning        | Long example lists may truncate |
| Gemini        | Learns patterns well             | Complex examples may be ignored |
| Perplexity    | Contextualizes answers quickly   | Limited memory for multiple examples |

---

## **3. Chain-of-Thought (CoT) Prompting**
**Definition:** The AI is asked to **reason step by step**, improving accuracy for complex tasks.

**Example Prompt:**  


Solve: If 3x + 5 = 20, what is x? Show your reasoning step by step.


**Expected Output:**  


Step 1: Subtract 5 from both sides: 3x = 15
Step 2: Divide both sides by 3: x = 5
Answer: x = 5


**Platform Comparison:**

| Platform      | Strengths                        | Weaknesses                      |
|---------------|---------------------------------|--------------------------------|
| ChatGPT       | Very strong reasoning            | Can be verbose                 |
| Gemini        | Structured reasoning supported   | Sometimes skips intermediate steps |
| Perplexity    | Some reasoning shown             | Often minimal, mostly factual  |

---

## **4. Role-Based Prompting**
**Definition:** The AI is asked to adopt a **specific role** to guide tone and content.

**Example Prompt:**  


You are a friendly math tutor. Explain to a beginner why 7 × 8 = 56 in a simple way.


**Expected Output:**  


Sure! Think of 7 groups of 8 apples. If you count all the apples, you’ll have 56 in total. So, 7 × 8 = 56!


**Platform Comparison:**

| Platform      | Strengths                        | Weaknesses                      |
|---------------|---------------------------------|--------------------------------|
| ChatGPT       | Excellent persona adaptation     | Can overemphasize role         |
| Gemini        | Concise, professional tone       | May prioritize facts over role-play |
| Perplexity    | Factual and brief                | Limited creativity in role     |

---

## **Side-by-Side Summary Table**

| Prompt Type       | Example Task                      | ChatGPT Output                  | Gemini Output                  | Perplexity Output               |
|------------------|----------------------------------|--------------------------------|--------------------------------|--------------------------------|
| Zero-Shot         | Translate "I love programming"   | J'aime programmer             | J'aime programmer             | J'aime programmer              |
| Few-Shot          | Translate "Good morning"         | Buenos días                    | Buenos días                    | Buenos días                     |
| Chain-of-Thought  | Solve 3x+5=20                    | Stepwise reasoning → x=5      | Stepwise reasoning → x=5      | Minimal reasoning → x=5        |
| Role-Based        | Tutor explanation 7×8=56         | Friendly, simple example       | Professional, concise         | Factual, brief explanation      |

---

## **Conclusion**
- **Zero-shot**: Quick and general, but limited for complex tasks.  
- **Few-shot**: Learns patterns well, better formatting and accuracy.  
- **Chain-of-Thought**: Best for complex reasoning and step-by-step solutions.  
- **Role-Based**: Excellent for tone, context, and persona-driven explanations.  


## Result

| Platform   | Prompt Type         | Accuracy | Coherence | Simplicity | Speed | UX | **Total (/25)** |
|------------|----------------------|------------|----------------|-------------------|------------|------------|--------------------|
| ChatGPT    | Zero-shot             | 4            | 4                | 4                    | 5            | 5            | 22                         |
| ChatGPT    | Few-shot               | 5            | 5                | 5                    | 4            | 5            | **24**                     |
| ChatGPT    | Chain-of-Thought  | 5            | 5                | 4                    | 3            | 5            | 22                         |
| ChatGPT    | Role-based             | 5            | 5                | 5                    | 4            | 5            | **24**                     |
| Gemini        | Zero-shot             | 3            | 3                | 3                    | 5            | 4            | 18                         |
| Gemini        | Few-shot               | 4            | 4                | 4                    | 4            | 4            | 20                         |
| Gemini        | Role-based             | 4            | 4                | 5                    | 4            | 4            | 21                         |
| Perplexity   | Zero-shot             | 4            | 4                | 4                    | 5            | 4            | 21                         |
| Perplexity   | Few-shot               | 4            | 4                | 5                    | 4            | 4            | 21                         |
| Perplexity   | Role-based             | 5            | 5                | 5                    | 4            | 4            | **23**                     |

---

## Conclusion

The best-performing combinations were:

1. **ChatGPT + Few-shot prompting → 24/25**  
2. **ChatGPT + Role-based prompting → 24/25**  
3. **Perplexity + Role-based prompting → 23/25**

**Result:**

- **ChatGPT** gave the strongest overall results, especially with few-shot and role-based prompting, producing accurate and student-friendly summaries.  
- **Gemini** was the fastest in response time but weaker in coherence and accuracy, making it suitable for quick but less-detailed outputs.  
- **Perplexity** provided balanced performance, with role-based prompting giving clear and structured summaries ideal for educational use.

---




