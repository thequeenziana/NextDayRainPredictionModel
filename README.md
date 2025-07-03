# NextDayRainPredictionModel
An artificial intelligence/ machine learning prediction model <br>
This project aims to predict whether it will rain the next day using historical weather data from Australia (2013-2017). It formulates the problem as a binary classification task (RainTomorrow: Yes/No) and compares multiple machine learning models to find the best balance between prediction accuracy and computational efficiency. <br>

### Models Used
- Support Vector Machine (SVM)
- Decision Tree
- Random Forest
- K-Nearest Neighbors (KNN)
- Long Short-Term Memory (LSTM) neural network

### Dataset
Australian Weather Dataset (2007-2017), focusing on data from 2013-2017. <br>
Features include temperature, humidity, wind speed, cloud cover, sunshine, and rainfall. <br>
Target variable: RainTomorrow (binary). <br>

### Preprocessing Steps
- Data sorting by date to maintain time order.

- Missing value imputation:<br>
Time interpolation for time-sensitive features (e.g., sunshine, cloud cover).<br>
Mode imputation for categorical features (RainToday, RainTomorrow).<br>
Median imputation for numeric features (rainfall).<br>
Random Forest-based imputation for improved categorical value filling.<br>
- Label encoding of categorical variables.
- Feature scaling for models sensitive to scale (KNN, LSTM).
- Handling class imbalance using SMOTE oversampling for minority class (RainTomorrow = Yes).

### Analysis
Random Forest gave the best balanced performance with ~82% accuracy.<br>
Decision Tree overfit and performed worse on recall and precision.<br>
KNN had high recall but low precision due to sensitivity to feature scaling.<br>
SVM balanced recall and F1-score well.<br>
LSTM captured temporal patterns but was slower and more resource-intensive.<br>
