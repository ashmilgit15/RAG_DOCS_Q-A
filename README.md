# DOCS-Q&A
ask questions about your pdf in english and get Answers powered by AI 

## DEMO

[![Demo](https://asciinema.org/a/oyTxudgQWvh1HFY5.svg)](https://asciinema.org/a/oyTxudgQWvh1HFY5)

## QUICKSTART
paste your groq api key to .env.example (get one free from https://console.groq.com)
currently uses "calculus.pdf" (you can change it to other pdf you like)
if you changed pdf or pdf name,update the name in line 17 in main.py (loader = PyPDFLoader("your-pdf-name.pdf"))

```
git clone https://github.com/ashmilgit15/RAG_DOCS_Q-A.git 
cd RAG_DOCS_Q-A
uv sync #install uv if you dont have it from here: https://docs.astral.sh/uv/getting-started/installation/
python main.py #python3 when mac or linux 
```
NOW ASK QUESTIONS ABOUT YOUR PDF
* NO GUESSING
* NO HALLUCINATIONS
TO EXIT - type "quit"

## FEATURES

* Load any PDF and ask questions in plain English
* Semantic search finds the most relevant chunks from your document
* Powered by Groq LLM + ChromaDB vector store
* Persistent storage — PDF only processed once, instant on subsequent runs

## HOW IT WORKS

First it splits your  document into chunks and store it in chromadb , then it uses HF model (semantic search) to find relevant topic and feeds it as context to the LLM model , the model then replies to your question based on the context

## REQUIREMENTS

* Python 3.11+
* Groq API key (free at https://console.groq.com)

## Built With
- [LangChain](https://langchain.com)
- [ChromaDB](https://trychroma.com)
- [Groq](https://groq.com)
- [HuggingFace Sentence Transformers](https://huggingface.co)