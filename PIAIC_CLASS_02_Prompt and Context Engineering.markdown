# Prompt Engineering Notes: Step 7 to 12 (Based on Lecture Transcript)

## Overview
This README.md contains detailed notes from the YouTube lecture on Prompt Engineering (Steps 7-12). These notes are structured exactly as explained by the instructor (Qasim Bhai, Amin Bhai, Junaid Bhai), using the same examples (e.g., movie review for "Conjuring", social media posts, customer reviews). Key learnings for students are highlighted, including best practices, pitfalls, and essential concepts for AI prompt crafting. Focus on practical application, testing, and iteration.

**Lecture Date/Context**: September 13, 2025 (based on transcript). Covers remaining steps after completing first 6. Upcoming: Context Engineering, Image/Video Generation (light coverage due to cost), Exam on these topics.

**Important for Students**:
- Assume AI (LLM) is not fully intelligent; be specific and structured.
- Always test prompts iteratively; document versions.
- Focus on positive instructions over negatives.
- Understand token limits to avoid incomplete outputs.
- Practice with tools like Google AI Studio for free experimentation.

---

## Step 7: Common Pitfalls and How to Avoid Them
Instructor: Junaid Bhai.  
Focus: Avoid mistakes that degrade prompt output quality. Use examples from movie review prompt ("Write a review about Conjuring").

### Pitfall 1: Vague/Open-Ended Instructions
- **Explanation**: Don't assume LLM is super intelligent; it relies on you for specifics. Vague prompts lead to unpredictable outputs.
- **Example**: Basic prompt: "Write a review about movie Conjuring." – Too open; no word limit, audience, style specified. LLM guesses, results vary across models (e.g., Grok vs. Gemini).
- **How to Avoid**: Be specific and to-the-point.
  - Improved: "Write a review about Conjuring. Word limit: 100-200. Audience: Teens aged 13-18. Style: Engaging and concise."
- **Student Learning**: Vague = Unpredictable. Specific instructions reduce reliance on LLM's assumptions.

### Pitfall 2: Conflicting Instructions
- **Explanation**: Contradictory intents confuse LLM, leading to poor results.
- **Example**: "Review should be 200 words" but later "Include all details, even if over 2 pages." – Conflicts on length.
- **How to Avoid**: Ensure consistency; focus on one task at a time.
- **Student Learning**: One intent per prompt. Test iteratively to catch conflicts.

### Pitfall 3: Over-Reliance on Negative Constraints ("Don'ts")
- **Explanation**: Endless "don't do this" lists grow prompts without limits; better to specify positives.
- **Example**: "Don't use formal English, don't use difficult words, don't ignore emotions." – List can expand endlessly.
- **How to Avoid**: Use positive instructions first.
  - Improved: "Use simple English, be empathetic, concise (100-200 words)."
- **Student Learning**: Positives focus LLM; negatives only where essential. Reduces prompt length.

### Pitfall 4: Ignoring Model Limits (Tokens, Output Length)
- **Explanation**: Prompts exceeding model limits (e.g., output tokens) cause truncation.
- **Example**: Prompt for 1000-word review but output limit set to 600 tokens – Output cuts off. Thinking mode adds extra tokens.
- **How to Avoid**: Check model specs (e.g., Gemini: ~65k output tokens, 1M context window). Set safe limits (e.g., 1500 for 1000 words + thinking).
- **Student Learning**: Context Window = Input + Output + Reasoning. Output Length = Max generated tokens. Experiment with configs.

### Pitfall 5: Assuming Prompts Are Final (No Iteration)
- **Explanation**: One prompt isn't perfect; always improvable via testing.
- **Example**: 20 movie reviews work, but small dataset biases you. Real use cases need variants.
- **How to Avoid**: Create versions (e.g., with Chain of Thought, Few-Shot). Use branching in tools like Google AI Studio.
- **Student Learning**: Iterative process: Version 1 → Test → Version 2 → Compare. Document all for experiments.

**Best Practices Recap (from Last Class)**: Combine techniques (e.g., System Prompt + Few-Shot). Test with real data.

---

## Step 8: Prompt Examples and Applications
Instructor: Junaid Bhai.  
Focus: Apply techniques to real use cases. Experiment with variants.

### Use Case 1: Social Media Post Creation
- **Basic Prompt**: "Write a social media post about coffee."
- **Improved**: "Write an engaging Instagram post about our local coffee shop's new seasonal drink. Audience: Young adults. Tone: Fun. Format: Main text + 3-5 hashtags + CTA. Max 150 words."
- **Techniques to Add**: Role-based (e.g., "You are a marketer"), Few-Shot (past posts as examples), Chain of Thought (if complex).
- **Variants**: Test with/without Chain of Thought or Few-Shot. Compare engagement.
- **Student Learning**: Tailor to platform (e.g., Twitter short, LinkedIn professional). Test on audience.

