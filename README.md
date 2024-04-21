**Overview**
This project is a Python application for retrieving information from a PDF document and answering questions based on the content of the document. It utilizes various natural language processing (NLP) techniques and libraries, including Hugging Face Transformers, to achieve this functionality.

**Features**
Extracts text from a PDF document using PyPDFLoader.
Splits the text into chunks for processing.
Converts text chunks into embeddings using Hugging Face Transformers.
Builds a vector store for efficient document retrieval.
Implements a RAG pipeline
Provides a simple API for querying the system with questions.

**Code Structure**

First we imports necessary libraries and modules for handling PDF documents, text processing, embeddings, vector stores, language models, and interaction with the ChainLit framework.
Then sets up the Hugging Face Hub API token as an environment variable.
then the PDF document is loaded and processed. The text is split into chunks, converted into embeddings, and a vector store is built for efficient retrieval.

repo_id = "tiiuae/falcon-7b"
llm = HuggingFaceHub(repo_id=repo_id, model_kwargs={'temperature': 0.2, 'max_length':1000})
This sets up a Hugging Face language model for question answering, using a specified repository ID and model parameters.
