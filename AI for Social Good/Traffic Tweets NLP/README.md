# Traffic Manila Tweet Analysis

## Project Overview
This project performs **semantic analysis** on public tweets related to **traffic in Manila**. Using **Natural Language Processing (NLP)** techniques, the project analyzes sentiment, identifies key themes, and uncovers public opinion trends about the traffic situation in Manila. The focus is on extracting meaningful insights by preprocessing the data, applying tokenization, sentiment analysis, and topic modeling.

---

## Data
- **Source**: Public tweets containing the keyword "traffic Manila."
- **Columns**:
  - `Date`: The date and time the tweet was posted.
  - `Tweet`: The tweet content.
  - `likeCount`: Number of likes received.
- **Dataset Size**: Contains thousands of tweets ranging from **01/01/2022 to 12/22/2022**.

---

## Methodology
1. **Language Detection**:
   - Used the `langdetect` library to filter out non-English tweets, ensuring analysis was performed only on relevant data.

2. **Data Preprocessing**: 
   - Cleaned the text by removing URLs, punctuation, special characters, and lowercasing all text.
   - Stopwords were removed, except for sentiment-related words like "not."
   - **Lemmatization** was applied to reduce words to their base form.

3. **Vectorization**: 
   - Tweets were converted to numerical features using **TF-IDF Vectorization** to represent text data for modeling.

4. **Sentiment Analysis**:
   - **VADER Sentiment**: Applied VADER (Valence Aware Dictionary for Sentiment Reasoning) for initial sentiment polarity classification (positive, neutral, negative).
   - **Logistic Regression**: Additionally, built a sentiment classifier using **Logistic Regression** for more refined sentiment prediction, trained using the vectorized tweets.


---

## Results
- **Sentiment Distribution**: Tweets were classified into three categories:
  - **Positive**: Tweets reflecting optimism about traffic.
  - **Negative**: Tweets expressing frustration or complaints.
  - **Neutral**: Informative tweets without strong sentiment.
  
- **Key Themes**: 
  - Traffic congestion hotspots.
  - Complaints about road conditions and delays.
  - Positive remarks on road improvements.

---

## Recommendations
- Authorities can leverage these insights to understand public sentiment and improve traffic management.
- Hotspots of traffic congestion identified from the data can guide infrastructure improvements.

---

## Model
- **Sentiment Analysis Model**: Pre-trained supervised model used for sentiment classification.

---

## Installation
 Clone the repository

 pip install -r requirements.txt
 
## Usage
import joblib
from vaderSentiment.vaderSentiment import SentimentIntensityAnalyzer

model = joblib.load('sentiment_model.joblib')
vectorizer = joblib.load('vectorizer.joblib')
analyzer = SentimentIntensityAnalyzer()
streamlit run app.py

## License
This update includes all the methodologies and tools you used (like `langdetect`, `vectorizer`, `Logistic Regression`, and `VADER Sentiment`). Let me know if you'd like any further adjustments!



  
