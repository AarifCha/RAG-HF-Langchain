# RAG-HF-Langchain Project
A RAG set up using HuggingFace model in conjunction to Langchain. The set up is meant to be able to run in google colab (with the most basic pro plan) to avoid costly cloud computing servicies. The HF model can also simply be replaced by OpenAI models using their API.
We then use Streamlit to create a webapp for our QA bot and host it using Ngrok. The app is still run on google colab which makes this a very cost efficient RAG webapp (basically just $1/hour if using A100 GPU on colab).

### HuggingFaceWLangChain Notebook
We go over how to use a HuggingFace model in conjunction to Langchain to set up a RAG with documents in your google drive. We first retrive a model from Huggingface and see test if it works well on hard coded prompts. Then we process pdf documents using Langchain and create chunks and their vector embeddings. To generate the vector embeddings, we use another HuggingFace model. Using these chunks and embeddings, we then create a vector store and see how it performs on some questions. Finally we put it all together and create a QA bot that answers questions based on the uploaded documents. COMPLETED (Might add chat history memeory in this or other notebook)

### GGUF_Model_with_Langchain_LlamaCpp Notebook
We see how to download a .gguf model file and run it on cpu using langchain and llama-cpp, which ports the model to cpp to make the inference faster. But it is still fairly slow.

### Website_RAG_with_Streamlit Notebook
In this notebook, we use Streamlit to create a webapp for our RAG. The app contains two tabs, one where you have a chat window to talk to the chat bot, and one where you are able to upload documents for the RAG to use. The webapp is then hosted using Ngrok which allows you to share the website with others or use the app on your phone while running the model completely on google colab!

NOTE: For more advanced application please check out my [Scientific RAG Gemini](https://github.com/AarifCha/Scientific-RAG-Gemini) repo!
