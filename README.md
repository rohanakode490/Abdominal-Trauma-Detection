# Abdominal Trauma Detection

This repository contains the Jupyter notebook used to develop a machine learning model for detecting abdominal trauma in medical scans. The project was part of a competition focused on identifying injuries through multiple data modalities, including statistical data, CAT scans, and 3D eco images.

[Visit the Kaggle competition page here.](https://www.kaggle.com/competitions/rsna-2023-abdominal-trauma-detection/data)

**Note:** The dataset used for this project was over 460GB and was provided by the competition organizers. Due to the large size of the dataset, all model training and evaluation were conducted on the competition platform itself. Only the code is available in this repository.


## Project Overview

We were tasked with analyzing medical scans of patients suspected of having abdominal trauma. Our approach involved creating a machine learning model using the **EfficientNet-B4** architecture, which was specifically tailored for the dataset’s unique characteristics. This ensemble model processed three different sources of information:

1. **Statistical Data** – Patient metadata and other numerical features.
2. **CAT Scans** – 2D medical images that required extensive preprocessing.
3. **Eco 3D Images** – 3D representations that added complexity to the detection process.

### Key Features

- **Localized Detection**: We designed separate models for each source of information (statistical data, CAT scans, and 3D images) and integrated them into an ensemble model for accurate trauma detection.
- **Data Augmentation**: One of the biggest challenges was the inconsistency and low quality of the medical scans, which made it difficult for the model to accurately detect injuries. To mitigate this, we employed extensive data augmentation techniques. By introducing various negative samples in different hues, we were able to train the model to extract more meaningful information from localized organ regions.
- **Model Efficiency**: After extensive optimization, our ensemble model achieved an impressive **87.4% accuracy**. This was particularly noteworthy given the challenges posed by the dataset's quality.

### Results and Achievements

- The project not only provided valuable insights into the application of AI in medical diagnosis but also earned a reward for the innovative use of machine learning in processing complex medical data.
- The competition judges praised our approach to handling noisy data and the overall model design, which balanced accuracy and efficiency.

## Files in This Repository

- **notebooks/**: Contains the Jupyter notebook used to build, train, and evaluate the EfficientNet-B4-based model.
- **models/**: Placeholder for model weights (not provided due to platform restrictions).
- **submission/**: Code to generate predictions and create submission files.

## How to Use

Although the dataset is not included in this repository, you can follow the code to understand how the model was constructed and trained. If you have access to a similar dataset or are participating in a related competition, you can adapt the provided notebook to your specific use case.

1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/abdominal-trauma-detection.git

   cd abdominal-trauma-detection
2. Install the necessary Python dependencies:
    ```bash
    pip install -r requirements.txt
3. Run the Jupyter notebook:
    ```bash
    jupyter notebook notebooks/abdominal_trauma_detection.ipynb

