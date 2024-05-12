**Music Recommendation System Report**

**Introduction**

The objective of this project was to develop a music recommendation system based on audio features extracted from audio files. The system utilizes machine learning techniques to recommend tracks similar to a given track ID. This report outlines the methodology employed, the implementation details, and the findings of the recommendation system.

**Methodology**

1. **Data Collection and Preprocessing**:
    - The Free Music Archive (FMA) dataset was used for this project. It consists of audio files along with metadata in CSV format.
    - Data preprocessing involved loading the CSV files into Pandas DataFrames, handling missing values, and normalizing numerical features. Text preprocessing was performed on categorical columns.

2. **Feature Extraction**:
    - Features such as Mel-frequency cepstral coefficients (MFCC) and spectral centroid were extracted from audio files using the Librosa library. These features capture important aspects of the audio signal related to timbre and spectral characteristics.

3. **Storing Data in MongoDB**:
    - Extracted audio features and metadata were stored in a MongoDB database for efficient retrieval and scalability.

4. **Building Approximate Nearest Neighbors (ANN) Index**:
    - An ANN index was constructed using the Annoy library. This index allows for fast similarity search based on the extracted audio features.

5. **Recommendation System**:
    - The recommendation system recommends tracks similar to a given track ID by querying the ANN index. It returns a list of recommended tracks based on their similarity to the input track.

6. **Evaluation**:
    - The effectiveness of the recommendation system was evaluated using Mean Average Precision (MAP) and Normalized Discounted Cumulative Gain (NDCG) metrics. Ground truth data consisting of user preferences was used for evaluation.

**Implementation**

- The project was implemented in Python using various libraries such as Pandas, NumPy, Librosa, Scikit-learn, PyMongo, and Annoy.
- The recommendation system was encapsulated in a Python script (`audio_recommendation.py`) which can be executed from the command line.
- Data preprocessing, feature extraction, and model evaluation were performed within the script.

**Findings**

- The recommendation system demonstrated promising results in recommending tracks similar to a given track ID.
- Evaluation metrics such as Mean Average Precision (MAP) and Normalized Discounted Cumulative Gain (NDCG) indicated the effectiveness of the recommendation system.
- The system's performance can be further improved with fine-tuning of parameters and incorporating user feedback.

**Conclusion**

In conclusion, the developed music recommendation system based on audio features proved to be effective in recommending tracks similar to a given input track. By leveraging machine learning techniques and efficient data storage and retrieval mechanisms, the system provides a valuable tool for music discovery and personalized recommendations.

