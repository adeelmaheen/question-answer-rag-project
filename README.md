# Question-Answering RAG Project

This project implements a Retrieval-Augmented Generation (RAG) system for answering questions based on the content of a PDF file. It uses the `langchain` library to load and process the PDF document, preparing it for a question-answering model.

## Project Overview

The core of this project is to build a system that can understand and extract information from a given PDF document to answer user queries. This is achieved by leveraging a RAG architecture, which combines the power of large language models with information retrieval techniques.

## Features

*   **PDF Document Loading**: Loads text content from a PDF file.
*   **Document Processing**: Prepares the loaded document for the RAG pipeline.
*   **Extensible**: Can be extended to include a vector store for efficient retrieval and a question-answering model to generate answers.

## Getting Started

### Prerequisites

Make sure you have Python installed on your system.

### Installation

1.  **Clone the repository:**
    ```bash
    git clone <repository-url>
    cd question-answer-rag-project
    ```

2.  **Install the required dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
    *(Note: You will need to create a `requirements.txt` file with the necessary packages.)*

    Alternatively, you can install the packages mentioned in the notebook directly:
    ```bash
    pip install langchain_community pypdf
    ```

### Usage

1.  Place your PDF file in the root directory of the project. The project currently uses `sample-pdf.pdf` as an example.
2.  Open and run the `main.ipynb` notebook to see the document loading in action.

## How It Works

The `main.ipynb` notebook demonstrates the first step of the RAG pipeline:

1.  **Loading the Document**: It uses `PyPDFLoader` from `langchain_community.document_loaders` to load the `sample-pdf.pdf` file.
2.  **Data Extraction**: The `loader.load()` method extracts the text content from the PDF and loads it into a variable.

The next steps, which are not yet implemented in the notebook, would typically involve:
-   Splitting the document into smaller chunks.
-   Creating vector embeddings for the chunks.
-   Storing the embeddings in a vector database (e.g., FAISS, Chroma).
-   Building a retrieval system to find relevant document chunks for a given question.
-   Using a language model to generate an answer based on the retrieved context.
