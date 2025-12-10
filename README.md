# LLM_FINE_TUNNING_ROJECT
Disease Prediction using LLM Fine-Tuning (QLoRA + TinyLlama)
This project demonstrates how to fine-tune an open-source Large Language Model (LLM) to identify likely disease patterns from natural-language symptom descriptions. Using TinyLlama-1.1B-Chat and QLoRA, the model is trained on the Disease and Symptoms dataset from Kaggle.
The goal is to create an educational model capable of:
Reading symptoms written in plain English
Predicting the closest matching disease from the dataset
Providing a short explanation
Displaying a mandatory medical safety disclaimer
This project is strictly educational and must NOT be used for real medical diagnosis.

Dataset Used
Source:
Kaggle Dataset: 
https://www.kaggle.com/datasets/choongqianzheng/disease-and-symptoms
dataset?select=DiseaseAndSymptoms.csv

Model & Training Details
Model Used
TinyLlama-1.1B-Chat (HuggingFace)
fine-tuned using QLoRA (4-bit low-rank adaptation)
Model Used are:-
The model selected for this project is TinyLlama-1.1B-Chat, a lightweight and instruction-tuned LLM that performs well on educational tasks while being highly resource-efficient.
It was fine-tuned using:
QLoRA (4-bit quantization + LoRA adapters)
PEFT (Parameter-Efficient Fine-Tuning)
bfloat16 mixed precision

Training Outcome
The training completed successfully on Colab GPU using 4-bit quantization.
The model showed a steady decrease in loss values across training steps.
LoRA adapter weights were saved, allowing efficient deployment without storing the full fine-tuned model.
After training, the model produced consistent structured responses containing:
Possible condition
Explanation
Note

Demo Case Testing
The fine-tuned model was tested with three real-world symptom sets:
Fever, headache, body pain
Cough, sore throat, runny nose
Abdominal pain, vomiting, diarrhea
For each case, the model correctly identified the closest disease pattern from the training dataset and provided a clear explanation along with a safety disclaimer.

conclusion:The fine-tuned TinyLlama model successfully learned to:
Understand natural-language symptom descriptions
Predict likely disease patterns from the dataset
Provide short, readable explanations


This approach significantly reduces memory usage and allows training on small GPUs without sacrificing model performance.