### Use Case 2: Data Analysis (Customer Reviews)
- **Basic Prompt**: "What do customers think about our product?"
- **Improved**: "Analyze these 10 customer reviews. Provide: Overall sentiment (positive/negative), key points, recommendations. Format: Structured report with headings."
- **Techniques**: Chain of Thought ("Think step-by-step per review"), React (Reason + Act).
- **Testing**: Generate sample reviews via ChatGPT. Compare versions (e.g., with/without Chain of Thought).
- **Student Learning**: Break into steps for accuracy. Use tools like Google AI Studio for branching.

### Use Case 3: Code Generation
- **Basic Prompt**: "Write a function to sort a list."
- **Improved**: "Write a Python function to sort a list. Use typing, OOP concepts. Include example data and usage."
- **Techniques**: Step-Back Prompting (research error causes), Tree of Thoughts (multiple solutions).
- **Student Learning**: Specify language/requirements. For errors: "Error in this API call; suggest fix."

**Key Learning**: Use learned techniques (Best Practices, Advanced Strategies). Create variants and test on same data.

---

## Step 9: Testing and Iteration
Instructor: Amin Bhai.  
Focus: Record, test, evaluate, iterate prompts. Use documentation.

### Process
- **Iteration**: Like making tea multiple times; improve each try.
- **Testing**: Run prompts, evaluate metrics (e.g., accuracy, relevance).
- **A/B Testing**: Compare 2+ variants simultaneously.
- **Documentation**: Use spreadsheets/docs for versions (e.g., Version 1.0: Goal, Model, Params, Input/Output, Quality (1-5), Accuracy (0-2)).

### Example Setup (Google Sheet/Doc)
- Columns: Version, Date, Goal, Model (e.g., GPT-5), Params (Temp, Top-P/K), Input, Output, Quality (1-5), Accuracy (0-2), Relevance (0-2), Completeness (0-2), Format (0-2), Tone/Notes.
- Test: Analyze 10 restaurant reviews (mock data from ChatGPT). Variant A: Basic prompt. Variant B: With System Prompt + Rules.

### Evaluation Metrics
- Consistency: Same output on repeats?
- Following Instructions: Adheres to rules?
- Creativity: If needed (adjust temp).
- Factual Accuracy: No hallucinations.
- **Structured Output**: Prefer JSON/XML for machine-readable results.

**Student Learning**: Document everything. Use A/B for comparisons. Advanced: Summarize history for long contexts.

---

## Step 10: Advanced Tips and Resources
- **Context Management**: Summarize history; break complex tasks (Chain of Thought).
- **Multimodal Prompting**: Combine text + images (e.g., "Specify spicy dishes in this menu image").
- **Prompt Chaining**: Break into steps (e.g., Research → Outline → Write).
- **Resources**: OpenAI Playground, Google AI Studio, Anthropic Console, Communities (Discord, Hugging Face), Papers/Guides.

**Student Learning**: Experiment with tools. Join communities for updates.

---

## Steps 11-12: Building a Prompt Library + Mixture of Experts (MoE)
Instructor: Qasim Bhai.  
Focus: Create reusable prompts; understand MoE for efficient AI.

### Building Prompt Library
- Template for tasks (e.g., Email Draft: Variables like recipient, subject).
- Document versions in docs/sheets.
- Projects: Personal Assistant (Email Scheduler), Content Creation, Data Analysis, Code Review. (Submit 3 versions on LinkedIn, tag channel).

### Mixture of Experts (MoE)
- **Traditional LLM**: Single model (1T params) – Slow, memory-heavy.
- **MoE**: Divide into experts (e.g., Medical, Math). Router/Gating model selects top experts (sparse matrix, top-K=2-8).
- **Benefits**: Faster inference (load only relevant experts), scalable, efficient memory.
- **Implementation**: Used in GPT-5, Grok, Gemini. Prompt clearly: Split tasks (bullets/steps) to activate right experts.
- **6-Step Framework**: Clear Command + Context + Logic + Persona + Format + Questions (Ask AI for clarifications).

**Student Learning**: Split tasks in prompts. Practice MoE-aware prompting. MoE reduces costs; apply in projects.

---

## Q&A Highlights (Key Learnings)
- **Params**: Learned weights (wx + b) from training data.
- **Reasoning/Thinking**: Improves accuracy via step-by-step (Chain of Thoughts).
- **Few-Shot vs. Fine-Tuning**: Temporary examples vs. permanent model update.
- **Tokens**: Depend on input/output/processing; good prompting minimizes waste.

**Assignment**: Build 1 project (3 prompt versions). Document and share on LinkedIn.

**Resources**:
- [Google AI Studio](https://aistudio.google.com/)
- [OpenAI Playground](https://platform.openai.com/playground)

*Notes by Your Name – Download and edit as needed.*