---
layout: page
title: Book Bot
description: RAG LLMs for book recs
img: assets/img/6.jpg
importance: 1
category: fun
---

### 📚 NYT Bestsellers Q&A with Retrieval-Augmented Generation

This is a fun personal project that I came up with to serve my own needs with good book recommendations! Here, I apply LLMs to create an intelligent Q&A system for exploring past New York Times bestsellers. Using Retrieval-Augmented Generation (RAG), the system retrieves relevant book details from a curated dataset of all the NYT bestsellers between 2010 and 2024 and generates (hopefully!) precise answers to user queries. The end product is a "book bot" that helps you search for record-breaking bestsellers or personalized recommendations.

### 🤔 Design considerations

There are two options for how to store data 

1. *Memorization* 
    - What this means: Store knowledge within LLM by fine-tuning)
    - Pros:
        - Fast inference speed (no retrieval overhead)
        - Less training complexity (need to train only one model)
    - Cons:
        - Limited scalability (must fine-tune every time data is added)
        - High resource requirement (larger model required for memorization)
        - May struggle with robustness if not trained well
    - Best for: Suited for fact-based questions encoded in training
2. *Retrieval-Augmented Generation (RAG)* 
    - What this means: a hybrid approach where one model retrieves relevant information and another one generates an answer
    - Pros:
        - Highly scalable and dynamic (new data can be added without fine-tuning)
        - Lower resource requirements since lightweight retrieval models can reduce load on the generator
    - Cons:
        - Slower inference speed due to retrieval step
        - Higher training complexity since we need to train both a retriever and a generator
    - Best for: diverse or open-ended questions requiring flexible, dynamic context

For our application, we will be using ***RAG*** for a scalable and lightweight deployment, at the expense of slow inference. 

### ⛏️ Data Acquisition

This project uses data from the NYT Books API and Google Books API to create a comprehensive dataset of past NYT bestsellers. The NYT API was used to identify bestsellers alongside their details like title, author, and NYT book descriptions, while the Google Books API supplied additional, widely-used book descriptions. To stay within API rate limits, a cron job was set up to retrieve bestseller data year by year, spanning 2010 to 2024, with daily updates ensuring a smooth and efficient data collection.

