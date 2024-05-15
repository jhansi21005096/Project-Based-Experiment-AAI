<H3>ENTER YOUR NAME:K.Jhansi</H3>
<H3>ENTER YOUR REGISTER NO:212221230045</H3>
<H3>DATE:</H3>
<H1 Align="center">Project Based Experiment<H1>
<H3>Objective:<H3>
Type your objective based on the question
<H3>Program:</H3>
  
```
pip install pandas textblob
import pandas as pd
from textblob import TextBlob

# Load the CSV file into a DataFrame
df = pd.read_csv('fb_sentiment.csv')

# Function to perform sentiment analysis using TextBlob
def analyze_sentiment(text):
    blob = TextBlob(str(text))
    return blob.sentiment.polarity

# Apply sentiment analysis to each row in the DataFrame
df['Sentiment'] = df['FBPost'].apply(analyze_sentiment)

# Output the DataFrame with sentiment analysis results
print(df.head())

# Filter out rows with negative sentiment (label 'N')
negative_feedback = df[df['Label'] == 'N']

# Output the negative feedback
print(negative_feedback)


```

  
<H3>Output:</H3>
![output](https://github.com/jhansi21005096/Project-Based-Experiment-AAI/blob/main/output%20p.png)
<H3>Inference:</H3>
Thus sentiment analysis using your Facebook data ias done and filtering the data that n only negative feedback for the code is done.
