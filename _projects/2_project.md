---
layout: page
title: AI Agent & RAG Assistant
description: A local AI assistant built with LangChain, LangGraph and ChromaDB
importance: 2
category: AI
giscus_comments: true
---

## AI Agent & RAG Assistant

I've been working on this project to better understand how LLM applications
work beyond simply sending a prompt to a model.

The idea is to build an assistant that can retrieve information from a
knowledge base and use it when answering questions.

### Technologies

- Python
- LangChain
- LangGraph
- Ollama
- Llama 3.2
- ChromaDB
- LangSmith

### How it works

The application takes the user's question and passes it through a small
workflow.

First, the system decides what kind of question it is. When additional
information is needed, it retrieves relevant documents from the vector
database and gives that context to the LLM before generating the answer.

I'm using **LangGraph** to organize the different steps of the workflow
instead of having everything inside one large function.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid
        title="AI assistant"
        class="img-fluid rounded z-depth-1"
        %}
    </div>

    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid
        title="LangGraph workflow"
        class="img-fluid rounded z-depth-1"
        %}
    </div>
</div>

<div class="caption">
    The assistant and the workflow used to process user questions.
</div>

### RAG

For the retrieval part, I'm using **ChromaDB** as the vector database.

The documents are converted into embeddings and stored in the database.
When a user asks something, the application searches for the most relevant
content and passes it to the model as context.

This makes the assistant more useful when the answer depends on information
that isn't directly contained in the model's prompt.

<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.liquid
        title="RAG pipeline"
        class="img-fluid rounded z-depth-1"
        %}
    </div>
</div>

<div class="caption">
    Simplified RAG pipeline used in the project.
</div>

### LangGraph

One of the main reasons I started using LangGraph was to understand how
different steps in an AI application can be connected together.

The workflow can contain different nodes for classification, retrieval,
generation and other processing steps.

This also gives me a better starting point for experimenting with more
advanced agent workflows.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid
        title="LangGraph workflow"
        class="img-fluid rounded z-depth-1"
        %}
    </div>
</div>

### Local LLMs

I'm also experimenting with **Ollama** so that I can run models locally
instead of depending entirely on external APIs.

For this project, I've been using **Llama 3.2** while learning how the
different components of an LLM application fit together.

### What I'm learning from this project

This project is mainly a learning project, but it has helped me understand
several things that are difficult to see when working with a simple
LLM + prompt setup:

- Building a basic RAG pipeline
- Working with vector databases
- Designing workflows with LangGraph
- Connecting LLMs with external data
- Running models locally with Ollama
- Tracing and debugging LLM applications with LangSmith

I'm continuing to extend the project with more structured agent workflows
and validation techniques.