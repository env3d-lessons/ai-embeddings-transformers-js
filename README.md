# Sentence Similarity with Embeddings - Exercises

In this set of exercises, you will work with a sentence similarity app and learn how to implement retrieval and generative models using embeddings. You will be guided through making the app more efficient, experimenting with different datasets, and incorporating advanced techniques like Retrieval-Augmented Generation (RAG).

---

### Q1: Pre-process all sentences 

If you noticed the current algorithm, it re-calculates the embeddings for all sentences every time the button is clicked. Make this app more efficient by pre-calculating embeddings for all sentences once. 

### Q2: Use a different dataset

Create a new file called `q2.html`

The file `prompts.csv` contains a list of prompts appropriate for feeding into LLMs such as ChatGPT.
Turn your app into a "prompt generator" by output a prompt from `prompts.csv` that is most
similar to the user's input sentence.

### Q3: Retrieval-Based Q&A (Only for the motivated i.e. aiming for an A and above)

Create a new file called `q3.html`

In this task, you will implement a **retrieval-based question-answering** system using embeddings. Instead of generating answers from scratch, you will use embeddings to retrieve the most relevant question in your dataset and output the associated answer.

First, choose an appropriate dataset from huggingface that contains "Questions and Answers".

1. **Retrieve the Most Similar Question**: After embedding the user’s input question, compare it to the embeddings of questions in your dataset to find the most similar question.

2. **Output the Answer**: Once the most similar question is retrieved, simply output the corresponding answer from your dataset.

**Goal:** Learn how embedding-based retrieval can be used for efficient question-answering without the need for a generative model.

### Q4: Complete with Retrieval-Augmented Generation or RAG (Only if you are extremely motivated i.e. aiming for A+)

Create a file called `q4.html`

In this task, you will implement a **Retrieval-Augmented Generation (RAG)** system using embeddings. Instead of generating answers from scratch, you will use a combination of retrieval and generation.

1. **Retrieve the Most Similar Question**: After embedding the user’s input question, compare it to the embeddings of questions in your dataset (e.g., **Natural Questions** or **Quora Question Pairs**) to find the most similar question.

2. **Generate the Answer**: Once the most similar question is retrieved, use a generative model (like GPT) to elaborate on or refine the answer based on the retrieved context. The generative model should help to provide a more detailed or relevant answer, beyond simply copying the stored answer.

NOTE: You cannot embed openai key (or any other keys) into your javascript, so you will need to create some 
server side component or use a local model, which runs really slow in the browser.

**Goal:** Learn how to integrate retrieval-based methods with generative models to produce more nuanced, 
context-aware responses.
