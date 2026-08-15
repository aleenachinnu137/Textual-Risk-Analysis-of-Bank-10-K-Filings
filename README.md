# Linguistic Distress Signals in Bank 10-K Filings

> A classical NLP and statistical study investigating whether changes in the language of bank 10-K filings can provide early signals of financial distress.

## 📌 Overview

This project investigates whether linguistic patterns in annual **10-K filings** contain measurable signals preceding major banking failures.

Rather than treating text merely as unstructured information, the study converts financial disclosures into quantitative linguistic measures and compares the behaviour of distressed and control banks over time.

The analysis uses **56 filings from an 8-bank panel**, covering the period from **2016–2023**, with particular focus on the language contained in risk-related sections.

The central question is:

> **Did the language used by banks change systematically before the 2023 banking failures?**

The study approaches this question using six complementary NLP methods:

1. Loughran–McDonald financial sentiment
2. Readability analysis using the FOG index
3. N-gram frequency analysis
4. TF-IDF lexical drift
5. Sentence-BERT semantic drift
6. LDA topic modelling

These measures are then evaluated against an empirical bootstrap null distribution.

---

## 🎯 Research Question

Financial distress may not be explicitly disclosed in advance. Management may instead reveal changes indirectly through:

- Increased uncertainty
- More cautious or hedging language
- Changes in risk-related vocabulary
- Removal of previously reassuring statements
- Changes in semantic content
- Shifts in the topics discussed

The project therefore tests whether these linguistic signals exhibit unusual behaviour before failure.

---

# 🔬 Methodology

```text
SEC / EDGAR Filings
        ↓
Document Collection
        ↓
10-K Parsing & Cleaning
        ↓
Risk Section Extraction
        ↓
Text Preprocessing
        ↓
┌─────────────────────────────────────┐
│          Six NLP Measures           │
│                                     │
│  LM Sentiment       FOG Readability │
│  N-grams            TF-IDF Drift   │
│  SBERT Drift        LDA Topics     │
└─────────────────────────────────────┘
        ↓
Bank-Year Measures
        ↓
Bootstrap Null Distribution
        ↓
Z-scores / Statistical Comparison
        ↓
Pre-failure Signal Assessment
