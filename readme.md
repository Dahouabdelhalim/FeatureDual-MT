
# FeatureDual-MT

**Helpful or Harmful? The Dual Role of Linguistic Features in LLM-Based Dialectal Machine Translation**

This repository accompanies our study on the impact of explicit linguistic features in **LLM-based machine translation** between **Algerian Dialect (Darija)** and **Modern Standard Arabic (MSA)**.

## Overview

We investigate whether **Part-of-Speech (POS) tags** and **diacritization** help or harm translation quality in two directions:

- **Algerian Dialect → MSA**
- **MSA → Algerian Dialect**

Using a linguistically enriched subset of the **PADIC** dataset, we evaluate several frontier and open-weight LLMs under multiple settings:  
- without linguistic features  
- with POS tags  
- with diacritics  

## Main Findings

- Linguistic features do **not consistently improve** LLM-based dialectal MT.
- **POS tags** often introduce noise and degrade translation quality.
- **Diacritics** show an **asymmetric effect**:
  - they can improve adequacy in **MSA → Algerian Dialect**
  - they strongly hurt performance in **Algerian Dialect → MSA**
- There is a clear gap between **automatic metrics** and **human judgment**, especially for adequacy.

## Dataset

The dataset used in this study is available in: /Data

It contains:
- parallel sentence pairs  
- POS annotations  
- diacritized variants  

## Scripts

All code and experiment scripts are available in: /scripts

## Models Evaluated

- GPT-4o variants  
- Claude 3.5 Sonnet  
- Gemini 1.5 Pro  
- LLaMA 3.1 8B Instruct  
- Gemma 2 9B Instruct  

## Evaluation

### Automatic Evaluation
- COMET  
- BLEU  
- ChrF++  
- MARBERT-v2 / CamelBERT-MSA  

### Human Evaluation
- Adequacy  
- Fluency  

Two expert annotators used a **3-point scale**:
- 0  
- 0.5  
- 1.0  

Agreement:
- 84.59% (fluency)  
- 86.78% (adequacy)  

## Key Conclusion

Explicit linguistic features should be used **carefully** in LLM-based dialectal MT.  
In many cases, POS tags and forced diacritization introduce noise instead of improving performance.

## Citation
