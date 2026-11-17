# Nathan_Cual_Milestone_4
# Sentiment Analysis: VADER vs Naive Bayes vs LLM

Compares three sentiment classifiers on Yelp polarity reviews: a rule-based
model (VADER), a classic ML model (TF-IDF + Naive Bayes), and an LLM
(Claude, zero-shot). Models are compared on accuracy, macro-F1, hard-case
accuracy, speed, and cost.

## Setup
1. Install packages:
   pip install pandas scikit-learn matplotlib vaderSentiment nltk anthropic
2. Day 4 needs an Anthropic API key. The notebook asks you to paste it when
   you run it, so no key is stored in the code. You need your own key, and
   the full run costs a few cents.

## Dataset
1. The full Yelp polarity files (train.csv, test.csv) are too large for GitHub.
   Download them from (https://github.com/DrJZhou/Datasets-for-Sentiment-Analysis) and place them in the project folder.
2. The fixed 300-review test set (test_300.csv) and my 30 hard cases
   (hard_cases.csv) are included.
3. Day 1 needs both files, Day 3 needs train.csv, and Days 2 and 4 run with
   only the saved 300-review test set.

## How to run (in order)
1. Day 1: loads the data, creates test_300.csv, EDA
2. Day 2: Tier 1, VADER baseline
3. Day 3: Tier 2, TF-IDF + Naive Bayes
4. Day 4: Tier 3, Claude zero-shot (needs an API key)
5. Day 5: results table, charts, error analysis

## Results
See results_table.csv, chart_macro_f1.png, chart_hard_cases.png, and report.pdf.
Per-model results are in results_vader.csv, results_nb.csv, and results_llm.csv.
