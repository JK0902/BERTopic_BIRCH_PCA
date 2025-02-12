# BERTopic_BIRCH_PCA

**What the project does**

The study title is Empowering Patient-Centered Research through Artificial Intelligence: A Novel Approach to Identifying Research Priorities in Cancer Care

Our research question:
Can Artificial Intelligence (AI) and Natural Language Processing (NLP) generate quality research ideas that prioritize patient concerns by analyzing a large database of patient portal messages?

Findings:
By analyzing 614,464 messages from patients with breast or skin cancer, AI-generated research topics were evaluated by six highly experienced clinicians for significance and novelty. One-third were highly significant and novel, and two-thirds were novel.


**Why the project is useful**
The findings of our study demonstrate that AI/NLP-driven analysis of large volumes of patient messages can generate quality research topics in cancer care that reflect patient perspectives, providing valuable guidance for future patient-centered health research endeavors.

We believe and hope that the concept of this study can be reproduced and applied to other patient-generated data for further experiments through these shared resources, contributing to the field.

**How users can get started with the project**
To better understand the context of our study, please read this article.
In this GitHub, we provided all the codes that we used for topic modeling. Three approaches included BERTopic, BERTopic with BIRCH (for obtaining more refined topics), BERTopic with BIRCH and PCA (for obtaining more refined topics yet with efficiency). 

Below is the language from the article.

“2-Staged topic modeling 
To identify patients’ clinical concerns, we analyzed the secure messages, constructing a 2-staged unsupervised NLP topic model leveraging Bidirectional Encoder Representations from Transformers (BERT) and Balanced Iterative Reducing and Clustering using Hierarchies (BIRCH) techniques to extract the essential topics. First, preprocessed messages were converted into sentences using pre-calculated embedding (all-miniLM-L6-v2). To simplify the dimensionality, we applied Uniform Mapping and Approximation and Projection and ConvectVectorizer to remove infrequent words. Finally, we employed a zero-shot clustering to categorize similar topics by cosine similarity score. 

To further refine the clustered topics, we constructed a new BERTopic model, applying the BIRCH algorithm, which can effectively and efficiently manage large data. We implemented Principal Component Analysis (PCA) and incremental fitting techniques for additional data process efficiency. For skin cancer messages, we were able to analyze them without PCA and incremental fitting because the data size was manageable (n=140,270). However, for breast cancer messages, we had to apply PCA and incremental fitting to efficiently handle the larger data size (n=474,194). To find the optimal number of components for reduced embeddings for PCA and the appropriate batch size for incremental fitting, we conducted a few experiments. After trying multiple combinations of options (e.g. n_components=180~220, batch size=500~2000), we decided to use n_components =200 and batch size=1000 because the number of components explaining 90% variance was 196.”


**This project is maintained by the first and the corresponding author of this article (Jiyeong Kim, PhD, MPH).


![image](https://github.com/user-attachments/assets/c64c75f5-1e2d-4c61-b3b2-3dda285e31fb)
