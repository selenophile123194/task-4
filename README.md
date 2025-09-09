# task-4
Context-Aware Conversational Chatbot
Context-Aware Conversational Chatbot
This notebook details the steps to build a context-aware conversational chatbot using LangChain and ChromaDB, capable of retrieving information from a custom corpus and maintaining conversational history. The final application is intended to be deployed with Streamlit.

Setup Environment and Dependencies
Necessary libraries including langchain, streamlit, chromadb, and sentence-transformers were installed using pip.

Load and Process Data
A dummy corpus file (corpus.txt) was created for demonstration purposes.
The custom corpus was loaded using TextLoader.
The loaded data was split into smaller, manageable chunks using RecursiveCharacterTextSplitter.
Embeddings were created for each text chunk using SentenceTransformerEmbeddings.
The original text chunks and their corresponding embeddings were stored together in a list called corpus_data.
Set up Vector Store
A vector store (ChromaDB) was initialized and populated with the text chunks and their embeddings.

Set up Language Model and Retriever
The Google API key was loaded from Colab secrets.
A language model (ChatGoogleGenerativeAI using the "gemini-1.5-flash" model) was initialized.
A retriever was configured to use the populated vector store.
A RetrievalQA chain was created to combine the language model and retriever for question answering.
Next Steps
The next steps would involve setting up a conversational chain to maintain history and integrating this with a Streamlit application for deployment.

