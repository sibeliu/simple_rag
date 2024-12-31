**Basic Retrieval Augmented Generation**

This repository contains a minimal implementation of RAG using a python list of tuples as a vector database, and local embedding and inference through Ollama. 
See it step by step in the jupyter notebook, or run the simple_rag.py file at the command line. 

It has several limitations that would have to be overcome in production: 
- vector similarity is calculated with respect to all elements of the database at every query, which would be prohibitive at scale
- there is no persistent memory of input data
- vector similarity is an imperfect metric that needs to be improved for truly useful results. For example, by using knowledge graphs (which will be our next example)
- local inference is useful only for a few edge cases, like highly secretive clients willing to deal with slow response times in order to maintain full data control

