# **Parameter-Efficient Sentiment Classification in E-Governance Using LoRA and Domain-Grounded Synthetic Data**

## **Overview**
Automated sentiment analysis of policy consultation comments is challenging due to technical language and data scarcity. We propose a framework that:
•	**Synthesizes Data**: Uses Google Gemini 1.5 Flash grounded in MCA policy documents to generate 16,602 labeled comments.
•	**Efficient Fine-Tuning**: Adapts DistilBERT using Low-Rank Adaptation (LoRA), reducing trainable parameters by ~10,000$\times$.
•	**Optimization**: Employs Optuna for Bayesian hyperparameter search to achieve a weighted F1-score of 0.71.

## **Dataset**
The dataset was generated using a domain-grounding strategy to ensure regulatory relevance.
•	**Neutral**: 6,383 (38.22%)
•	**Positive**: 6,142 (36.77%)
•	**Negative**: 4,177 (25.01%)

## **Model Training**
To replicate the training using our optimized hyperparameters from Trial 9:
•	Learning Rate: $6.32 \times 10^{-5}$
•	Batch Size: 32
•	Optimizer: AdamW

## **Results**
The model achieves a weighted F1-score of 0.71. It is particularly robust at identifying Negative sentiment (0.78 F1), which is critical for identifying compliance friction and stakeholder concerns in policy consultations.

