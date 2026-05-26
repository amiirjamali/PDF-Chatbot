# PDF-Chatbot

This is a simple PDF chatbot project. You can give it a PDF file, ask a question, and it will return the most relevant text from the document.

## How it works

The project uses a simple RAG process:

1. Read the PDF file
2. Extract the text
3. Split the text into smaller parts
4. Convert each part into embeddings
5. Store embeddings using FAISS
6. When a question is asked, find the most similar text and return it

## Tools Used

- FastAPI
- sentence-transformers (`all-MiniLM-L6-v2`)
- FAISS
- PyPDF
- Docker

## Project Structure

```bash
pdf-chatbot/
├── main.py          # API and main app
├── pdf_utils.py     # Load PDF file
├── rag.py           # Chunking, embeddings and search
├── requirements.txt
├── Dockerfile
└── data/            # PDF files
