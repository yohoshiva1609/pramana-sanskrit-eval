This repository provides Python implementations of over 30 evaluation metrics tailored for **Sanskrit** and other **low-resource languages**

Traditional evaluation metrics such as BLEU, ROUGE, or METEOR were primarily developed for high-resource languages like English. However, **morphologically rich and syntactically flexible languages** such as Sanskrit pose unique challenges, where surface-level similarity is not sufficient to judge translation or generation quality. This repository addresses that gap by offering:

- Classical metrics adapted to Sanskrit word order
- Neural and embedding-based semantic evaluation metrics
- Structural and syntactic metrics for segmentation and parsing
- Model-based metrics like COMET, BLEURT, and XNLI-style entailment scoring

---

## Included Metrics

**Surface-level metrics**  
- BLEU
- METEOR  
- ROUGE-N, ROUGE-L, ROUGE-W, ROUGE-S, ROUGE-SU  
- ChrF, ChrF++
- Translation Edit Rate (TER),Translation Edit Rate with Morphology (TER-M)
- Exact Match (EM)

**Embedding-based Metrics**  
- BERTScore    
- Crosslingual Optimized Metric for Evaluation of Translation (COMET)
- Language-agnostic BERT Sentence Embedding (LaBSE) 
- YiSi-0, YiSi-1, YiSi-2, YiSi-3  
- X(NLI)-R, X(NLI)-D  

**Structural Metrics**  
- UAS, LAS (dependency parsing)  
- Bits Per Character (BPC)


**Ranking & Retrieval-based Metrics**
- Mean Reciprocal Rank (MRR)
- Mean Average Precision (MAP)


**Statistical & Human Agreement Metrics**
- Perplexity
- Token-level F1 Score for Segmentation
- Cohen’s Kappa (κ)
- Krippendorff’s Alpha
- Informedness (Bookmaker Informedness / Youden’s J Statistic)
- Matthews Correlation Coefficient (MCC)
- LEPOR (Length Penalty, Precision, n-gram Position difference Penalty, Recall)


## Prerequisites

Ensure the following packages are installed before running any metric scripts:

| Package        | Purpose                                      |
|----------------|----------------------------------------------|
| `nltk`         | BLEU score & smoothing functions             |
| `numpy`        | Vector operations                            |
| `torch`        | Deep learning + embedding models             |
| `transformers` | BERT, LaBSE, XLM-R, etc.                     |
| `bert-score`   | BERTScore metric                             |
| `evaluate`     | BLEURT score (HuggingFace implementation)    |
| `fasttext`     | Static embeddings for YiSi-1 (Sanskrit)      |
| `unbabel-comet`| COMET metric                                 |
| `bleurt`       | BLEURT scoring model (via GitHub)            |



## 🛠 Installation

1. Clone the repository  
   ```bash
   git clone https://github.com/yourusername/pramana-sanskrit-eval.git
   cd pramana-sanskrit-eval
