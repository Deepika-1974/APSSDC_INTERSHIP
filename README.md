# Reviews Text Preprocessing and Analysis

This project focuses on text preprocessing and analysis of customer reviews. Various techniques such as tokenization, stopword removal, stemming, lemmatization, and normalization are applied to clean the data and prepare it for further analysis.

## Project Overview

- **Dataset**: CSV file containing customer reviews (`Reviews.csv`).
- **Tasks**:
  1. Data loading and inspection.
  2. Data cleaning (handling missing values and duplicates).
  3. Word Cloud visualization for most frequent words in the reviews.
  4. Frequency analysis of specific target words.
  5. Text preprocessing (tokenization, stemming, lemmatization, removing stopwords).
  6. Data normalization (expanding contractions, removing emojis, and HTML tags).

## 1. Dataset

The dataset contains customer reviews with the following columns:
- **Review**: The textual review from customers.

## 2. Key Libraries

The following Python libraries are used for this project:
- **Pandas**: For data manipulation and analysis.
- **Matplotlib** & **Seaborn**: For data visualization.
- **WordCloud**: To generate a word cloud of review text.
- **NLTK**: For text preprocessing (tokenization, stemming, lemmatization, stopword removal).
- **BeautifulSoup**: For HTML tag removal.
- **Contractions**: For expanding contractions.
- **Emoji**: For handling emojis in text.

## 3. Data Preprocessing Steps

### Data Inspection
- **Data loading**: The dataset is loaded using `pandas.read_csv`.
- **Data exploration**: The structure and summary of the dataset are checked using `.info()`, `.head()`, `.tail()`, etc.
- **Missing values and duplicates**: Checked using `.isnull().sum()` and `.duplicated()`.

### Text Cleaning and Visualization
- **Word Cloud**: A word cloud is generated from the reviews to visualize the most frequent words.
- **Frequency Analysis**: Specific words such as 'good', 'great', 'amazing', 'bad', 'not bad' are analyzed to check their frequency in the reviews.

### Text Preprocessing
1. **Lowercasing**: Convert all reviews to lowercase for uniformity.
2. **Tokenization**: Split reviews into individual words using NLTK's `word_tokenize`.
3. **Stopword Removal**: Remove common English stopwords like 'the', 'is', etc., using NLTK's stopwords list.
4. **Stemming**: Use the PorterStemmer to reduce words to their base or root form.
5. **Lemmatization**: Apply WordNetLemmatizer to convert words to their base forms, considering context (POS tagging).
6. **Removing Numbers**: Numbers are removed from the text using regular expressions.
7. **Cleaning Special Characters**: Remove special characters using regular expressions.
8. **Expanding Contractions**: Using the `contractions` library to expand words like "don't" to "do not".
9. **Handling Emojis**: Convert emojis to their text representation using the `emoji` library.
10. **Removing HTML Tags**: Use `BeautifulSoup` to strip HTML tags from reviews.

## 4. Visualizations and Results

- **Word Cloud**: A visual representation of the most common words in the review text.
- **Frequency Bar Plot**: Displays the frequency of targeted words (e.g., 'good', 'great', etc.).
- **Processed Reviews**: Display the results of text preprocessing including tokenized, stemmed, lemmatized, and cleaned reviews.

## 5. How to Run

### Prerequisites

Ensure you have the following Python packages installed:
```bash
pip install pandas matplotlib seaborn wordcloud nltk beautifulsoup4 contractions emoji
