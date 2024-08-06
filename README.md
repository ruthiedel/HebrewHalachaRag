# Hebrew Halachic Answering System

## Overview

This project provides an innovative system for answering halachic questions using a Retrieval-Augmented Generation (RAG) algorithm. It is specifically tailored for the Yalkut Yosef book, addressing the unique challenges associated with Hebrew language models. The system combines text embedding with efficient search and retrieval to provide accurate halachic responses.

## Features

- **Hebrew Halachic Answering**: Uses the RAG algorithm to generate halachic answers based on the Yalkut Yosef book.
- **Text Processing**: Processes Hebrew text into sections and chunks.
- **Text Embedding**: Utilizes a Hebrew BERT model to create embeddings for text data.
- **Data Storage**: Saves processed texts and embeddings into MongoDB.
- **Search and Retrieval**: Performs search and reranking using FAISS for nearest neighbor search.
- **Interactive Interface**: Provides a Streamlit interface for querying and file uploads.

## Prerequisites

Before running the code, ensure you have the following installed:

- Python 3.x
- PyTorch
- Transformers
- MongoDB
- FAISS
- Streamlit
- `anthropic` library (for Claude-2.1 integration)

## Installation

1. Clone the repository:

    ```bash
    git clone <repository-url>
    cd <repository-directory>
    ```

2. Install the required Python packages:

    ```bash
    pip install torch transformers pymongo faiss-cpu streamlit anthropic
    ```

3. Ensure MongoDB is installed and running on your local machine. Create databases `halacha` and `halacha_embedding` as required.

## Configuration

1. **BERT Model**: The code uses `avichr/heBERT`. Ensure the model is accessible or adjust the `model_name` variable if using a different model.

2. **API Key**: Set the API key for the `anthropic.Client` in the `RAG` function and add api key for cohere as well.



## Code Explanation

- **Text Splitting**: `text_splitter` splits text into chunks based on predefined separators.
- **Embedding**: `embeddingVectors` converts text to embeddings using BERT.
- **Data Preprocessing**: `DataPreprocessing` processes text and stores it in MongoDB.
- **Search and Reranking**: `RAG` performs search and reranking using FAISS and Claude-2.1.

## Innovation

This project is unique in that it addresses the specific challenges of Hebrew language models by tailoring the RAG algorithm to the Yalkut Yosef book. This approach offers a novel solution to providing accurate halachic answers in Hebrew, overcoming the limitations of existing language models.

## Contributing

Feel free to open issues or submit pull requests if you have suggestions or improvements.



## Acknowledgments

- Thanks to the creators of BERT and Streamlit for their valuable tools.
- Special thanks to the MongoDB and FAISS communities for their support.
