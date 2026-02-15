# Retrieval-Augmented Question Answering with GPT2 
🚀 Project Overview

This project implements a retrieval-augmented question answering (QA) system and systematically evaluates different generative language models using both:
Semantic similarity metrics (BERTScore)
Language fluency metrics (Perplexity)
The goal is to analyze the trade-off between:
Text quality (fluency)
Semantic alignment
Model architecture differences
##  🔹 Retrieval-Augmented Question Answering with GPT2

This project implements a retrieval-augmented question answering (QA) system using GPT2 as the generative model and Dense Passage Retrieval (DPR) for context retrieval. User queries are first converted into dense vectors, relevant passages are retrieved from the internal document library, and then GPT2 generates context-aware answers.

The system handles preprocessing, tokenization, and embedding of company documents, stores them in a FAISS index, and efficiently retrieves the top-k relevant contexts for each question. Retrieved contexts are concatenated with the user question to form the input for GPT2.

To improve answer quality, the generation process uses parameters such as beam search (num_beams), maximum token length, and length penalties. These parameters were systematically tuned to explore their effects on the conciseness, relevance, and fluency of the generated answers.

Generated answers are evaluated using BERTScore for semantic alignment and Perplexity for fluency, helping to quantify how well GPT2 generates contextually relevant responses. The evaluation highlights the trade-off between fluency and semantic correctness.

This project demonstrates that combining retrieval with generation significantly improves answer relevance compared to using GPT2 alone, providing a robust framework for internal document QA and knowledge management.
