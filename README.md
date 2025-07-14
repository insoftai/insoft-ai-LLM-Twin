## 🎯 Overview

This project is a LLM-powered AI twin — an AI system that emulates a person's writing style and knowledge using vector databases, fine-tuned models, and scalable inference.

## 🧠 System Capabilities

- Crawl personal digital data from platforms like Medium, Substack, and GitHub.
- Store and sync unstructured data in MongoDB and Qdrant using RabbitMQ and CDC.
- Process and stream features through Bytewax and Superlinked.
- Train custom LLMs using LoRA/QLoRA with Comet ML monitoring.
- Package and deploy fine-tuned models via AWS SageMaker.
- Serve as a scalable RAG-based API with prompt evaluation via Opik.
- Interact through a Gradio UI for generating style-aligned content.

## 🧱 Architecture

The system is split into four Python microservices:

### 🔍 Data Collection
- Crawlers for Medium, Substack, and GitHub.
- Data stored in MongoDB via ETL.
- CDC pattern used to sync changes via RabbitMQ.
- AWS Lambda packaging for scalable crawling.

### 🧬 Feature Pipeline
- Bytewax-powered stream processing.
- Clean, chunk, embed data and store vectors in Qdrant.
- Superlinked refactor for optimized embedding + Redis indexing.

### 🧠 Training Pipeline
- Generate instruction datasets from raw text.
- Fine-tune LLMs with LoRA/QLoRA.
- Track experiments with Comet ML.
- Evaluate with Opik, store best models on Hugging Face.
- Automated via AWS SageMaker.

### ⚡ Inference Pipeline
- Deploy models from Hugging Face to SageMaker.
- Build REST API with scalable inference.
- Optimize prompts with advanced RAG logic.
- Prompt tracing + evaluation with Opik.
- Bonus: optimize RAG queries using Superlinked.

## 🔧 Tools Used

- Comet ML for experiment tracking
- Qdrant for vector search
- AWS SageMaker for model training + deployment
- Opik for monitoring/evaluation
