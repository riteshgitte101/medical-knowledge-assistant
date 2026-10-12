# Architecture — Medical Knowledge Assistant

## High-Level Flow (Planned)

```
Medical question
    │
    ▼
Generate query embedding and compare with document embeddings
    │
    ▼
Retrieve the most relevant passages
    │
    ▼
Chat model generates an evidence-grounded answer
    │
    ▼
Answer with source references
```

This is the intended direction for the project. It is **not a working implementation yet**.

---

## Components and Their Responsibilities

### `main.py`
The entry point. Will eventually tie together the retrieval and chat model steps: accept a question, search for relevant text, pass it to the model, and display the answer.

### `models/chat_model.py`
Sets up the language model (chat model) that generates answers. The model provider has not been chosen yet. This module will use LangChain to initialize and call the model.

### `models/embedding_model.py`
Sets up the embedding model that converts text into numerical vectors. These vectors allow us to measure similarity between the user's question and stored medical documents.

### `retrieval/similarity_search.py`
Implements the search step. Takes the user's question, computes its embedding, compares it against document embeddings using cosine similarity, and returns the most relevant passages.

### `data/sample_medical_documents.py`
Contains a small set of sample medical text passages for early development and testing. These are clearly labelled as educational samples, not verified medical guidance.

### `documents/`
Will hold uploaded PDF files in a later stage. PDF processing is not implemented yet.

---

## What the Initial Skeleton Contains

- Folder structure with placeholder files for each component.
- Sample medical documents for testing (clearly marked as educational, not medical advice).
- Documentation of the intended architecture and data flow.
- Project configuration files (`.env.example`, `.gitignore`, `requirements.txt`).

## What We Can Implement Next (Concepts Already Studied)

- Embedding text using a chosen model and computing cosine similarity.
- Basic similarity search: given a question and a set of documents, find the most relevant ones.
- Calling a chat model through LangChain to generate an answer from retrieved text.
- Simple question-answer loop in `main.py`.

## What Remains for Future Learning and Development

- **PDF ingestion:** Loading, parsing, and splitting PDF documents into searchable chunks.
- **Trusted source management:** Tracking and verifying where each piece of information came from.
- **Citation verification:** Ensuring the model's answer accurately reflects the retrieved evidence.
- **Medical safety checks:** Detecting questions that require professional medical advice and responding appropriately.
- **Vector database:** Storing embeddings efficiently for larger document collections (currently we will use in-memory search).
- **Prompt engineering:** Designing prompts that produce reliable, well-structured, audience-appropriate answers.
- **User interface:** A frontend for interacting with the assistant (not planned for the initial stages).

---

## Disclaimer

This project is a learning exercise built by a B.Tech IT student. It is not a medical device and must not be used for real clinical decisions.
