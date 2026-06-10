# Environment Setup Guide

## Option 1: Google Colab (Recommended)

1. Open the Colab link from the README.
2. Enable GPU for faster processing:
   - Go to Runtime → Change runtime type
   - Select T4 GPU → Save
3. Run all cells from top to bottom using Shift + Enter.

> Important: If you restart the Colab runtime, you must
> re-run ALL cells from the top, since restarting clears
> all variables from memory.

---

## Option 2: Run Locally

### Prerequisites
- Python 3.9 or higher
- pip package manager
- At least 4GB of free disk space

### Step 1: Clone the Repository
Open your terminal and run:
git clone https://github.com/SaurabhChaudhary046/rag-conversational-bot.git
cd rag-conversational-bot

### Step 2: Create a Virtual Environment
On Windows:
python -m venv venv
venv\Scripts\activate

On Mac/Linux:
python -m venv venv
source venv/bin/activate

### Step 3: Install All Dependencies
pip install -r requirements.txt

### Step 4: Launch the Notebook
jupyter notebook notebook/rag_bot.ipynb

### Step 5: Run Cells in Order
- Phase 1: PDF download and chunking
- Phase 2: Embeddings and FAISS vector database
- Phase 3: Language model integration
- Phase 4: Conversational memory
- Phase 5: Evaluation

---

## First Run Downloads

On first run these are downloaded automatically:

| Item | Size |
|------|------|
| Embedding model (all-MiniLM-L6-v2) | ~90 MB |
| flan-t5-base | ~250 MB |
| flan-t5-large (if upgraded) | ~750 MB |

These are cached after the first download.

---

## No API Keys Required

This project is fully open-source and free.
No OpenAI or paid API keys are needed.
All models download automatically from Hugging Face.

---

## Common Issues and Fixes

| Issue | Fix |
|-------|-----|
| ModuleNotFoundError: langchain.text_splitter | Use langchain-text-splitters package |
| KeyError: text2text-generation | Load T5 directly via T5Tokenizer |
| FutureWarning on embedding dimension | Use .get_embedding_dimension() |
| Colab RAM crash | Restart runtime, use flan-t5-base |
| PDF download blocked | Check internet, re-run cell |
