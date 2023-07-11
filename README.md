# Using NLP to Interpret Large Volumes of Scientific Text

A weakly-supervised Machine Learning algorithm that can quickly and accurately summarize the state of the research in a field using Natural Language Processing and Dynamic Topic Modeling by analyzing a dataset of published abstracts pertaining to that topic.

## Abstract

Natural Language Processing is an effective tool for analyzing large volumes of text effectively. However, most scientific articles contain sophisticated language that can be difficult to understand effectively and quickly. To expedite this, I tuned a model that can quickly classify abstract datasets about scientific topics into specific subcategories. Using the ArXiv corpus with over 2.2 million abstracts, I created a dataset of climate change articles, on which I ran pretrained HuggingFace models. Using observational and quantitative data (ROUGE, Cosine Similarity, etc.), I tuned the parameters of various keyword extraction models and analyzed the keyword frequency of the dataset. Then, using the BERTopic model with various embedding techniques (SentenceTranformers, spaCy, etc.), I classified the dataset into clusters which could be individually analyzed. I used abstractive and extractive summarization models on each cluster to concisely describe the general progress of particular climate change topics. Using dynamic topic modeling, I then plotted the prevalence of different topics over time, which provided insight into the interest in climate change topics over the past decade. By finding relationships between hyperparameters and the size of the abstract dataset, I generalized the model for various input sizes. This weakly-supervised algorithm allows analysts and researchers to quickly derive general conclusions about specific scientific topics and visualize their relevance in the scientific community over time.

# Introduction

- Scientific research articles can be difficult to understand thoroughly since they often contain sophisticated language that requires extensive knowledge in the topic covered. 

- However, many roles in various fields of science necessitate the ability to quickly understand the overall state of the research in a particular topic, which can be a conglomeration of thousands of scientific articles. 

- Natural Language Processing, which includes sub-processes such as Topic Modeling, Keyword Extraction, and Summarization, is an emerging tool that is frequently used to train AI models to interpret text. 

- In the past, AI/ML researchers have used Natural Language Processing models in order to summarize and analyze large corpora of text in order to build artificially intelligent search engines. However, due to the large size of the training dataset, this often leads to general conclusions that fail to provide the details that thorough research analysis requires. 

- This study aims to develop a weakly supervised machine learning algorithm that can quickly and accurately summarize the state of research in a field using Natural Language Processing and Dynamic Topic Modeling by analyzing a dataset of published abstracts pertaining to that topic.

# Methodology

<img width="775" alt="image" style="text-align:center;" src="https://github.com/Ishan314/dlp_model/assets/53442182/aecb43a2-54b0-435d-9757-f3e1c531e436">

