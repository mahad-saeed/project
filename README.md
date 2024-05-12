# project

**Project Overview**

This project involves processing audio files to extract features and metadata, preprocessing and storing the data, building an approximate nearest neighbors (ANN) index for recommendation, and evaluating the recommendation model.

**Libraries Used**
- **Pandas**: For data manipulation and analysis.
- **NumPy**: For numerical computing.
- **Mutagen**: For reading audio metadata.
- **Librosa**: For audio analysis.
- **Scikit-learn**: For data preprocessing and evaluation metrics.
- **MongoDB and PyMongo**: For storing and retrieving data.
- **Annoy**: For building the approximate nearest neighbors index.

**Code Description**

1. **Data Loading and Preprocessing**: 
    - The code loads data from CSV files into Pandas DataFrames.
    - It preprocesses the data by filling missing values and normalizing numerical features.
    - Text preprocessing is performed on categorical columns.
  
2. **Feature Extraction**: 
    - Features like MFCC (Mel-frequency cepstral coefficients) and spectral centroid are extracted from audio files using Librosa.
  
3. **Storing Data in MongoDB**: 
    - Extracted audio features and metadata are stored in MongoDB for efficient retrieval.
  
4. **Building ANN Index**: 
    - An approximate nearest neighbors index is built using Annoy, combining MFCC and spectral centroid features.
  
5. **Recommendation System**: 
    - The system recommends tracks similar to a given track ID based on the ANN index.
  
6. **Model Evaluation**: 
    - The model is evaluated using Mean Average Precision (MAP) and Normalized Discounted Cumulative Gain (NDCG) metrics.

**How to Use**

1. Ensure all required libraries are installed (`pip install pandas numpy mutagen librosa scikit-learn pymongo annoy`).
2. Run the provided Python script.
3. Adjust paths and configurations as needed for your environment.
4. Modify ground truth data and evaluation metrics according to your requirements.

