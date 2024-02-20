# Predicting-Emotion-of-Spotify-Songs
### AIM: Predicting Whether the Song is Sad Song or Happy Song.

### Dataset: Kaggle Spotify Label Dataset

#### Dataset Columns and its Info

Labels: {'sad': 0, 'happy': 1, 'energetic': 2, 'calm': 3}# we wll select only 2 i.e sad & happy

Acousticness: A confidence measure from 0.0 to 1.0 of whether the track is acoustic. 1.0 represents high confidence the track is acoustic.

Danceability: Danceability describes how suitable a track is for dancing based on a combination of musical elements including tempo, rhythm stability, beat strength, and overall regularity. A value of 0.0 is least danceable and 1.0 is most danceable.

Energy: Energy is a measure from 0.0 to 1.0 and represents a perceptual measure of intensity and activity.

Instrumentalness: Predicts whether a track contains no vocals. “Ooh” and “aah” sounds are treated as instrumental in this context. Rap or spoken word tracks are clearly “vocal”. The closer the instrumentalness value is to 1.0, the greater likelihood the track contains no vocal content. Values above 0.5 are intended to represent instrumental tracks, but confidence is higher as the value approaches 1.0.

Liveness: Detects the presence of an audience in the recording. Higher liveness values represent an increased probability that the track was performed live. A value above 0.8 provides a strong likelihood that the track is live.

Loudness: the overall loudness of a track in decibels (dB).Loudness is the quality of a sound that is the primary psychological correlate of physical strength (amplitude). Values typically range between -60 and 0 db.

Speechiness: Speechiness detects the presence of spoken words in a track. (e.g. talk show, audiobook, poetry).Values above 0.66 describe tracks that are probably made entirely of spoken words. Values between 0.33 and 0.66 describe tracks that may contain both music and speech, either in sections or layered, including such cases as rap music. Values below 0.33 most likely represent music and other non-speech-like tracks.

Valence: A measure from 0.0 to 1.0 describing the musical positiveness conveyed by a track. Tracks with high valence sound more positive (e.g. happy, cheerful, euphoric), while tracks with low valence sound more negative (e.g. sad, depressed, angry).

Tempo: The overall estimated tempo of a track in beats per minute (BPM). In musical terminology, the tempo is the speed or pace of a given piece and derives directly from the average beat duration.


### Importing Libraries and Dataset
Data Manipulation:
Pandas
numpy 
Visualization library:
matplotlib.pyplot
seaborn

### Basic EDA (Exploratory Data Analysis)
Checking Shape- There are 277938 rows and 12 columns 
Missing values- There are no missing values in this dataset
checking Info & describe of dataset

Checking Correlation- Then we check correlation by Heatmap using .corr() function, Highest correlated column with the target column is Instrumentalness with 0.54
Droping unwanted columns

### Binary Classification 
we are selecting only two labels i.e Sad & Happy, After selecting these two labels we have a data shape of near about 18000 rows with 11 columns.
Then we put our input features in X variable and target column in y variable.

### Splitting of Data
We split the data into 7:3 ratio , (test size of 30%) with random state : 42

### Scaling Values
We have applied Standard Scaler on Data.
Satandard Scaler:
StandardScaler is used in machine learning and data preprocessing to standardize features by removing the mean and scaling them to unit variance. This process is important because it helps in bringing all features to a similar scale, which prevents certain features from dominating the learning process simply because they have larger scales than others.
Standardizing the features ensures that they have a mean of 0 and a standard deviation of 1, making it easier for algorithms to learn.

### Applying Logistic Regression

Logistic regression is a classification algorithm used to predict the probability of a binary outcome based on one or more predictor variables. It models the relationship between the dependent variable and independent variables by estimating the probabilities using a logistic function.
After applying model we check predictions on X test scsaled data and then we plot classification report and confusion metrics

### Accuracy
Our model got 88.44% accuracy on train data & 88.32% on test data 

### Improving Model by GridSearch CV

GridSearchCV is a technique used for hyperparameter tuning in machine learning, where a grid of hyperparameters is systematically searched using cross-validation to find the optimal combination that maximizes the model's performance on a given dataset. It exhaustively tries all possible hyperparameter combinations to identify the best set of values for the model.
After applying Gridsearch cv with proper parameters we get best parameters 

### Final Accuracy & Classification Report
we got 88.32% Accuracy













