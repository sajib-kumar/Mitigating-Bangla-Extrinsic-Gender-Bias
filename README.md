<div align="center">


# ⚖️ Mitigating Extrinsic Gender Bias for Bangla Classification Tasks

<div align="justify">
  
  In this study, we investigate extrinsic gender bias in Bangla pretrained language models, a largely underexplored area in low-resource languages. To assess this bias, we construct four manually annotated, task-specific benchmark datasets for sentiment analysis, toxicity detection, hate speech detection, and sarcasm detection. Each dataset is augmented using nuanced gender perturbations, where we systematically swap gendered names and terms while preserving semantic content, enabling minimal-pair evaluation of gender-driven prediction shifts. We then propose **RandSymKL**, a randomized debiasing strategy integrated with symmetric KL divergence and cross-entropy loss to mitigate the bias across task-specific pretrained models. **RandSymKL** is a refined training approach to integrate these elements in a unified way for extrinsic gender bias mitigation focused on classification tasks. Our approach was evaluated against existing bias mitigation methods, with results showing that our technique not only effectively reduces bias but also maintains competitive accuracy compared to other baseline approaches.
</div>

📄 **[Read the Preprint on arXiv](https://arxiv.org/pdf/2411.10636)**



</div>

---

## ✨ Key Contributions

- 🗂️ **4 benchmark datasets** for Bangla gender bias evaluation (sentiment, toxicity, hate speech, sarcasm)
- 📖 **573-pair Bangla gendered lexicon** built from grammar books and web sources
- 🧠 **RandSymKL** — a stochastic debiasing strategy outperforms all baselines across fairness metrics while maintaining strong accuracy

---

## 🗃️ Repository Structure

The repository is organized into three main directories:

- **`Approach/`** — Contains the code and results of all 8 approaches applied to detect and mitigate extrinsic gender bias. In each approach subdirectory, there are two files for each task (sentiment analysis, sarcasm detection, hate speech detection, and toxicity detection) — one containing the implementation and one containing the obtained results.
- **`Data/`** — Contains the datasets for all four tasks, along with a CSV file of the gender paired lexicon.
- **`Gender Name Alteration/`** — Contains the code for generating gender-name swapped text from the original text.

---

## 🧠 RandSymKL

<p align="justify">
RandSymKL feeds male- and female-centric text pairs simultaneously into a Pretrained Language Model (PLM) followed by maxpool, dropout, and a task-specific linear layer, producing logits <code>z₁</code> and <code>z₂</code>. At each training step, one is randomly selected for cross-entropy loss, while a symmetric KL divergence term penalizes distributional divergence between gendered predictions.
</p>
  
![Methodology](https://raw.githubusercontent.com/sajib-kumar/Mitigating-Bangla-Extrinsic-Gender-Bias/main/RandSymKL.png)

---

## 📜 Citation

```bibtex
@article{joy2024mitigating,
  title   = {Mitigating Extrinsic Gender Bias for Bangla Classification Tasks},
  author  = {Joy, Sajib Kumar Saha and Mahy, Arman Hassan and Sultana, Meherin
             and Abha, Azizah Mamun and Ahmmed, MD Piyal and Dong, Yue and Shahariar, G M},
  journal = {arXiv preprint arXiv:2411.10636},
  year    = {2024},
  url     = {https://arxiv.org/pdf/2411.10636}
}
```

---

