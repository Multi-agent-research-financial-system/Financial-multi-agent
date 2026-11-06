Document Chunking, Embeddings and Vector Database Design

Project: Multi-Agent Financial Research System
Batch: CSM-B12
Assigned member: Javvadula Shanmukha Aditya Sairam

1. Objective

To design a document processing method that divides extracted financial text into smaller chunks, generates embeddings and stores them in a vector database for efficient retrieval.

2. Proposed Workflow
Receive extracted PDF text.
Clean unnecessary extraction artefacts.
Divide text into smaller chunks.
Add overlap between consecutive chunks.
Generate embeddings.
Store embeddings and metadata in a vector database.
Retrieve relevant chunks based on user questions.
Return retrieved text with source-page information.
3. Chunking Strategy

Two methods will be considered:

Fixed-size chunking

Divides text into chunks of a selected size with overlap.

Structure-aware chunking

Uses headings and document sections to preserve financial report structure.

An initial experiment may use:

Chunk size: 1,000 characters.
Overlap: 200 characters.

These are proposed starting values and must be tested.

4. Metadata

Each chunk should preserve:

Field	Description
Chunk ID	Unique chunk identifier
Document ID	Original PDF ID
Company Name	Company name
Financial Year	Reporting year
Page Number	Original source page
Section Title	Section heading
Chunk Text	Extracted text
Embedding Model	Model used
5. Proposed Technologies
Python
Sentence Transformers
ChromaDB
Retrieval-Augmented Generation (RAG)

The final versions should be selected after compatibility and performance testing.

6. Retrieval Evaluation

The proposed system will be evaluated using:

Retrieval relevance.
Recall@5.
Correct document identification.
Correct page identification.
Retrieval response time.

Recall@5 measures how often relevant evidence appears among the five highest-ranked retrieved chunks.

7. Experiment Plan

Compare different chunking methods using the same financial documents and questions.

Record:

Chunk size.
Overlap.
Chunking strategy.
Embedding model.
Vector database configuration.
Retrieval results.
8. Expected Output

A searchable vector database containing financial document chunks and metadata, allowing the Research Agent to retrieve relevant evidence.

9. Current Status

This is a proposed design. Implementation and experiments are pending.

10. Next Steps
Study chunking methods.
Select an embedding model.
Prepare sample financial documents.
Implement a chunking baseline.
Configure ChromaDB.
Evaluate retrieval quality.