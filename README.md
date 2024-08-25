# Project report collection

This repository is the collection of every completed report corresponding to the projects from the public and private repository of Hirbod-JORFlint.
In this README, a summary of every uploaded project is gradually added for future insights.

## An approach for Language Model probing 
The approach for applying the probing task originated from paper 
<a href="https://aclanthology.org/2022.coling-1.413/">(Where Does Linguistic Information Emerge ...)</a>. 
The probing tasks involve Part-of-Speech tagging and Syntactic Ancestors Prediction along with 6 different metrics to investigate the difference between the language models
trained in English and Persian languages respectively. Similar to the original paper, differences in information distribution among these models were observed. Although
These findings do not necessarily suggest language-specific characteristics, it can be concluded that there might be a need to tailor these models to specific languages for
language-specific tasks.
Questions to be investigated:
1. How do language-specific factors influence the interpretability of neural language models across various languages?
2. Do different pre-training objectives affect the information distribution across layers in language models?
3. Is the model's size an impactful factor when investigating the information distribution across layers?

Aside from the improved capacity of larger models for more complex patterns and better generalization, investigating overlapping functionalities in smaller layers might provide
a useful insight into the overall information emergence in Large language models.

## Bias identification using language models
This work as a use machine learning approach to detect and measure bias in news articles using a fine-tuned RoBERTa model inspired by the work <a href="https://aclanthology.org/2021.findings-emnlp.101/">(Neural Media Bias Detection Using Distant Supervision With BABE.)</a>.
In this project to evaluate the effectiveness and performance of the bias detection model, three baselines along with the metrics of Accuracy\Precision\Recall\F1 score were utilized.
After observing the good performance of the model across the metrics, and gaining deeper insights into the model's decision-making process for the purpose of identifying key parts of the input that significantly
influence the output and project the data into a lower-dimensional space to understand the possible relationship between the sentences identified by the model.
As a result, the model shows promise in bias identification and its classification according to achieving a higher f1-score against baselines.
Questions to be investigated:
1. "Anchors" help explain why the model made a particular classification, for example, the model was successful in correctly predicting certain combinations of words "halt, efforts, declared, ..." as non-biased, these combinations
might be observed in biased text input as well. Can we define metrics to specifically target the generalization capability of the model in such cases?

The embeddings capture the semantic information from sentences, and when projected into lower dimensions, data points that are closer together represent sentences that are more semantically similar.
However, while the dimensions from the t-SNE plot show relationships within clusters, the dominant words in those sentences do not directly indicate a clear bias, and four out of five clusters have mixed amounts of bias and
non-biased input text suggests that the embedding structure is capturing bias in a way that isn't easily explained just by looking at the top words alone:  
&emsp;2. What are the specific relationships between the two t-SNE dimensions and the bias patterns within the dataset were observed? Do they represent any particular semantic properties?  
&emsp;3. Why might the top words in a cluster not show a dominant relationship to bias? Does this suggest a limitation in using word frequency as an indicator of bias, or are there other factors at play?
