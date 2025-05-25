# 🧠 Clinical Reasoning in Kenyan Healthcare Using AI
**Data Science Capstone Project**

## 🎯 Problem Statement
Can AI models like GPT-4 replicate or assist clinical reasoning demonstrated by Kenyan healthcare professionals?

---

## 🔍 Objectives
- Extract structured features (e.g., experience) from free-text nurse prompts.
- Evaluate semantic similarity between clinician and LLM responses.
- Assess tone, empathy, and sentiment across responses.
- Measure diagnostic accuracy using SNOMED CT codes.
- Perform manual and automatic evaluation of AI output quality.

---

## 📊 Dataset Overview
- 400 training and 100 test medical vignette samples.
- Metadata includes: County, Health level, Nursing Competency, Years of Experience.
- Text fields: Prompt, Clinician, GPT-4, LLAMA, GEMINI responses.
- Labels: SNOMED diagnostic codes (DDX SNOMED).

---

## 🧼 Preprocessing
- Extracted nurse experience from prompt text using regex.
- Normalized SNOMED CT codes into lists.
- Validated experience metadata against parsed prompt values.

---

## 🧠 Modeling Approach
- Sentence embeddings using `all-MiniLM-L6-v2`.
- Cosine similarity to compare clinician vs AI outputs.
- VADER sentiment analysis to capture empathy/tone.
- Planned lexical metrics: BLEU, ROUGE.

---

## 📊 Exploratory Data Analysis (EDA)
- Counties and facility types well distributed.
- Experience level spans from junior to senior nurses.
- Word clouds generated for prompt overview.
- Diagnosis count per case: mostly 2–5 SNOMED codes.

---

## 📈 Results Summary
- Most prompts matched their metadata fields correctly.
- GPT-4 responses had high cosine similarity (~0.85) to clinician answers.
- Sentiment variation observed: clinicians more cautious/empathic.
- Manual review highlighted tone differences and hallucinations in LLM outputs.

---

## 💬 Discussion
- LLMs capture structure and logic but often miss nuance and context.
- Empathy and clinical tone need specific training or rule-based refinement.
- SNOMED evaluation required for factual correctness beyond text similarity.

---

## ✅ Recommendations
- Deploy AI as assistive, not standalone, tools in clinical settings.
- Implement SNOMED-aware evaluators for fact checking.
- Tune models on regional language/guidelines to increase relevance.

---

## 🔮 Future Work
- Evaluate LLAMA and GEMINI thoroughly.
- Use topic modeling (e.g., BERTopic) to cluster vignettes by theme.
- Extend to multi-turn conversations and follow-up question modeling.
- Build a RAG-based interactive assistant for field nurses.

---

## 📎 Appendix
- Experience parsing from prompt text.
- SNOMED CT parsing utilities.
- Manual review samples.
