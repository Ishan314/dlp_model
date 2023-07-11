# Using NLP to Interpret Large Volumes of Scientific Text

A weakly-supervised Machine Learning algorithm that can quickly and accurately summarize the state of the research in a field using Natural Language Processing and Dynamic Topic Modeling by analyzing a dataset of published abstracts pertaining to that topic.

## Abstract

Natural Language Processing is an effective tool for analyzing large volumes of text effectively. However, most scientific articles contain sophisticated language that can be difficult to understand effectively and quickly. To expedite this, I tuned a model that can quickly classify abstract datasets about scientific topics into specific subcategories. Using the ArXiv corpus with over 2.2 million abstracts, I created a dataset of climate change articles, on which I ran pretrained HuggingFace models. Using observational and quantitative data (ROUGE, Cosine Similarity, etc.), I tuned the parameters of various keyword extraction models and analyzed the keyword frequency of the dataset. Then, using the BERTopic model with various embedding techniques (SentenceTranformers, spaCy, etc.), I classified the dataset into clusters which could be individually analyzed. I used abstractive and extractive summarization models on each cluster to concisely describe the general progress of particular climate change topics. Using dynamic topic modeling, I then plotted the prevalence of different topics over time, which provided insight into the interest in climate change topics over the past decade. By finding relationships between hyperparameters and the size of the abstract dataset, I generalized the model for various input sizes. This weakly-supervised algorithm allows analysts and researchers to quickly derive general conclusions about specific scientific topics and visualize their relevance in the scientific community over time.

## Introduction

- Scientific research articles can be difficult to understand thoroughly since they often contain sophisticated language that requires extensive knowledge in the topic covered. 

- However, many roles in various fields of science necessitate the ability to quickly understand the overall state of the research in a particular topic, which can be a conglomeration of thousands of scientific articles. 

- Natural Language Processing, which includes sub-processes such as Topic Modeling, Keyword Extraction, and Summarization, is an emerging tool that is frequently used to train AI models to interpret text. 

- In the past, AI/ML researchers have used Natural Language Processing models in order to summarize and analyze large corpora of text in order to build artificially intelligent search engines. However, due to the large size of the training dataset, this often leads to general conclusions that fail to provide the details that thorough research analysis requires. 

- This study aims to develop a weakly supervised machine learning algorithm that can quickly and accurately summarize the state of research in a field using Natural Language Processing and Dynamic Topic Modeling by analyzing a dataset of published abstracts pertaining to that topic.

## Methodology

<img width="75%" alt="image" style="text-align:center;" src="https://github.com/Ishan314/dlp_model/assets/53442182/c7a71f2d-b520-46bd-8800-db5b02fd933e">

## Results

<img width="75%" alt="image" src="https://github.com/Ishan314/dlp_model/assets/53442182/46eb9185-bc4a-429b-bded-24c47065b4b8">

Figure 1. Keyword Frequency. The most common extracted keywords from the initial ArXiv dataset.



<img width="75%" alt="image" src="https://github.com/Ishan314/dlp_model/assets/53442182/f8f8a142-d2d5-47f1-8b8d-f97161e67242">

<p width="75%">Figure 2. Document Clustering. A visual representation of how the documents are clustered.</p>



<img width="75%" alt="image" src="https://github.com/Ishan314/dlp_model/assets/53442182/37ee7987-557b-4323-a41a-8f6e75bbc672">

<p width="75%">Figure 3. Dynamic Topic Modeling. The frequency of climate change topics from ArXiv from 2008-2022.</p>

## An Example Summarization Result

**Topic 6 Summarization (ice extent, Antarctic ice)**:
The Arctic sea-ice cover has been diminishing over the past decades, raising the question of whether the remaining ice will disappear abruptly. We show that the loss of Arctic sea ice would not follow the conceptual predictions of the theory of dynamical systems, and that characteristic trends can be expected in the future.

The summarization provides insight into the subtopic, what is being covered currently, as well as what is expected in the future. 

## Discussion and Future Steps

- The weakly-supervised NLP approach is great at quickly and accurately summarizing large amounts of scientific text and providing insight into trends in that scientific field.

- However, most of the parameters used in the algorithm are specific to the topic at hand, Climate Change, and depend on variable aspects such as the size of the inputted abstract dataset and the number of distinct subtopics in the field.

  - To fix this, one could find relationships between the values of the parameters as well as variables such as dataset length and formulate equations relating the two quantities.

  - These equations could be used in the program to make it adaptive, allowing it to effectively parametrize itself and run effectively on datasets of any size and topic, be it broad or narrow.

- In addition, various embedding techniques used to reduce inconsistencies in the results could significantly improve the topic modeling and summarization of the model but could also drastically impact its adaptability.

- GPU optimization can lead to significantly faster runtimes and could also result in high levels accuracy in the topic modeling

- Currently, the abstractive summarization is performed on the top three most representative documents of the topic, and accounted for the entire cluster will provide more insight into the subtopic.

## Acknowledgements

I am truly grateful for Dr. Azucena Rodriguez, the IMSA SIR office, and Argonne National Laboratory for making this research possible. I also thank Dr. Prasanna Balaprakash for guiding me throughout the research project.  

## References

1. Dong, X., & de Melo, G. (2019). A robust self-learning framework for cross-lingual text classification. Proceedings of the 2019 Conference on Empirical Methods in Natural Language Processing and the 9th International Joint Conference on Natural Language Processing (EMNLP-IJCNLP), 6306–6310. https://doi.org/10.18653/v1/D19-1658
2. Fabbri, A. R., Kryściński, W., McCann, B., Xiong, C., Socher, R., & Radev, D. (2021). Summeval: Re-evaluating summarization evaluation. arXiv. https://doi.org/10.48550/arXiv.2007.12626
3. Grootendorst, M. P. (n.d.). Home. Retrieved April 6, 2023, from https://maartengr.github.io/BERTopic/index.html
4. Hubbard, K. E., & Dunbar, S. D. (2017). Perceptions of scientific research literature and strategies for reading papers depend on academic career stage. PLoS ONE, 12(12), e0189753.
https://doi.org/10.1371/journal.pone.0189753
5. Mallick, T., Bergerson, J. D., Verner, D. R., Hutchison, J. K., Levy, L.-A., & Balaprakash, P. (2023). Analyzing the impact of climate change on critical infrastructure from the scientific literature: A weakly supervised NLP approach. arXiv. https://doi.org/10.48550/arXiv.2302.01887



