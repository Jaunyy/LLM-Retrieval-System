# LLM Retrieval System

This project was a collaboration between **Jonathan Ocampo**, **Aayushma Sapkota**, and **Naiela Islam**.  
It implements a Retrieval-Augmented Generation (RAG) pipeline capable of handling complex queries over messy, multi-format datasets.  
The underlying methodology and design choices are discussed in detail in our research paper: [https://rb.gy/lwmood](https://rb.gy/lwmood).

---

## Overview

We built and ran this system entirely in **Google Colab**.  
The workflow was straightforward:  
1. Mount Google Drive in Colab.  
2. Provide the file or folder path containing the dataset.  
3. The system recursively traverses the directory, indexing all supported file types (PDF, CSV, unstructured text, etc.).  
4. Using RAG techniques, it retrieves the most relevant information and generates context-aware answers to queries.

The system is resilient to irregular directory structures and inconsistent file formatting, enabling it to search through chaotic data collections and still deliver coherent, accurate answers.

---

## Test Data

To evaluate the system, we developed a small benchmark of **5 queries across five categories**:

- **Factual queries**  
  *Example:* “Who were the head coaches from Japan that coached Ruby Sevens?”
- **Comparative queries**  
  *Example:* “How do the Olympic Charters from 1955 and 2025 differ?”
- **Analytical queries**  
  *Example:* “What trends are visible in the Olympic tennis data?”
- **Cross-document queries**  
  *Example:* “What is the correlation between women and men throughout all Olympic sports of 2024?”
- **Exploratory queries**  
  *Example:* “Summarize notable changes in Olympic governance structures over time.”

---

## Key Features
- Works directly in Google Colab for easy setup.
- Accepts entire folders or single files from Google Drive.
- Handles mixed and messy datasets without manual preprocessing.
- Uses Retrieval-Augmented Generation (RAG) for accurate and context-aware responses.

---

## Reference
Full methodology and results are detailed in our research paper: [https://rb.gy/lwmood](https://rb.gy/lwmood)
