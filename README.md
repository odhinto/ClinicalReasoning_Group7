# 🧠 Clinical Reasoning in Kenyan Healthcare Using AI (Enhanced Version)

This enhanced markdown outlines a capstone project using NLP to evaluate whether AI models like GPT-4 can emulate the reasoning of real clinicians in Kenya.

---

## 🎯 Problem Statement
Can we build models or evaluation tools to measure how well AI can replicate human clinical judgment in low-resource healthcare settings?

---

## 🧪 Objectives
- Extract structured information (like nurse experience) using RegEx.
- Use sentence embeddings to compare AI vs human responses.
- Analyze tone and empathy with sentiment analysis.
- Use NLP foundations (Bag-of-Words, TF-IDF) for text statistics.
- Apply classification (predict medical specialty from prompt).

---

## 🗃️ Dataset Summary
- 400 training samples, 100 test samples.
- Fields: Prompt, Clinician response, GPT-4, LLAMA, GEMINI.
- Metadata: County, Health level, Nursing Competency, Experience.
- Labels: SNOMED CT diagnostic codes.

---

## 🔧 Techniques Used

### ✅ Regular Expressions
Used to extract number of years of experience from nurse prompts.

### ✅ Word Embeddings
Used `SentenceTransformer` (MiniLM) to compare how close AI and clinician answers are in meaning.

### ✅ Bag-of-Words (BoW)
Used `CountVectorizer` to find most common words and build a word frequency matrix.

### ✅ Corpus Statistics
Counted tokens, characters, vocabulary size, and average words per clinician response.

### ✅ TF-IDF Vectorization
Used `TfidfVectorizer` to detect which words carry more weight in responses.

### ✅ Text Classification
Built a Naive Bayes classifier to predict the medical specialty (Clinical Panel) based on the prompt.

---

## 📊 Evaluation Metrics
- **Cosine Similarity** (semantic overlap)
- **Sentiment Score** (using VADER)
- **Classification Report** (precision, recall, F1)

---

## 🔍 Manual Review
Spot-checked AI responses against human clinician answers for reasoning quality and tone.

---

## 💡 Key Insights
- GPT-4 had high similarity but sometimes lacked empathy.
- Nurse experience in the prompt matched metadata ~100%.
- SNOMED codes varied per case but were properly extractable.

---

## 📈 Recommendations
- Use AI as decision support only, not as replacements.
- Highlight and validate medical facts with SNOMED-based rules.
- Train AI on regional data for cultural and clinical safety.

---

## 🔮 Future Work
- Evaluate LLAMA and GEMINI on same metrics.
- Use topic modeling (e.g., BERTopic) to group vignettes.
- Add multi-turn Q&A and chat capability.
- Develop a real-time RAG system for field use.

