# Prompt Engineering aur AI Agents ke Notes

Yeh notes video transcript se banaye gaye hain, jisme creator ne concepts ko analogies aur examples se samjhaya hai. Main ne exactly unke examples follow kiye hain, apni taraf se kuch nahi add kiya. Har cheez ko structured tareeke se likha hai, taaki student ke liye asaan ho seekhna. Important learnings aur student ke liye zaroori points bhi include kiye gaye hain.

## Prompt Engineering ka Introduction

- **Prompt Engineering ki Ahmiyat**: Har jagah AI se baat karne ka tareeqa. Asaan alfaaz mein: AI ko sahi tareeke se samjhana taaki woh sahi jawab de.
- **Jagged Intelligence**: AI kuch cheezon mein superhuman hai, lekin kuch mein bohot kharab. Depend karta hai prompt pe.
- **Course Overview**: 6-step framework, context engineering, NanoBanana banana, video editing with VE3, UI/UX design with Llama, applications banana.
- **Learning Point**: AI ki capability badhti ja rahi hai, lekin galat prompt se gadbad ho sakti hai.
- **Student ke Liye Zaroori**: Rozana zindagi mein AI se baat karte waqt prompt ko clear rakho. Practice se seekho.

## Mixture of Experts (MoE) ki Tafseel

- **Dense Network vs MoE**: Pehle single large network (dense) hota tha, jisme billions parameters load hote the ek token predict karne ke liye.
- **MoE ki Research**: Google ne 2023 mein Mistral aur Mixtral mein MoE introduce kiya. Chhote-chhote expert networks banaye gaye.
- **Kaise Kaam Karta Hai**: Input query router network se guzarti hai, jo sahi expert ko select karta hai (e.g., history expert for "Who is the founder of Pakistan?").
- **Router Network**: Probability calculate karta hai kis expert ko activate karna hai.
- **Fayde**: Multiple tasks ke liye alag experts, kam resources use, behtar performance.
- **Nuksan**: Galat prompt se galat expert activate ho sakta hai.
- **Example**: Math ke liye math expert, Python code ke liye coding expert.
- **Learning Point**: Prompt ko clear rakho taaki sahi expert activate ho.
- **Student ke Liye Zaroori**: MoE samjho taaki prompt mein steps define kar sako. Research papers padho for deep understanding.

## 6-Step Prompt Engineering Framework

- **Framework ka Fayda**: 1x se 10x better output. Complex tasks mein iterations kam karta hai.
- **Step 1: Command**: Direct action verb se shuru karo (e.g., Recommend, Analyze, Create). Weak words avoid karo (e.g., Give, Help).
  - Bad Example: "Give me investing advice."
  - Good Example: "Recommend a diversified investment strategy for a moderate-risk investor saving for a home within 5 years."
- **Step 2: Context**: Background, constraints, goals batao. Rule of Three: Who (hu), What, When.
  - Who: Age, income (e.g., 32-year-old earning $90,000/year).
  - What: Specific goal (e.g., buy a home).
  - When: Timeline (e.g., 5 years).
- **Step 3: Logic**: Kaise sochna hai aur respond karna hai batao. Output ke andar relations define karo.
- **Step 4: Role Play**: AI ko expert banao (e.g., "You are a certified financial advisor with 15 years of experience specializing in personal finance and mid-term investment plans.").
- **Step 5: Format**: Output ka structure batao (e.g., Bullet points under 3 sections: Asset Allocation, Rationale, Risk Considerations).
- **Step 6: Ask Questions**: AI se kaho gaps pooche (e.g., "Ask me 10 questions that will help tailor this strategy even more.").
- **Practical Example**: Investment strategy prompt ko step-by-step refine karke better output mila.
- **Learning Point**: Yeh framework AI ki real power unlock karta hai.
- **Student ke Liye Zaroori**: Har step practice karo. Gemini ya ChatGPT pe test karo. Common mistakes avoid karo (e.g., questions se shuru na karo).

## Context Engineering ka Introduction

- **Context vs Prompt Engineering**: Prompt direct LLM se baat hai. Context agent ke liye hai, jo LLM ko use karta hai.
- **Context Engineering ki Definition**: Dynamic system jo runtime pe decide karta hai LLM ko kya prompt dena hai.
- **Fayde**: Right info, format, time pe output. Brand consistency, scalability.
- **Use Cases**: Customer service agents, sales assistants, accounting agents.
- **Components**: Instructions, user input, conversation history, role, constraints, external integrations (e.g., APIs, databases).
- **Analogy**: LLM = CPU (brain), Context = RAM (memory).
- **Learning Point**: Agents mein context manage karna zaroori hai taaki LLM efficient ho.
- **Student ke Liye Zaroori**: Study mode agent banao jaise assignment mein. XML/Markdown format mein context structure karo.

## Important Learnings aur Tips for Students

- **Seekhne Wali Baatein**: Prompt ko clear aur structured rakho. MoE samjho taaki sahi expert activate ho. 6-step framework practice karo.
- **Zaroori Skills**: AI agents banao, context manage karo. Real-world applications mein test karo (e.g., study mode agent).
- **Homework Idea**: 6-step framework use karke investment strategy ya study mode agent banao.
- **Final Tip**: Practice se concepts strong karo. Galtiyon se seekho, iterations karo. AI ki limits samjho.