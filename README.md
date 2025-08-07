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

## Example Query & Response

```bash
Question: [08:03:34] Querying: which city had the highest average temperature in 2012
<ipython-input-1-c8a8a4d18da9>:439: LangChainDeprecationWarning: The method `BaseRetriever.get_relevant_documents` was deprecated in langchain-core 0.1.46 and will be removed in 1.0. Use :meth:`~invoke` instead.
  docs = retriever.get_relevant_documents(question)

================================================================================
Answer (retrieved in 7.03 seconds):
================================================================================
The data provided in Document 4 (/content/drive/MyDrive/FileSystemTesting/Temperatures/stl_monthly_temps_1999_2024.csv) shows that for the year 2012, the annual average temperature for the "stl" location was 61.2°F, which was the highest annual average in the data range from 1999 to 2020. However, without temperature data from other cities, I cannot determine which city had the highest average temperature in 2012.
================================================================================
```

## 📊 Distribution of Indexed File Types

The system was tested on a dataset containing mixed file formats. Below is the distribution of indexed files during evaluation:

<img width="989" height="590" alt="image" src="https://github.com/user-attachments/assets/ccec4b7d-2cdf-48e9-9961-c8fd447b18e5" />


## Reference
Full methodology and results are detailed in our research paper: [https://rb.gy/lwmood](https://rb.gy/lwmood)
