# Student MDP Lesson Materials
## English for Computer Science - Integrated Grammar & Math Exercises

---

## **Lesson 1: Vocabulary & Basic Descriptions (Week 1-2)**

### **Learning Objectives:**
- Learn 20 key technical terms
- Practice present simple tense for describing states and actions
- Use "can/could" for possibilities

### **Key Vocabulary:**

| Term | Definition | Example Sentence |
|------|------------|------------------|
| State | A situation or condition | The student is in the **rested state** |
| Action | Something you can do | The student can take the **action** of studying |
| Transition | Moving from one state to another | There is a **transition** from rested to tired |
| Probability | The chance of something happening | The **probability** is 0.8 or 80% |
| Reward | Points you get for an action | The **reward** for studying is +5 |
| Policy | A rule about what to do | The **policy** tells us which action to choose |
| Terminal | The end point | Exam is a **terminal state** |
| Discount factor | How much we value future rewards | The **discount factor** gamma is 0.9 |

### **Exercise 1.1: Fill in the Blanks**

Complete these sentences using vocabulary from above:

1. The student has three possible _________: Rested, Tired, and Exam.
2. When you are rested, you can choose between two _________: Study or Browse.
3. The _________ of becoming tired after studying is 0.8.
4. If you study well, you get a positive _________ of +10.
5. The _________ state means the game is over.
6. A good _________ tells you the best action in each state.

### **Exercise 1.2: Sentence Building**

Use the present simple tense to describe:

**Pattern:** "When the student [verb], they [result]"

Example: *When the student studies, they become tired.*

Now you try:
1. When the student browses / become tired
2. When the student sleeps / become rested
3. When the student is prepared / take the exam

### **Exercise 1.3: Can/Could for Possibilities**

Complete using "can" or "could":

1. From the rested state, the student _______ study or browse.
2. If you are tired, you _______ sleep to recover.
3. After studying, you _______ go directly to the exam (20% chance).
4. The student _______ not take any actions from the exam state.

---

## **Lesson 2: Conditionals & Logic (Week 3-4)**

### **Learning Objectives:**
- Use if-then structures to describe transitions
- Practice zero and first conditionals
- Express cause and effect relationships

### **Grammar Focus: Conditionals for MDP**

**Zero Conditional** (Always true):
- If + present simple, present simple
- "If you sleep, you become rested" (probability = 1.0)

**First Conditional** (Probable future):
- If + present simple, will + verb
- "If you study, you will probably become tired"

**Conditional with probability:**
- "If you study when rested, there is an 80% chance that you will become tired"

### **Exercise 2.1: Zero Conditional (100% Probability)**

Write sentences for these certain transitions:

1. Sleep → Rested (p=1.0)
   - If _________________________________, you become rested.

2. Browse (when rested) → Tired (p=1.0)
   - If _________________________________, _________________.

### **Exercise 2.2: First Conditional with Probability**

Complete these sentences with probability phrases:

**Useful phrases:**
- "there is an X% chance that..."
- "you will probably..."
- "it is likely that..."
- "you might..."

1. Study (when rested) → Tired (p=0.8)
   - If you study when rested, _________________________________.

2. Study (when rested) → Exam (p=0.2)
   - If you study when rested, _________________________________.

3. Browse (when tired) → Stay Tired (p=0.9)
   - If _________________________________, there is a 90% chance that _________________.

4. Browse (when tired) → Exam (p=0.1)
   - If _________________________________, you might _________________.

### **Exercise 2.3: Cause and Effect**

Connect these using "because" or "therefore":

1. Studying is hard work → You become tired
   - _________________________________________________________________

2. You browse instead of study → You waste time
   - _________________________________________________________________

3. You sleep for 8 hours → You feel rested
   - _________________________________________________________________

### **Exercise 2.4: Complex Conditionals**

Write full sentences describing the decision process:

**Pattern:** "If the student is in [state] and takes action [action], then [result] with probability [p]."

1. Rested + Study → Tired (0.8)
2. Tired + Browse → Exam (0.1)
3. Tired + Sleep → Rested (1.0)

---

## **Lesson 3: Reading Mathematical Notation (Week 5-6)**

### **Learning Objectives:**
- Read set notation aloud
- Express probability functions verbally
- Explain the Bellman equation components

### **How to Read Mathematical Symbols:**

