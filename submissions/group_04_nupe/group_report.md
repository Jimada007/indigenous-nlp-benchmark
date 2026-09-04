# Group 04 — Nupe (Nupeci) — HW1 Report

## Data Sources
- 25 hand-collected documents (Nupe poetry/prose) from Isyaku Bala Ibrahim's blog: https://ibibrahim.blogspot.com — bilingual (Nupe + English translation), English portion stripped during cleaning.
- Additional articles scraped live from Nupe Wikipedia (https://nup.wikipedia.org) via the public MediaWiki API, using our own scraper written and run inside HW1_assignment.ipynb.

## Corpus Metrics
- Total processed sentences: 3,432 (3,088 train / 344 held-out)
- Vocabulary size (V): 7,525 (including <s> / </s> boundary tokens)
- Zipfian exponent (s): 0.92

## N-Gram Model
- Unigram and Bigram models built from scratch (Python dict-based frequency counts)
- Laplace (add-1) smoothing applied to the bigram model
- Bigram perplexity on our own 90/10 held-out split: 1140.09
- Bigram perplexity on instructor's blind test set: 2738.66

## Notes
- Held-out perplexity is high relative to typical English benchmarks, expected given a small training set (3,088 sentences) with a comparatively large vocabulary (7,525 types) — Laplace smoothing is known to over-distribute probability mass across the large number of unseen bigrams in sparse settings. Will re-evaluate once the instructor's blind test file is available.
