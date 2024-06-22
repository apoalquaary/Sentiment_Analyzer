# Sentiment_Analyzer
 
Sentiment Analyzer is a powerful tool designed for users who need to perform sentiment analysis on customer data or social media content. It provides an easy-to-use interface for analyzing sentiments using state-of-the-art AI models for Arabic, English, and multilingual texts.

Scope
This project integrates three robust sentiment analysis models:

Arabic Model: Utilizes a specialized model trained for Arabic text sentiment analysis.
English Model: Uses a model optimized for sentiment analysis in English text.
Multilingual Model: Capable of analyzing sentiment in multiple languages, offering flexibility for diverse text sources.
These models are renowned for their accuracy and have been integrated into the project to simplify sentiment analysis tasks without requiring users to delve into complex AI implementations.

Installation
To get started with Sentiment Analyzer, follow these steps:

Clone the repository:

bash
Copy code
git clone https://github.com/yourusername/sentiment-analyzer.git
cd sentiment-analyzer
Install dependencies:

bash
Copy code
pip install -r requirements.txt
Configuration
Configure the config.yaml file to tailor the program to your needs:

File Details: Specify the path to your data file (excel_file_path or csv_file_path) and the name of the column containing text to analyze (text_column_name).

Example:

yaml
file:
  path: docs/microblogging.xlsx
  columnName: Text

  
Data Cleaning: Enable data cleaning (clean_data: 1) if your data requires preprocessing for social media text. Disable it (clean_data: 0) for other types of data.

Model Selection: Uncomment one of the models (arabic_model, english_model, multilingual_model) to specify which sentiment analysis model to use. The selected model will be automatically downloaded to the models/ folder.

Example:

yaml
  # Uncomment one of the following models:
  # analyzing_model: CAMeL-Lab/bert-base-arabic-camelbert-da-sentiment 
  # analyzing_model: cardiffnlp/twitter-roberta-base-sentiment 
  # analyzing_model: cardiffnlp/twitter-xlm-roberta-base-sentiment 

Usage
Using File Input
Run the main script:

bash
Copy code
python sentiment_analyzer.py
This will read the specified data file (excel_file_path or csv_file_path) and analyze sentiments based on the chosen model.

Using Direct Input
Prepare a list of texts:
Create a Python script (test.py) and provide a list of texts as input to the Sentiment Analyzer.

python
Copy code
from sentiment_analyzer import SentimentAnalyzer

texts = [
    "Text 1 to analyze.",
    "Another text for sentiment analysis.",
    "And a third example text."
]

analyzer = SentimentAnalyzer()
results = analyzer.analyze_texts(texts)

print(results)
Replace sentiment_analyzer with the appropriate module or class name in your project structure.

Contributing
Contributions to Sentiment Analyzer are welcome!.

License
This project is licensed under the MIT License.

