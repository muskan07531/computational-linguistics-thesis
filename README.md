## EVALUATING LLAMA 3.3 ON MONOLINGUAL AND CODE-SWITCHED SINDHI–ENGLISH INPUTS: A BIDIRECTIONAL MATRIX LANGUAGE ANALYSIS

## About This Project 
This project investigates how large language models handle monolingual and code-switched language varieties. I created 4 custom MCQ datasets (100 questions each), where every question had 4 options (1 correct answer and 3 distractors). All answer options were kept in English across all four conditions.This decision was made because the Matrix Language Frame (MLF) model cannot be meaningfully applied to single-word options, and keeping options consistent in English avoided confounding variables across conditions. Each dataset was fed to LLaMA 3.3 using zero-shot prompting and was prompted to select one answer per question. Responses were scored using a binary system (1 for correct, 0 for incorrect) and performance was then measured based on accuracy scores across all four dataset conditions.

## Datasets
I created 4 original datasets (100 MCQs each):
| Dataset | Description |
|---------|-------------|
| Monolingual English | Standard English MCQs |
| Monolingual Sindhi | Standard Sindhi MCQs |
| English Matrix + Sindhi Embeddings | English-dominant with Sindhi words embedded |
| Sindhi Matrix + English Embeddings | Sindhi-dominant with English words embedded | 

## Methodology
- **Model tested:** LLaMA 3.3 (accessed via Groq API)
- **Prompting strategy:** Zero-shot prompting
- **Scoring:** Binary (1 = correct, 0 = incorrect)
- **Evaluation metric:** Accuracy per dataset condition
- **Statistical tests:** Cochran's Q Test and McNemar's Test
- **Theoretical framework:** Matrix Language Frame (MLF) Model
  
## Key Findings
| Dataset | Accuracy |
|---------|----------|
| Monolingual English | 65% |
| Sindhi Matrix + English Embeddings | 65% |
| English Matrix + Sindhi Embeddings | 63% |
| Monolingual Sindhi | 60% |

Accuracy varied across conditions, however differences were not statistically significant, which may be attributed to the relatively  small sample size (100 MCQs per dataset). The overall trend suggests that English-dominant conditions yielded slightly higher accuracy, 
indicating that LLaMA 3.3 performs more reliably on English and English-influenced inputs than on purely Sindhi text.

## Code
Full code for running the experiment is available in the `/code` folder of this repository.

## Dataset 
Complete datasets are available in the '/data' folder of this repository. 

## Author
[Muskan] — Linguistics Major, Bahria University, Karachi
