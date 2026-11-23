# Dynamic Math Quiz Generation System (CCP)

**Course:** Analysis of Algorithms (Spring 2026)  
**Instructor:** Mr. Muhammad Usman Sharif  
**Team Members:**
* **Majd Alzuhri** (SAP ID: 71591)
* **Tareq AbyShamala** (SAP ID: 71600)

---

## 📌 Project Overview
This project implements a **Boundary-based Randomized Generation Algorithm** in C++ to solve the real-world educational challenge of dynamically generating non-repetitive, difficulty-scaled math quizzes without relying on memory-intensive static question databases.

### Key Features
* **Dynamic Generation:** Real-time creation of arithmetic problems (`+`, `-`, `*`, `/`, or `Mix`) across multiple difficulty levels (`Easy`, `Medium`, `Hard`, `Mix`).
* **Modular Design:** Built using clean C++ functions, `structs` (`stQuestion`, `stQuizz`), and `enums` (`enQuestionLevel`, `enOperationType`).
* **Instant Evaluation:** Automated real-time grading and final pass/fail statistical reporting.

---

## 🧠 Algorithmic Design & Complexity

### Algorithms & Techniques Used
1. **Boundary-based Randomized Generation ($O(1)$ per item):** Dynamically scales random number ranges based on selected difficulty levels.
2. **Linear Traversal / Iteration ($\Theta(N)$):** Sequentially generates and evaluates $N$ quiz questions.
3. **Direct Array Indexing ($O(1)$):** Uses constant-time lookup arrays for mapping operation symbols and difficulty labels.

### Complexity Summary
* **Time Complexity:** 
  * Best Case: $\Omega(N)$
  * Average Case: $\Theta(N)$
  * Worst Case: $O(N)$
* **Space Complexity:** 
  * Auxiliary Space: $O(1)$
  * Total Space: $O(N)$ (bounded by the static array limit of 100 questions).

---

## 📂 Repository Structure
```text
├── code/
│   └── main.cpp               # Complete C++ source code
├── docs/
│   └── Project_Report.pdf     # Detailed CCP Analysis & AI Reflection Report
└── README.md                  # Project documentation
```

---

## 🚀 How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/Your-Username/Dynamic-Math-Quiz-Algorithm.git
   ```
2. Navigate to the code directory and compile using `g++`:
   ```bash
   cd Dynamic-Math-Quiz-Algorithm/code
   g++ main.cpp -o MathQuiz
   ```
3. Run the executable:
   ```bash
   ./MathQuiz
   ```

---

## 📊 Sample Test Cases

| Test ID | Input (`N`, `Level`, `Op`) | Scenario | Expected Output | Status |
| :--- | :--- | :--- | :--- | :--- |
| **TC-01** | `5, Easy, Add` | Normal | 5 addition questions bounded `[1-10]` scored accurately | Pass |
| **TC-02** | `1, Hard, Mix` | Small | 1 mixed-operation question bounded `[50-100]` | Pass |
| **TC-03** | `100, Med, Sub` | Large | Full capacity (100 questions) generated and evaluated | Pass |
| **TC-04** | `101, Easy, Add` | Boundary | Exceeds static array bound (`100`) | Fail (Known Constraint) |

---

## 🤖 AI Usage & Critical Evaluation Summary
AI tools (Gemini) were utilized responsibly during the planning phase to explore algorithmic alternatives and verify time/space complexity derivations. While the AI's suggestion for randomized bounded generation was accepted for its $O(N)$ space efficiency, suggestions to integrate Machine Learning for adaptive difficulty were critically evaluated and **rejected** as computational overkill for the scope of this problem.