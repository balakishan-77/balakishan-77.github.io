---
layout: default
---

# Neutrino

> Neutrino is a nutrition assistant based on **RAG**, **reflection** and **langgraph** agentic framework. 

## Assistant
The assistant generates response taking **historical** interaction into account and asks **clarifications** when needed. Leverages an agentic **RAG** tool for generating accurate **content** in the response.

## RAG Tool

*   The RAG agent generates hypothetical questions from the user's query, uses these questions to retrieve **context** from **vector store**
*   Sends the user query and retrieved context to **LLM** for genrating response
*   Calcuates the groundedness and precision **scores** of the LLM response
*   When the scores are lower, repeats the entire process upto a predefined **max** iterations
*   Leverages langgraph for **reflective** agent execution to get a response with high score



[Link to HF space](https://huggingface.co/spaces/balakishan77/hf).

## Porting the solution

*   This architecture of the solution is not coupled to python or streamlit
*   The solution has been ported to SpringBoot and Angular.
*   [Link to SpringBoot Solution](http://74.224.124.209:4200/home).
*   **SpringBoot** takes the place of python and leverages langgraph4j
*   **Angular takes** the place of streamlit
*   This architecture can be implemented in other technologies like **golang** as well where langgraph is supported
