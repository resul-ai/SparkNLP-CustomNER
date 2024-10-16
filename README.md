# SparkNLP-CustomNER Project

This project demonstrates the implementation of a Spark NLP Healthcare Pipeline and the training of a Custom Named Entity Recognition (NER) model. The objective is to leverage pre-trained models for entity extraction, generate a custom dataset, and use it to train a specialized NER model. The project is structured in three interconnected parts, each building upon the previous to achieve a comprehensive NER solution.

We begin by implementing a pipeline using Spark NLP's pre-trained `ner_clinical` and `ner_posology` models on a public healthcare dataset. The extracted entities are then converted into CoNLL format, creating a custom dataset tailored to our specific needs. Finally, this custom dataset is used to train and evaluate a new NER model, demonstrating the full cycle from data preparation to model deployment.

## Part I: Pipeline Implementation

In this part, we set up the Spark NLP for Healthcare environment and implemented a Named Entity Recognition (NER) pipeline using pre-trained models.

Key achievements:
- Set up Spark NLP for Healthcare with the necessary dependencies.
- Utilized the `ner_clinical` and `ner_posology` models from Spark NLP Healthcare.
- Created a Spark NLP pipeline that includes tokenization, sentence splitting, and NER using both models.
- Processed the mt_samples dataset, a publicly available healthcare-related dataset.
- Extracted and reviewed entity predictions from the pipeline for both clinical and medication-related entities.

## Part II: CoNLL File Generation

This part focused on converting the NER predictions from Spark NLP models into the CoNLL format, which is essential for training custom NER models.

Key achievements:
- Developed a robust function to convert NER predictions into the standard CoNLL format.
- Ensured each token is correctly labeled with its corresponding entity tag.
- Generated CoNLL files that are compliant with the standard format used for NER model training.
- Implemented error handling and validation to ensure data integrity during the conversion process.

## Part III: Custom NER Model Training

The final part involved using the generated CoNLL file to train and evaluate a custom NER model using Spark NLP.

Key achievements:
- Utilized the generated CoNLL file to train a custom NER model with Spark NLP.
- Implemented a training pipeline that includes embedding selection, graph creation, and model configuration.
- Evaluated the performance of the custom NER model using metrics such as precision, recall, and F1-score.
- Implemented visualization of training progress and model performance.
- Demonstrated the use of the trained model for making predictions on new data.

## Bonus Features

- Implemented visualization of NER predictions using the Spark NLP Display library.
- Provided detailed training logs and performance metrics throughout the training process.
- Included example predictions and visualizations to showcase the model's capabilities.

## Running the Project

To run this project:

1. Ensure you have the necessary Spark NLP Healthcare license and dependencies installed.
2. Execute the notebooks in order: 
   - `1_Pipeline_Implementation.ipynb`
   - `2_CoNLL_File_Generation.ipynb`
   - `3_Custom_NER_Model_Training.ipynb`
3. Follow the instructions within each notebook for detailed steps and explanations.

This project demonstrates a comprehensive approach to NER in the healthcare domain, from using pre-trained models to creating a custom solution tailored to specific needs.

*R. Caliskan - Data Scientist*