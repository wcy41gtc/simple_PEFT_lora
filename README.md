
# This notebook demonstrates using parameter efficient fine tuning (PEFT) technique on foundation models
* PEFT technique: Low Rank Adaptation
* Model: distilbert-base-uncased
* Evaluation approach: accuracy
* Fine-tuning dataset: sms_spam
## PEFT Technique Selection & Initial Setup:
* Chose specific parameter-efficient fine-tuning (PEFT) settings for adapting a foundation model using the Hugging Face peft library, targeting minimal computational resource use.
## Model and Dataset Preparation:
* Loaded a pre-trained DistilBert model and an SMS spam dataset. Prepared data for fine-tuning by tokenizing texts and splitting into training and test sets.
## Baseline Model Evaluation:
* Evaluated the original pre-trained model’s performance to establish a benchmark before fine-tuning.
## Fine-Tuning Process:
1. Applied fine-tuning to the DistilBert model using the training subset of the dataset.
2. Adjusted model parameters minimally to optimize for the spam detection task, using training arguments like learning rate and batch size settings.
3. Implemented and tracked training progress and metrics such as loss and accuracy.
## PEFT Model Setup:
1. Configured and instantiated a PEFT model using LoRA (Low-Rank Adaptation) adjustments specific to certain model components (like query, key, and value layers in transformers).
2. Trained the PEFT model on the spam detection task, aiming to improve upon the baseline performance.
## Inference and Evaluation:
1. Conducted inference with the fine-tuned model to assess performance enhancements.
2. Compared the performance of the PEFT-enhanced model against the original model, demonstrating significant improvements in accuracy.
## Results:
* Showcased effective fine-tuning with the PEFT model, achieving higher accuracy in spam detection compared to the pre-tuned model, thereby validating the efficiency and effectiveness of the chosen fine-tuning technique.