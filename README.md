# Medical Knowledge Assistant

A Python-based assistant that answers medical questions using evidence from trusted sources. Designed to serve both the general public (with clear, understandable explanations) and medical students/researchers (with technical depth and supporting evidence).

## Current Status

**Phase: Project skeleton — no working implementation yet.**

The initial folder structure and placeholder files are in place. No AI models, retrieval logic, or dependencies have been added. We are building this project step by step.

## Project Structure

```
medical_knowledge_assistant/
│
├── main.py                          # Application entry point (placeholder)
├── requirements.txt                 # Dependencies (to be added later)
├── .env.example                     # API key template
├── .gitignore                       # Files excluded from version control
├── README.md                        # This file
│
├── models/
│   ├── chat_model.py                # Chat/language model setup (placeholder)
│   └── embedding_model.py           # Embedding model setup (placeholder)
│
├── retrieval/
│   └── similarity_search.py         # Similarity search logic (placeholder)
│
├── data/
│   └── sample_medical_documents.py  # Sample documents for testing
│
├── documents/
│   └── README.md                    # Info about future PDF support
│
└── docs/
    └── architecture.md              # Architecture documentation
```

## Planned Features (Not Yet Implemented)

- Accept typed medical questions
- Retrieve relevant information from trusted medical sources
- Generate evidence-grounded answers with citations
- Support uploaded PDFs as knowledge sources
- Handle uncertainty transparently

## Getting Started

No setup steps are needed yet. Dependencies and configuration instructions will be added as the project develops.

## Disclaimer

This project is a learning exercise. It is not a medical device and should not be used for real clinical decisions. Sample documents included are for educational and testing purposes only.
