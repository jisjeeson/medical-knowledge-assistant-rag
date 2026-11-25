# Medical Knowledge Assistant | RAG-Based Chatbot

## Project Overview

An AI-powered medical question-answering chatbot that leverages Retrieval-Augmented Generation (RAG) to generate context-based responses from medical reference documents.

The project combines document retrieval, semantic search and Large Language Models (LLMs) with an interactive Gradio interface.

## Key Features

- Medical PDF document loading and preprocessing
- Recursive text chunking with overlapping context
- Semantic embeddings using Hugging Face
- FAISS-based vector storage and similarity search
- Context-based answer generation using Google Gemini
- Prompt engineering and basic prompt injection testing
- Secure API key management using Google Colab Secrets
- Interactive chatbot interface using Gradio
- Basic exception handling

## Technology Stack

| Component | Technology |
|---|---|
| Programming Language | Python |
| RAG Framework | LangChain |
| Document Processing | PyPDF |
| Embeddings | Hugging Face Sentence Transformers |
| Vector Store | FAISS |
| Large Language Model | Google Gemini |
| User Interface | Gradio |
| Development Environment | Google Colab |

## System Architecture

```text
Medical PDF Documents
         ↓
Document Loading and Preprocessing
         ↓
Text Chunking
         ↓
Hugging Face Embeddings
         ↓
FAISS Vector Store
         ↓
User Query → Semantic Retrieval
                    ↓
             Retrieved Context
                    ↓
             Prompt Template
                    ↓
               Gemini LLM
                    ↓
             Generated Answer
                    ↓
             Gradio Interface
```

## How to Run

1. Open `RAG_BOT.ipynb` in Google Colab.
2. Install the required dependencies using the installation cell.
3. Generate a Gemini API key through Google AI Studio.
4. Add the API key to Colab Secrets with the name `GOOGLE_API_KEY`.
5. Enable notebook access for the secret.
6. Upload suitable medical reference documents and configure the document paths.
7. Execute the notebook cells sequentially.
8. Launch the Gradio interface and enter a medical question.

## Example Queries

- What are the symptoms of blood cancer?
- What are the remedies for acne?
- What are the symptoms of diabetes?
- What causes anaemia?

## Security

API credentials are managed using Google Colab Secrets rather than hardcoded into the notebook. Basic prompt injection tests are included to explore chatbot behaviour.

## Future Enhancements

- Document source citations and page-level references
- Conversational memory
- Retrieval and response quality evaluation
- Improved medical safety guardrails
- Hybrid search and document reranking
- Cloud deployment

## Disclaimer

This project is developed for educational and research purposes. It has not been clinically validated and is not intended for medical diagnosis, treatment or as a substitute for professional medical advice.
