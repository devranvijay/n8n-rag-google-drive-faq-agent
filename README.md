# n8n-rag-google-drive-faq-agent

An n8n workflow that lets you ask questions about files stored in Google Drive and get accurate, source-grounded answers instead of manually searching through documents.

## How it works

1. A file is added or updated in a watched Google Drive folder.
2. The workflow downloads the file, splits it into smaller chunks, and converts each chunk into embeddings using the Gemini Embeddings API.
3. Those embeddings are stored in a Pinecone vector index.
4. When a question comes in, the AI Agent searches Pinecone for the most relevant chunks.
5. Gemini generates an answer grounded in the retrieved content, rather than making one up.

## Tools used

- n8n (workflow orchestration)
- Google Gemini API
- Gemini Embeddings
- Pinecone (vector database)
- Google Drive (document source)
- AI Agent node

## Contents

- `RAG Workflow For Faq Documents stored in Google Drive (1).json` - exported n8n workflow, importable directly into your own n8n instance.

## Demo video

A walkthrough covering the setup, configuration, file ingestion, and live question-answering: add your Loom link here.

## Status

This is a working demo. Next step is hardening it for production use (error handling, scaling the ingestion pipeline, and evaluating retrieval quality).
