# TextHarvestAI

TextHarvestAI is a Streamlit research assistant that turns web pages and PDF documents into searchable knowledge. It extracts text, creates embeddings, retrieves relevant passages with FAISS, and uses Gemini to answer questions from the selected content.

## Features

- Extract text from a public web page
- Upload and process multiple PDF documents
- Split long content into retrieval-friendly chunks
- Generate embeddings with Google Generative AI
- Store and search vectors locally with FAISS
- Ask questions through an interactive Streamlit interface

## How it works

`URL or PDF → text extraction → chunking → Gemini embeddings → FAISS retrieval → context-aware answer`

## Technology stack

- Python
- Streamlit
- Google Gemini
- LangChain
- FAISS
- Beautiful Soup
- PyPDF2

## Run locally

```bash
git clone https://github.com/Virajpoolabhavi/TextHarvestAI.git
cd TextHarvestAI/"web scraper"
python -m venv .venv
# Windows: .venv\Scripts\activate
# macOS/Linux: source .venv/bin/activate
pip install -r requirements.txt
```

Create a `.env` file in the application directory:

```env
GOOGLE_API_KEY=your_google_gemini_api_key
```

Start the application:

```bash
streamlit run chatpdf1.py
```

## Current limitations

- The vector index is stored locally and is replaced when new content is processed.
- Web extraction currently focuses on paragraph content.
- This is a portfolio application; production deployment would require stronger validation, error handling, and persistent storage.

## Future improvements

- Add source citations to generated answers
- Support multiple saved document collections
- Add automated tests and URL validation
- Update the retrieval pipeline to current LangChain APIs

## Author

Built by [Viraj Poolabhavi](https://github.com/Virajpoolabhavi).