| Symbol | How to Say | Example |
|--------|-----------|---------|
| S = {...} | "S equals the set containing..." | S = {Rested, Tired, Exam} |
| ∈ | "is an element of" / "belongs to" | Rested ∈ S |
| P(A\|B) | "P of A given B" | P(Tired \| Rested, Study) |
| γ | "gamma" | γ = 0.9 |
| π(s) | "pi of s" or "policy of s" | π(Rested) = Study |
| ∅ | "empty set" or "no elements" | A(Exam) = ∅ |
| R(s,a,s') | "R of s, a, s-prime" | R(Rested, Study, Tired) |

### **Exercise 3.1: Reading Set Notation**

Say these aloud, then write them in words:

1. S = {Rested, Tired, Exam}
   - Written: "S equals ________________________________"

2. A(Rested) = {Study, Browse}
   - Written: "The action space ________________________________"

3. A(Exam) = ∅
   - Written: "________________________________"

### **Exercise 3.2: Reading Probability Functions**

Convert to English sentences:

1. P(Tired | Rested, Study) = 0.8
   - "The probability of _________________ given that you are _________________ and you _________________ equals _________________."

2. P(Exam | Rested, Study) = 0.2
   - "_________________________________________________________________"

3. P(Rested | Tired, Sleep) = 1.0
   - "_________________________________________________________________"

### **Exercise 3.3: Reading Reward Functions**

Express these in complete sentences:

**Pattern:** "The reward for [action] when transitioning from [state] to [state'] is [value]."

1. R(Rested, Study, Tired) = +5
   - _________________________________________________________________

2. R(Rested, Study, Exam) = +10
   - _________________________________________________________________

3. R(Tired, Browse, Exam) = -10
   - _________________________________________________________________

### **Exercise 3.4: The Five-Tuple**

Complete this description:

"An MDP is defined by a five-tuple (S, A, P, R, γ) where:
- S is _________________________________________________________________
- A is _________________________________________________________________
- P is _________________________________________________________________
- R is _________________________________________________________________
- γ is _________________________________________________________________"

---

## **Lesson 4: Explaining Calculations (Week 5-6)**

### **Learning Objectives:**
- Describe mathematical operations in English
- Explain the discount factor concept
- Calculate and express expected values

### **Mathematical Language:**

| Operation | How to Say |
|-----------|-----------|
| 0.9² | "zero point nine squared" or "zero point nine to the power of two" |
| 0.9 × 10 | "zero point nine times ten" or "zero point nine multiplied by ten" |
| 5 + 10 | "five plus ten" |
| -10 | "minus ten" or "negative ten" |
| = | "equals" or "is equal to" |

### **Exercise 4.1: Discount Factor Calculation**

Fill in the blanks to explain the discount calculation:

"The discount factor γ _______ 0.9. This means that a reward received two steps from now is worth:

γ² × reward = (_______)² × 10
            = _______ × 10
            = _______

So a reward of +10 in the future is worth _______ right now."

### **Exercise 4.2: Expressing Comparisons**

Complete these comparison sentences:

1. Immediate reward vs. Future reward:
   - "A reward of +10 received now is _______ valuable _______ a reward of +10 received later."

2. Good vs. Bad actions:
   - "Studying when rested (R=+5) is _______ rewarding _______ browsing when rested (R=+1)."

3. Best outcome:
   - "Going straight to the exam prepared (R=+10) gives the _______ reward."

### **Exercise 4.3: Multi-Step Explanation**

Explain this calculation step-by-step in complete sentences:

**Problem:** Calculate the discounted value of a +5 reward received 1 step later.

**Calculation:** γ¹ × 5 = 0.9 × 5 = 4.5

**Your explanation (fill in):**
"First, we _________________________________________________________________
Then, we _________________________________________________________________
Therefore, _________________________________________________________________"

---

## **Lesson 5: Writing Code Comments (Week 7-8)**

### **Learning Objectives:**
- Write clear, concise comments
- Use imperative and descriptive language
- Explain the purpose of code sections

### **Comment Writing Patterns:**

1. **Purpose comments:** "Calculate...", "Initialize...", "Update..."
2. **Explanation comments:** "This represents...", "We use this to..."
3. **Note comments:** "Note that...", "Remember...", "Important:..."

### **Exercise 5.1: Comment the MDP Python Code**

Add comments to this code:

```python
# Student MDP Implementation

S = ['Rested', 'Tired', 'Exam']


A = {
    'Rested': ['Study', 'Browse'],
    'Tired': ['Sleep', 'Browse'],
    'Exam': []
}


P = {
    ('Rested', 'Study', 'Tired'): 0.8,
    ('Rested', 'Study', 'Exam'): 0.2,
}


R = {
    ('Rested', 'Study', 'Tired'): 5,
    ('Rested', 'Study', 'Exam'): 10,
}


gamma = 0.9

```

### **Exercise 5.2: Explain This Function**

Write a short paragraph explaining what this function does:

```python
def calculate_discounted_reward(reward, steps):
    return (gamma ** steps) * reward
```

**Your explanation:**
"This function _________________________________________________________________
_________________________________________________________________
_________________________________________________________________"

---

## **Lesson 6: Speaking & Presentation (Week 11-12)**

### **Learning Objectives:**
- Present the MDP graph orally
- Use transition phrases
- Explain decision-making processes

### **Useful Presentation Phrases:**

**Opening:**
- "Let me explain..."
- "I'd like to walk you through..."
- "This diagram shows..."

**Transitions:**
- "Moving on to..."
- "Now let's look at..."
- "Next, we'll examine..."

**Emphasizing:**
- "It's important to note that..."
- "The key point here is..."
- "Pay attention to..."

**Concluding:**
- "In summary..."
- "To sum up..."
- "The main takeaway is..."

### **Exercise 6.1: Guided Presentation Script**

Complete this presentation about the Student MDP:

"Good morning. Today, I'd like to _______________________ the Student MDP problem.

First, let's look at the states. The student can be in _______ different states: _____________, _____________, and _____________. The exam state is _____________ because _______________________.

Now, moving on to the actions. When the student is rested, they can _____________ or _____________. If they are tired, they can _____________ or _____________.

The key point here is the _____________ function. For example, if the student _____________ when rested, there is an _______% chance that _____________.

Let's look at rewards. Studying gives a reward of _______, which is _______ than browsing. However, if you _____________ unprepared, you get a _______ reward of _______.

In summary, the optimal policy should tell the student to _____________ when rested and _____________ when tired."

### **Exercise 6.2: Describe a Transition Path**

Describe this sequence orally:

**Path:** Rested → (Study) → Tired → (Sleep) → Rested → (Study) → Exam

**Your description:**
"The student starts in _________________________________________________________________
_________________________________________________________________
_________________________________________________________________
Finally, _________________________________________________________________"

### **Exercise 6.3: Answering Questions**

Practice answering these questions about the MDP:

1. Q: "Why is γ less than 1?"
   A: _________________________________________________________________

2. Q: "What happens if the student keeps browsing when tired?"
   A: _________________________________________________________________

3. Q: "Which is better: Study or Browse when rested?"
   A: _________________________________________________________________

---

## **Lesson 7: Collaborative Writing (Week 13-14)**

### **Learning Objectives:**
- Write a structured technical explanation
- Use cohesive devices
- Edit and improve clarity

### **Exercise 7.1: Group Writing Task**

**Task:** Write a 200-word explanation of the Student MDP for someone who has never seen it before.

**Structure to follow:**

**Paragraph 1 - Introduction (40 words):**
- What is the problem about?
- Why is it interesting?

**Paragraph 2 - The Setup (80 words):**
- What are the states and actions?
- What are the rules?

**Paragraph 3 - The Goal (40 words):**
- What are we trying to find?
- Why does it matter?

**Paragraph 4 - Conclusion (40 words):**
- Summary of key points

**Cohesive devices to use:**
- Moreover, Furthermore, In addition (adding information)
- However, On the other hand (contrasting)
- Therefore, Thus, As a result (showing results)
- For example, For instance (giving examples)

---

## **Final Project: MDP Presentation (Week 15-16)**

### **Project Requirements:**

Create a 5-minute presentation that includes:

1. **Slide 1: Title & Introduction**
   - State the problem clearly
   - Explain why it's relevant

2. **Slide 2: The Five-Tuple**
   - Define each component
   - Use correct mathematical notation

3. **Slide 3: State Diagram**
   - Show all states and transitions
   - Label probabilities and rewards

4. **Slide 4: Example Calculations**
   - Show one discount calculation
   - Explain step-by-step

5. **Slide 5: Optimal Policy**
   - State what the best actions are
   - Explain why

### **Assessment Rubric:**

| Criteria | Weight | Description |
|----------|--------|-------------|
| **Vocabulary** | 20% | Correct use of technical terms |
| **Grammar** | 20% | Proper conditionals and descriptions |
| **Mathematical Expression** | 20% | Correct reading of formulas |
| **Clarity** | 20% | Easy to understand |
| **Fluency** | 20% | Smooth delivery, good pace |

---

## **Answer Key (Selected Exercises)**

### Lesson 1, Exercise 1.1:
1. states
2. actions
3. probability
4. reward
5. terminal
6. policy

### Lesson 2, Exercise 2.1:
1. If you sleep when tired, you become rested.
2. If you browse when rested, you become tired.

### Lesson 3, Exercise 3.1:
1. "S equals the set containing Rested, Tired, and Exam"
2. "The action space for the Rested state equals the set containing Study and Browse"
3. "The action space for the Exam state is the empty set" or "There are no actions from the Exam state"

---

## **Additional Resources:**

### **Vocabulary Flashcards**
Create flashcards with:
- Front: Technical term
- Back: Definition + Example sentence from MDP

### **Grammar Practice**
- Khan Academy: Conditionals
- British Council: Cause and Effect
- Purdue OWL: Technical Writing

### **Math Notation Practice**
- Read probability textbooks aloud
- Practice with classmates
- Record yourself explaining formulas

### **AI Tools for Practice**
- **ChatGPT**: "Explain my MDP description and suggest improvements"
- **Grammarly**: Check your written explanations
- **Google Colab**: Write and comment Python code

---

## **Self-Assessment Checklist**

After completing these lessons, you should be able to:

- ☐ Define all 20 key vocabulary terms
- ☐ Use conditionals to describe state transitions
- ☐ Read mathematical notation aloud correctly
- ☐ Explain the discount factor calculation
- ☐ Write clear code comments
- ☐ Present the MDP problem for 5 minutes
- ☐ Answer questions about rewards and policies
- ☐ Work collaboratively to explain technical concepts

---

**Notes for Instructors:**

These materials align with:
- **ESP principles**: Authentic contexts, needs-based learning
- **CLIL framework**: Content + Communication + Cognition + Culture
- **MKO3 outcomes**: LO1-LO5 coverage
- **Assessment**: Maps to 40% project, 20% exercises, 10% participation