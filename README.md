<h1 align="center">Sectoral ReAct Agent – Digital Transformation Assistant</h1>

## 📌 Project Overview
This project implements a **sector-specific intelligent agent** focused on **Digital Transformation in Businesses**.  
The goal is to move beyond static question-answering and build a system that **retrieves, reasons, and filters knowledge** using a Retrieval-Augmented Generation (RAG) approach.

The agent evaluates whether a user question is **within the scope of the sectoral knowledge base** and retrieves the most relevant contextual information when applicable.

## 🎯 Project Goal
- Design a **sectoral AI assistant** for the field of **Digital Transformation**
- Use **technical documents** instead of fixed answers
- Filter **out-of-domain questions**
- Provide **traceable and explainable retrieval results**

This project follows the **ReAct Agent design philosophy**, focusing on reasoning over retrieved information.

## 🏢 Selected Sector
**Digital Transformation in Businesses**

### Reason for Selection
- Requires **strategic, organizational, and technical knowledge**
- Highly relevant to modern enterprises
- Suitable for semantic similarity and reasoning-based retrieval

## 📂 Dataset & Data Source
- **Data Type:** Plain text document  
- **File:** `data/digital_transformation.txt`  
- **Content:**  
  Analysis of digital transformation impacts on:
  - Business strategy
  - Organizational culture
  - Decision-making processes
  - Competitive advantage
  - Human factor and employee adaptation

The document is manually curated and used as a **domain-specific knowledge base**.

## 🧠 Methodology
### ✅ Method Used: RAG (Retrieval-Augmented Generation)
The system:
1. Splits the document into fixed-size text chunks
2. Converts chunks into vector embeddings
3. Stores embeddings in memory
4. Retrieves the most relevant chunk using cosine similarity
5. Rejects out-of-domain questions using a similarity threshold

## 🧩 Core Components

### Text Chunking
- Chunk size: **400 words**
- Ensures semantic coherence

### Embedding Model
- `sentence-transformers/paraphrase-multilingual-MiniLM-L12-v2`
- Supports **Turkish language**

### Similarity Filtering
- Threshold: **0.35**
- Prevents hallucination and irrelevant answers

## 🧪 Benchmark Scenarios

### Scenario A – In-Domain Questions
Examples:
- Digital transformation strategy risks
- Organizational resistance
- Impact on competitiveness
- Human factor in transformation

### Scenario B – Out-of-Domain Questions
Examples:
- French Revolution
- Quantum computing

Out-of-domain questions are **explicitly rejected**.

## 🔍 Output Details

For each user query, the system displays the following information:

- **User Question**: The original question provided by the user.
- **Retrieved Context**: The most relevant document chunk retrieved using semantic similarity (if the question is in-scope).
- **Similarity Score**: A numerical score indicating how closely the question matches the retrieved document content.
- **Out-of-Scope Warning**: If the similarity score is below the defined threshold, the system notifies that the question is outside the document scope.

## 📊 Output Image
  ![Image](https://github.com/user-attachments/assets/8be15391-6179-498c-82ec-bf64526d5f11)

## 🤝 Contributing
Contributions are welcome! 

## 📡 Contact
For any queries or collaborations, feel free to reach out!

🌐 GitHub: [zeynepcol](https://github.com/zeynepcol)  
👤 LinkedIn: [zeynep-col](https://linkedin.com/in/zeynep-col/)
