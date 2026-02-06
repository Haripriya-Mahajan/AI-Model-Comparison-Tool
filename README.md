# AI Model Comparison Tool

A Python-based platform to analyze and compare **AI Models** using research papers, benchmark CSVs, and Artificial Analysis API data.

---

## Project Overview

This tool helps researchers and enthusiasts explore, benchmark, and compare AI models efficiently. Users can:

- Extract text from PDFs of research papers.
- Compress extracted text for faster AI analysis using the Scaledown API.
- Load benchmark CSVs for performance metrics.
- Fetch AI model evaluations like intelligence, coding, math, speed, and latency from the Artificial Analysis API.
- Compare models by intelligence, speed, or latency.
- Retrieve relevant research and benchmark evidence for queries.

---

## Features

- **PDF Extraction:** Automatically reads uploaded PDFs and extracts text.
- **Text Compression:** Optional compression of text using the Scaledown API for AI research use.
- **Benchmark Analysis:** Load CSV benchmarks for model comparison.
- **Artificial Analysis Integration:** Fetch evaluation metrics of models via API.
- **Intelligent Query Handling:** Supports queries about intelligence, speed, latency, or research evidence.
- **Model Comparison:** Compare canonical AI models and their API variants side by side.

---

## Usage

1. Mount Google Drive in Colab:

```python
from google.colab import drive
drive.mount('/content/drive')
```
2. Install dependencies:

```python
!pip install PyPDF2 pandas requests
```
3. Upload PDFs and CSV benchmarks when prompted.

4. Provide API keys for Scaledown (optional) and Artificial Analysis API (optional).

5. Enter a query to get comparisons or research results.

---

## Example Queries
"Which model is better in intelligence?"

"Top 5 fastest models"

"Latency comparison between GPT-4 and Claude 3 Opus"

"Research on GPT-4 reasoning performance"

---

## Cache Management
Cached data is stored in LLM_Project_Cache in Google Drive:

- pdf_texts.pkl — Extracted PDF text.

- pdf_texts_compressed.pkl — Compressed PDF text.

- benchmark_data.pkl — Benchmark CSV data.

- aa_api_models.pkl — Artificial Analysis API data.

This avoids repeated uploads and API calls.

---

## Tech Stack
- Python 3.x

- PyPDF2, pandas, requests

- Google Colab integration

- Scaledown API for text compression

- Artificial Analysis API for model benchmarking

---

## Author
Haripriya Mahajan

B.Tech CSE-AIML, LNCT

Aspiring Data Scientist
