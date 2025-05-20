# Mitigating-Extrinsic-Gender-Bias-in-Bangla-Text-Classification-via-Nuanced-Gender-Perturbations
In this study, we investigate extrinsic gender bias in Bangla pretrained language models, a largely underexplored area in low-resource languages. To assess this bias, we construct four manually annotated, task-specific benchmark datasets for sentiment analysis, toxicity detection, hate speech detection, and sarcasm detection. Each dataset is augmented using nuanced gender perturbations, where we systematically swap gendered names and terms while preserving semantic content, enabling minimal-pair evaluation of gender-driven prediction shifts. We then propose RandSymKL, a randomized debiasing strategy integrated with symmetric KL divergence and cross-entropy loss to mitigate the bias across task-specific pretrained models. To our knowledge, this approach is the first to integrate these elements in a unified strategy for extrinsic gender bias mitigation focused on the classification task. Our approach was evaluated against existing bias mitigation methods, with results showing that our technique not only effectively reduces bias but also maintains competitive accuracy compared to other baseline approaches.

# Repository Structure
The repository has two folders.

**Approach** contains the code and results of all 8 approaches we applied to detect and mitigate extrinsic gender bias. In each approach subdirectory, there are two files for each task (sentiment analysis, sarcasm detection, hatespeech detection, and toxicity detection). One contains the implementation, and one contains the obtained results.
<br>
**Data** directory contains the datasets for all the tasks, along with a csv file that contains the gendered terms.
<br>
**Gender Name Alteration** contains the codes for generating gender-name swapped text from the original text.
