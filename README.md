# AI-Model-Comparison-Tool

This project is a Python-based research assistant for analyzing large language models (LLMs). It allows you to extract text from PDFs, compress them for research, load benchmark CSVs, fetch model evaluation data from the Artificial Analysis API, and query models by intelligence, speed, or latency.

Features

Extract text from PDF research papers.

Optional text compression using Scaledown API for faster processing.

Load and cache benchmark CSV data for offline use.

Fetch and cache Artificial Analysis API data for model comparisons.

Query models by:

Intelligence / reasoning ability

Speed (tokens/sec)

Latency (time to first token)

Comparison of canonical LLM families (GPT, Gemini, Claude, LLaMA).

Automatic caching to avoid repeated downloads or compressions.

Search PDFs and benchmarks for query-based evidence.

Installation

Clone the repository:

git clone https://github.com/<your-username>/LLM-Research-Tool.git
cd LLM-Research-Tool


Open the project in Google Colab.

Install required packages:

!pip install PyPDF2 pandas requests

Usage

Mount Google Drive (for caching PDFs, compressed texts, and API data):

from google.colab import drive
drive.mount('/content/drive')


Upload PDFs (or use cached PDFs).

Optionally enter Scaledown API key to compress PDFs for faster research.

Upload benchmark CSV (or use cached CSV).

Enter Artificial Analysis API key to fetch LLM performance data.

Run queries:

user_query = input("Enter your query: ")
print(answer_query(user_query))


Examples of queries:

Which model has lower latency, GPT or Gemini?

Top models by intelligence

Fastest models

GPT performance benchmarks

File Structure
LLM-Research-Tool/
│
├─ main_colab_notebook.ipynb       # Main Colab notebook
├─ README.md                       # Project overview
├─ requirements.txt                # Optional pip dependencies
└─ LLM_Project_Cache/              # Cached PDFs, compressed texts, CSVs, API data

Caching Behavior

PDFs → cached at pdf_texts.pkl

Compressed PDFs → cached at pdf_texts_compressed.pkl (only compressed once per runtime)

Benchmark CSV → cached at benchmark_data.pkl

API Data → cached at aa_api_models.pkl

The system automatically skips compression or API fetch if cached data exists.

Dependencies

Python 3.x

PyPDF2

pandas

requests

Optional APIs:

Scaledown API
 (for text compression)

Artificial Analysis API
 (for model evaluation data)

License

This project is released under the MIT License.
