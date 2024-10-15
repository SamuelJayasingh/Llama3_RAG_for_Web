# Llama 3 RAG on Google Colab

This repository contains an implementation of Retrieval-Augmented Generation (RAG) using the **Llama 3** model on **Google Colab**. This project integrates **LangChain** and **Chroma** for document retrieval and embedding, demonstrating how to combine a retrieval system with a powerful language model for answering questions based on a custom dataset.

## Overview

Retrieval-Augmented Generation (RAG) is a technique that enhances the capabilities of a language model by incorporating external knowledge sources, such as documents or web pages. This project leverages RAG by:
- Using **Llama 3** as the language model to generate answers.
- Employing **Chroma** as the vector store for efficient document retrieval.
- Utilizing **LangChain** for chaining language model and retrieval steps.

## Features
- **Document Retrieval**: Retrieve relevant documents based on a user's query.
- **LLM Response Generation**: Generate answers using Llama 3, augmented by the retrieved documents.
- **Google Colab Integration**: The entire setup is designed to run on Google Colab, enabling free and accessible experimentation.

## Setup Instructions

### 1. Clone the repository
```bash
git clone https://github.com/SamuelJayasingh/Llama3_RAG_for_Web.git
cd Llama3_RAG_for_Web
```

### 2. Install Required Packages
Install the necessary Python libraries using `pip`. Ensure your environment includes the following dependencies:
```bash
pip install langchain chromadb flask pandas requests gradio ollama
```

### 3. Open in Google Colab
To run this project in Google Colab:
- Go to [Google Colab](https://colab.research.google.com/).
- Upload the `.ipynb` notebook included in this repository.
- Run the cells to set up the environment and run the Llama 3 RAG model.

### 4. Prepare Your Data
To test the model on your own dataset:
1. Upload your data (URLs or text) in a CSV format.
2. The URLs will be loaded and split into chunks using **LangChain's text splitter**.
3. The model will generate embeddings using **OllamaEmbeddings** and store them in **Chroma** for retrieval.

### 5. Run the Retrieval and Generation Pipeline
After setting up your dataset, you can ask questions to the Llama 3 model. The system will:
1. Retrieve relevant documents from the Chroma vector store.
2. Use Llama 3 to generate an answer based on the retrieved context.

### 6. Using the Gradio Interface
This project includes a Gradio-based interface for interacting with the RAG pipeline. Launch the Gradio UI by running the code, then enter your question in the text box to get a response.

## Example Usage
1. Load your documents (from URLs or CSV files) into the vector store.
2. Ask a question through the interface:
   ```plaintext
   Question: What is the role of LangChain in this project?
   ```
3. The system retrieves relevant documents and Llama 3 generates a response:
   ```plaintext
   LangChain helps to manage and chain the different components of the retrieval and generation process. It connects the document retrieval system with the language model to provide context-aware answers.
   ```

## Key Technologies
- **Llama 3**: The language model used to generate context-aware answers.
- **LangChain**: A framework for integrating LLMs with external sources of data, like databases or APIs.
- **Chroma**: A vector database used to store document embeddings and enable fast retrieval.
- **Google Colab**: A free, cloud-based platform for running Python code, including machine learning projects.
- **Gradio**: A web interface that allows easy interaction with machine learning models.

## Resources
- **LangChain Documentation**: [LangChain](https://langchain.readthedocs.io/)
- **Chroma Documentation**: [Chroma](https://docs.trychroma.com/)
- **Llama 3 Model**: [Meta AI LLaMA](https://ai.facebook.com/blog/large-language-model-llama-meta-ai/)
- **Google Colab**: [Google Colab](https://colab.research.google.com/)

## Contribution

- If you have any suggestions to this README or about the Script, feel free to inform me. And if you liked, you are free to use it for yourself.(P.S. Star it too!! 😬 )

- Your Contributions are much welcomed here!
   > Fork the project
   > > Compile your work
   > > > Call in for a Pull Request

Credits: [Samuel Jayasingh](https://github.com/SamuelJayasingh)

Last Edited on: 15/10/2024


## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
