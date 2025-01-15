# NER Project: Named Entity Recognition for Mountain Names

## **Project Overview**

This project performs Named Entity Recognition (NER) for detecting mountain names in text. The model is trained on a custom dataset of mountain names, including synthetic data to improve performance.

## **Project Structure**

- **`NER_Project/`** — contains all files related to this project.
  - **`Dataset_creation_explanation.ipynb`** — notebook explaining the process of dataset creation.
  - **`Mountain Test Project.ipynb`** — main notebook for training and testing the NER model.
  - **`final_dataset.csv`** — final labeled dataset used for training the model.
  - **`model files.txt`** — folder containing Google Drive link to the trained model files.
  - **`CSV files`** — additional datasets used during the project including:
    - **Mountain.csv** -  Kaggle Mountain Dataset
    - **annotated_mountain_dataset.csv** - formed dataset with Wikipedia sentences.
    - **synthetic_data.csv** - data from GPT generation.
    - ** combined_annotated_dataset.csv** - combined Wiki and GPT data.
  - **`requirements.txt`** - all libraries used in the project
  - **`Python scripts.txt`** — contains links to Google Drive Python scripts, including:
    - **Python script (.py) for model training.**
    - **Python script (.py) for model inference.**
  - **NER_Potential Improvements.pdf** - file with my thoughts on potential improvements.

## **Setup Instructions**

1. **Clone the repository**:
   ```bash
   git clone https://github.com/Markol06/TestProject-NER-CV.git
   cd TestProject-NER-CV/NER_Project
2.Install required dependencies: Make sure Python 3.8+ is installed, then run:
pip install -r requirements.txt
3.Run the Jupyter notebook: 
Open Mountain Test Project.ipynb in Jupyter and execute all cells to train the model or use it for inference.
Or use python scripts.
4.Results: The trained model will be saved in the saved_model/ folder and can be used for further predictions.

Solution Explanation
Dataset Creation:

The dataset was created by manually collecting mountain names and labels.
Additional synthetic data was generated to improve model robustness. Details of the dataset creation process can be found in the Dataset_creation_explanation.ipynb notebook.
Model Training:

The model is based on BERT fine-tuned for the NER task.
Key hyperparameters used for training:
epochs = 8
batch_size = 16
learning_rate = 3e-5
Model Evaluation:

The trained model achieved the following results:
F1-Score for class B-MOUNTAIN: 0.73
F1-Score for class I-MOUNTAIN: 0.74
