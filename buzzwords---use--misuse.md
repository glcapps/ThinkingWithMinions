## Buzzwords: Use & Misuse

As language-model tooling has spread into business and technical discussions, its vocabulary has followed. Some terms are precise. Others are used loosely, imprecisely, or as placeholders for understanding. In this article, we’ll clear the fog around the most common terms you’ve likely heard in boardrooms, brainstorms, and pitches. This article clarifies common terms by separating definition from misuse.

---

### 🧠 Training  
**What it *means*:** The original, expensive process of creating a model. Billions of words. Massive infrastructure. It is the process by which a model’s parameters are learned from large datasets.

**How it’s *misused*:** “We trained ChatGPT to write our reports.”  
No, you didn’t. You *used* ChatGPT. You may have *guided* it. But unless you're OpenAI, you're not doing training.

**Common confusion:** People think every interaction “trains” the model. It doesn’t. That's called prompting — and the model forgets it as soon as you close the tab.

---

### 🔧 Fine-Tuning  
**What it *means*:** Taking a pre-trained model and adjusting it slightly to specialize it. Like teaching a fluent speaker technical jargon for your industry.

**How it’s *misused*:** “Let’s fine-tune it with some emails.”  
Fine-tuning requires specialized infrastructure and expertise and is not the same as providing examples at runtime.

**Common confusion:** Fine-tuning is *not* copy-pasting your company wiki into the prompt box. That’s a different kind of enhancement — and usually not necessary.

---

### 🎯 Prompt Engineering  
**What it *means*:** Designing precise instructions that help the model do what you want — especially when the stakes or complexity are high.

**How it’s *misused*:** “You just need the right prompt and it’ll solve anything.”  
Prompts matter, but they’re not magic incantations. A vague prompt plus a buzzword doesn’t equal insight.

**Common confusion:** It’s not about syntax tricks — it’s about delegation. It is closer to specifying requirements than issuing commands.

---

### 🤯 Hallucination  
**What it *means*:** When the model confidently makes things up — inventing names, dates, quotes, or just fabricating answers.

**How it’s *misused*:** “The AI lied to us!”  
No, it hallucinated. The model generates plausible output without verifying correctness against an external source.

**Common confusion:** People expect models to be like search engines. They’re not. They’re text predictors with no grounding unless you give it to them.

---

### 📚 Context  
**What it *means*:** The total amount of information the model can “hold in mind” during a session — the information made available to the model during a single interaction.

**How it’s *misused*:** “This model has lots of context, so it knows everything.”  
Nope. Context is *temporary.* Once the chat ends or the limit is hit, it’s gone.

**Common confusion:** Many assume context is infinite — but every word you add eats into the limit. Managing context is a critical skill in LLM use.

---

### 🔡 Token  
**What it *means*:** A chunk of text — not quite a word, not quite a syllable. Models read and respond in tokens.

**How it’s *misused*:** “It can read my 100-page report.”  
Not if that report is more tokens than the model’s limit. Know your model’s budget.

**Common confusion:** Tokens represent processing units. Larger inputs consume more capacity.

---

### 📦 RAG (Retrieval-Augmented Generation)  
**What it *means*:** A technique that feeds external knowledge into the model in real time by retrieving and supplying external material as part of the generation process.

**How it’s *misused*:** “We do RAG, so accuracy is solved.”  
RAG is helpful — but not a silver bullet. Poor documents in, poor answers out.

**Common confusion:** RAG is not search. It’s a system architecture. Just having access to files doesn’t mean the answers improve.

---

### 🤖 Smart  
**What it *means*:** There is no single technical definition. The term is often used as a proxy for capability without specifying which capability is being discussed.

**How it’s *misused*:** “This is the smartest AI yet.”  
“Smart” is vague. Are we talking about creativity? Logic? Memory? Cost-efficiency? Be specific.

**Common confusion:** Bigger doesn’t mean better. Sometimes the “smarter” model gives worse answers — or just more expensive ones.

---

## 🚫 Buzzwords You’re Probably Misusing

- **Training:** You’re *prompting*, not training.
- **Fine-tuning:** Unless you hired a lab, you’re not.
- **Hallucination:** It’s not lying. It’s guessing.
- **Token:** Think of it like text budget, not words.
- **Smart:** Specify the capability or behavior being referenced.

---

Buzzwords are not inherently harmful. Precision is what makes them useful.