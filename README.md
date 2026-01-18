#  Campus-RAG: official-university-info-bot
> **Ensuring institutional trust through grounded AI retrieval.**

##  Project Overview
Students often struggle to navigate the vast and complex landscape of university regulations, leading to missed opportunities and administrative errors. Traditional AI "hallucinates" facts; this system "researches" them.

###  The Problem
- **Search Engines:** Only provide document links without synthesizing an answer.
- **Generic Chatbots:** Lack grounding in official institutional data and provide unverified guesses.

###  The Solution: RAG Architecture
This project implements **Retrieval-Augmented Generation (RAG)** to ensure every answer is:
1. **Grounded:** Derived exclusively from official university PDFs/Text files.
2. **Citable:** Every response includes a source reference (e.g., `Withdraw_Policy.pdf`).
3. **Reliable:** The system is programmed to admit uncertainty if data is missing, preventing misinformation.

---

##  System Blueprint


### 1. Document Ingestion (The "Librarian")
- **Loader:** Scans university repositories for official documentation.
- **Chunker:** Slices large handbooks into "Policy Units" for precise searching.

### 2. Retrieval Engine (The "Searcher")
- **Embeddings:** Converts text into numerical vectors to understand meaning.
- **Vector Store:** Uses **FAISS** to find the exact rule a student is asking about in milliseconds.

### 3. Generation (The "Translator")
- **LLM:** Translates dry, complex legal/policy language into clear, student-friendly answers without changing the facts.

---

##  Technical Stack
- **Language:** Python 3.10
- **Orchestration:** LangChain
- **Vector Database:** FAISS
- **Data:** Official University Regulations (Text/PDF)

---

##  Future Roadmap
- [ ] Multi-lingual support for international students.
- [ ] Secure integration with student transcripts for personalized degree audits.
- [ ] Deployment to campus kiosks via voice-to-text.
