# GPTCurationCreator
# Description
This project is a Python-based script that uses Natural Language Processing (NLP) and Machine Learning to process and analyze text documents. The code uploads text documents, splits them into manageable chunks, generates embeddings, performs query searches on the documents, and provides curated responses based on these queries.

# Installation
Install all necessary Python packages with the following commands:
```
!pip install openai langchain faiss-cpu

!pip install langchain

!pip install openai

!pip install python-magic

!pip install chromadb

!pip install unstructured

!pip install tiktoken
```

# Usage
Environment Variables: Make sure to set the OPENAI_API_KEY environment variable with your actual API key.
```
os.environ['OPENAI_API_KEY'] = 'your_openai_api_key'
```
Document Upload: Upload your text document(s) with the files.upload() command, which allows interactive file upload in a notebook environment.

Document Processing: Large documents are split into smaller chunks using the CharacterTextSplitter. Then, the text is tokenized and split into further chunks before embedding is generated.

Embedding Generation: Embeddings for the documents are generated using the OpenAIEmbeddings class.

Query Execution: Run queries on the documents. A query is defined as a string and each document is queried separately. The responses from each document are stored in a list.
```
query = "create curations of publications about eCommerce based on the content in the title"
```
Results: The responses for each document are printed out at the end of the process.

Note: If the document is too large to process in one go, the script will automatically break it down into smaller chunks for processing.

# Warnings
You may encounter warnings when running the script if the number of requested results is greater than the number of elements in the index. This is expected behavior and does not affect the results of the script.
