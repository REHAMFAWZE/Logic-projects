🧩 Forward & Backward Chaining Rule-Based System
🧠 Overview

This project implements both Forward Chaining and Backward Chaining inference mechanisms for a rule-based expert system.
The system reasons about fruit classification based on various physical characteristics and logical rules, demonstrating classic AI reasoning techniques.

🍎 Problem Description

The system identifies fruit types based on attributes such as:

Shape, color, and size

Diameter measurements

Skin smell properties

Seed count

Citrus classification

It processes rules and facts to infer logical conclusions — such as determining that a fruit is an apple or orange based on its observed properties.

⚙️ Features
🔙 Backward Chaining

Goal-driven reasoning: Starts from a goal and works backward to find supporting evidence.

Detailed tracing: Displays every reasoning step for full transparency.

Numeric condition handling: Supports comparisons like diameter > 2 or diameter < 10.

Recursive reasoning: Automatically proves sub-goals required to reach the main goal.

🔜 Forward Chaining

Data-driven reasoning: Begins with known facts and applies rules to infer new ones.

Rule firing tracking: Keeps a record of which rules were used.

Fact source attribution: Indicates which rule produced each inferred fact.

🧾 File Structure
📦 Forward_Backward_Chaining_System
 ┣ 📜 rules.txt          # Contains IF-THEN rules
 ┣ 📜 facts.txt          # Contains initial known facts
 ┣ 📜 RuleBasedSystem.ipynb  # Main implementation (Forward & Backward chaining)
 ┗ 📜 README.md

🧠 Example Rules

Some of the knowledge base rules include:

IF shape is round AND color is red AND size is medium THEN fruit is apple
IF diameter > 2 AND diameter < 10 THEN size is medium
IF skin_smell THEN perfumed
IF fruit is orange THEN citrus_fruit

🧩 Usage
🔙 Backward Chaining
goal = 'citrus_fruit'
result = backward_chaining_with_trace(rules, facts, goal, proven_facts)

🔜 Forward Chaining
result, final_facts, used_rules, fact_sources = forward_chaining(rules, facts, goal)

🔧 Core Functions
🗂️ Rule & Fact Management

loadRules(filePath): Loads rules from a text file.

loadFacts(filePath): Loads known facts from a text file.

add_fact_uniquely(facts, fact): Adds new facts while preventing duplicates.

evaluate_numeric_condition(condition, facts): Evaluates conditions with numeric comparisons.

🧠 Inference Engines

backward_chaining_with_trace(): Executes backward chaining with detailed reasoning output.

forward_chaining(): Executes forward chaining and tracks used rules.

is_condition_met(): Checks if rule conditions are satisfied.

🧾 Example Output

The system prints detailed reasoning steps such as:

Which rules are being considered

Sub-goals required for inference

Successful condition evaluations

Final derived conclusions and inferred facts

Example:

Trying to prove: citrus_fruit
Checking rule: IF fruit is orange THEN citrus_fruit
Proved: fruit is orange
✅ Goal 'citrus_fruit' successfully proven!

💡 Applications

This rule-based system can be adapted for:

Expert systems for classification and diagnosis

Decision support systems

Educational tools for teaching inference methods

AI reasoning demonstrations

🧰 Requirements

Python 3.x

Jupyter Notebook (optional, for running interactively)

🧠 Key Takeaways

This project demonstrates core AI reasoning techniques using both forward and backward chaining, essential for understanding expert systems, knowledge representation, and logical inference.

👩‍💻 Author

Reham Fawzy Sayed
🎓 Computer Science & AI Student | Logic & Reasoning Enthusiast
📧 [remonaaa734@gmail.com
]
🌐 [https://rehamfawze.github.io/Portfolio/]
