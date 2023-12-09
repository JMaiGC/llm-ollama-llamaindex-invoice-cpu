# Invoice data processing LLM RAG on CPU with Ollama, LlamaIndex and Weaviate


<a href="https://www.youtube.com/watch?v=Higmr8qMoNk" target="_blank">Update Video URL</a>

___

## Quickstart

### RAG runs offline on local CPU

1. Install Weaviate local DB with Docker:
   
```
docker compose up -d
```

2. Install the requirements: 

```
pip install -r requirements.txt
```

3. Install <a href="https://ollama.ai">Ollama</a> and pull LLM model specified in config.yml

4. Copy text PDF files to the `data` folder

5. Run the script, to convert text to vector embeddings and save in Weaviate: 

```
python ingest.py
```

6. Run the script, to process data with LLM RAG and return the answer: 

```
python main.py "What is the invoice number value?"
```