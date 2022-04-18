Download dataset from https://www.kaggle.com/datasets/kazanova/sentiment140

Packages Used in SahilPatel_DataPreprocess:
- Pandas
- Nltk

Packages Used in SahilPatel_Models:
- Sklearn
- Numpy
- Pandas
- Seaborn
- Matplotlib

Packages Used in SahilPatel_Flask:
- Flask
- Flask_cors

Save and unzip it in "datasets" folder or change the file_input_path in second cell of SahilPatel_DataPreprocess.ipynb to where dataset is saved

SahilPatel_DataPreprocess: 
- reads original dataset, preprocesses it, and saves it locally as 'processed_data.csv'

SahilPatel_Models:
- reads processed_data.csv into dataframe
- converts dataset to vector using TfidfVectorizer
- splits data into training and test set
- trainings and tests LogisticRegression, LinearSVC, and BernoulliNB
- saves a pickle file for all models and the vectorizer

SahilPatel_Flask:
- reads the pickle file and hosts the model locally on http://127.0.0.1:5000/
- takes input in form of "http://127.0.0.1:5000/sentiment?model={MODEL_OPTION}&text{YOUR_TEXT}" 
  - MODEL_OPTION is "lr", "nb", or "svm" and YOUR_TEXT can be any text/sentence
  - To run locally: http://127.0.0.1:5000/sentiment?model=lr&text=i%20like%20pizza
  
You can also try: http://spatel475.pythonanywhere.com/sentiment?model=lr&text=i%20like%20pizza

https://sahilpatel-dev.web.app/sentiment communicates with http://spatel475.pythonanywhere.com/sentiment
