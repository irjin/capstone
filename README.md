# DSC 180A Project (Section B09)

In a rapidly evolving information landscape, widespread misinformation and disinformation present a significant challenge as the general public navigates through online media sources. To address this problem, this project aims to use transcribed textual features to categorize misleading information on a varying scale. The dataset used in this project was scrapped from PolitiFact and was cleaned to include the title, article, and summary. Nine machine learning classifiers were used, resulting in a final accuracy of 0.5369.  

Keywords: misinformation, disinformation, machine learning

## Getting Started
1. Clone the repository.

2. Download the required libraries.
```bash
pip install pandas
pip install numpy
pip install scikit-learn
pip install nltk
pip install imblearn
```
3. Run the notebook from top to bottom. 

## Features

1. ClickBait (Title, Article): To assess whether the article would be a ClickBait, the TF-IDF was calculated for the title and article column using scikit-learn’s TfidfVectorizer. Then, the cosine similarity between them was calculated to assess whether the content of the article truly matches its corresponding title. 
2. Sentiment Analysis (Article): Using NLTK, an overall rating was given to the article based where a number closer to 1 meaning mostly positive, -1 meaning mostly negative, and 0 meaning mostly neutral. 
3. Quality of Writing (Article): As many fake news show signs of poor quality of writing, one feature was dedicated to calculating this by assessing the diversity of vocabulary in the articles based on the Type-Token Ratio (TTR). The formula is given by the number of unique words divided by the total number of words. All stopwords and punctuation were removed before this calculation. 
4. Expressiveness (Article): Adjectives can be a way to show expressiveness. One of the features in this dataset was calculated by the number of adjectives divided by the total number of words. 

## Labels

0-5, corresponding to Pants-Fire, False, Barely-True, Half-True, Mostly-True, and True
