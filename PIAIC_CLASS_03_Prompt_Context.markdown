# Prompt Engineering Class Notes (Roman Urdu)

Yeh notes YouTube class ke transcript se tayyar kiye gaye hain. Main ne sirf woh cheezain shaamil ki hain jo students ke liye zaroori hain aur yaad rakhni chahiye. Examples creator ke diye hue waise hi shaamil hain. Yeh file GitHub ke liye README.md ke taur par use ki ja sakti hai.

## Introduction aur Recap
- Class mein Prompt Engineering ke 12 steps cover kiye ja rahe hain. Pehle 6 steps complete ho chuke hain, baqi 6 baqi hain.
- Aaj ke topics: Common Pitfalls, Examples, Testing & Iteration, Mixture of Experts (MoE), aur 6-step Prompting Framework.
- Image/Video generation costly hai, is liye class mein thora cover kiya jayega, exam mein nahi hoga.
- Exam Prompt Engineering aur Context Engineering pe hoga.

## Common Pitfalls aur Unse Bachne ke Tareeqe
Prompt likhte waqt kuch galtiyan common hain jo results ko kharab kar sakti hain. Yeh avoid karen:

1. **Vague Instructions se Bachna**:
   - Prompt ko general na banayen, specific banayen.
   - Example: "Write a review about movie Conjuring" – Yeh vague hai. Better: "Write a 200-word review about The Conjuring for readers aged 18-30, in casual style, including plot summary and emotional impact."
   - Kyun? LLM intelligent hai lekin assume na karen ke woh sab samajh jayega. Specific instructions den.

2. **Conflicting Instructions se Bachna**:
   - Ek hi prompt mein mukhalif baatein na likhen.
   - Example: "Write a 200-word review" aur phir "Include all details, even if it goes over 2 pages" – Yeh conflict hai.
   - Tip: Ek time pe ek task pe focus karen, consistent rahen.

3. **Negative Instructions (Don'ts) ki Bajaye Positive Instructions (Dos) Istemal Karen**:
   - Don'ts ki lambi list na banayen, jo karna hai woh bataen.
   - Example: "Do not use formal English, do not use difficult words, do not ignore emotions" ki bajaye: "Use simple English, be empathetic, concise, and think from user's perspective. Review should be 100-200 words."
   - Kyun? Don'ts unlimited ho sakte hain, dos specific aur effective hote hain.

4. **Model Limits ko Nazar Andaaz na Karen**:
   - Token limits, output length, context window check karen.
   - Example: Output length 600 tokens set hai, lekin prompt mein "Write 1000-word review" likha – Yeh incomplete rahega.
   - Context Window: Input + Output + Reasoning sab include hota hai (e.g., video upload karne se tokens badh jaate hain).
   - Thinking Mode on hone se extra tokens burn hote hain.

5. **Prompt ko Iterative Improve Karen**:
   - Ek prompt likhen, test karen, improve karen. Versions banayen (e.g., Branching in AI Studio).
   - Example: Movie review prompt ke versions banayen – Ek with Chain of Thought, dusra with Few-Shot.

6. **Best Practices**:
   - Positive instructions pe focus.
   - Testing ke baad constraints add karen.
   - Different techniques combine karen (e.g., System Prompt + Context).

## Prompt Examples aur Improvements
Class mein different use cases pe prompts diye gaye:

1. **Movie Review**:
   - Basic: "Write a review about The Conjuring."
   - Improved: "Write a 200-word review for 18-30 year olds, casual style, include plot, emotions, between 100-200 words, use simple English."
   - Test karen: Different models (Flash, Grok) pe run karen, results compare.

2. **Social Media Post**:
   - Basic: "Write a social media post about coffee."
   - Improved: "Write an engaging Instagram post about a local coffee shop's new seasonal drink. Audience: young adults. Tone: fun and inviting. Format: main text, 3-5 hashtags, call to action. Max 150 words."
   - Techniques: Role-based (You are a marketer), Few-Shot (past posts as examples), Chain of Thought.

3. **Data Analysis**:
   - Basic: "What do customers think about our product?"
   - Improved: "Analyze the following customer reviews and provide insights. Output: Structured report with headings – Overall Sentiment (positive/negative), Key Points, Recommendations."
   - Add: Chain of Thought – "Think step by step for each review."

4. **Code Generation**:
   - Basic: "Write a function to sort a list."
   - Improved: "Write a Python function to sort a list using quicksort. Include type hints, proper OOP concepts. Input example: [3,1,4], Output: [1,3,4]."

## Testing aur Iteration
- Prompt ko test karen: Multiple runs, A/B testing (do versions compare).
- Iteration: Prompt likhen, test karen, improve karen (versions banayen).
- Evaluation Metrics: Consistency, Accuracy, Relevance, Completeness, Format.
- Tools: Google AI Studio, OpenAI Playground, Claude Console.
- Example Sheet: Version, Goal, Model, Temperature, Input, Output, Quality (1-5), Accuracy (0-2), etc.
- A/B Testing: Do prompts same data pe run karen, best choose.

## Mixture of Experts (MoE)
- Traditional LLM: Ek hi model sab jaanta hai (slow, memory heavy).
- MoE: Multiple small "expert" models (e.g., Medical, Math, Coding).
- Router/Gating Model: Input ko analyze karta hai, right expert ko bhejta hai (probabilities use karke, sparse matrix).
- Fayde: Faster inference, less memory, scalable (new experts add karen).
- Example: "Who is founder of Pakistan?" – Router history expert ko bhejta hai.
- Prompting Tip: Clear action verbs use karen taake right expert activate ho (e.g., "You are a history expert").

## 6-Step Prompting Framework
Yeh best way hai prompt likhne ka:
1. **Persona**: Role bataen (e.g., "You are a finance expert").
2. **Task**: Clear command (e.g., "Analyze this data").
3. **Context**: Background den (e.g., audience, constraints).
4. **Examples**: Few-Shot den.
5. **Format**: Output structure bataen (e.g., JSON, bullets).
6. **Question**: AI ko allow karen questions poochne ka (e.g., "Ask me 10 questions to tailor this better").

Example: "You are a marketing expert. Create a strategy for a coffee shop. Context: Target young adults. Examples: Past campaigns. Format: Steps 1-4. Ask questions if needed."

## Assignments/Projects
- Ek project choose karen: Personal Assistant (email drafting), Content Creation, Data Analysis, Code Review.
- 3 prompts banayen (different models: GPT, Gemini, Claude).
- Document: Versions, Input/Output, Metrics.
- GitHub pe upload karen (README.md), tag @penwarsity.

Yeh notes complete hain. Practice karen aur examples try karen!