# Sentiment Analysis Practice

A Python-based sentiment analysis project that analyzes Amazon product reviews using Natural Language Processing (NLP) techniques. This project demonstrates how to use NLTK and VADER sentiment analyzer to classify and visualize sentiment in customer reviews.

## Overview

This project performs sentiment analysis on Amazon product reviews, correlating sentiment scores with star ratings. It uses VADER (Valence Aware Dictionary and sEntiment Reasoner) sentiment analyzer to compute positive, negative, neutral, and compound sentiment scores for each review.

## Features

- **Data Loading**: Reads Amazon product reviews from CSV file
- **Exploratory Data Analysis (EDA)**: Visualizes review distribution by star ratings
- **NLP Processing**: 
  - Tokenization using NLTK
  - Part-of-Speech (POS) tagging
  - Named Entity Recognition (NER) chunking
- **Sentiment Analysis**: 
  - VADER sentiment scoring (positive, negative, neutral, compound)
  - Correlation analysis between sentiment scores and star ratings
- **Visualizations**: 
  - Bar plots showing sentiment scores by review ratings
  - Comparative analysis of positive, neutral, and negative sentiment scores

## Requirements

### Python Packages
- `pandas` - Data manipulation and analysis
- `numpy` - Numerical computing
- `matplotlib` - Plotting and visualization
- `seaborn` - Statistical data visualization
- `nltk` - Natural Language Toolkit
- `tqdm` - Progress bars for loops

### NLTK Data
The following NLTK data packages are required:
- `punkt` - Tokenizer models
- `averaged_perceptron_tagger` - POS tagger
- `vader_lexicon` - VADER sentiment analyzer lexicon
- `maxent_ne_chunker` - Named entity chunker
- `words` - Word list

## Installation

1. Clone or download this repository

2. Install required Python packages:
```bash
pip install pandas numpy matplotlib seaborn nltk tqdm
```

3. Download required NLTK data:
```python
import nltk
nltk.download('punkt')
nltk.download('averaged_perceptron_tagger')
nltk.download('vader_lexicon')
nltk.download('maxent_ne_chunker')
nltk.download('words')
```

## Usage

1. **Prepare your data**: 
   - Place your `Reviews.csv` file in the appropriate directory
   - Update the file path in the notebook if needed

2. **Run the notebook**:
   - Open `Sentiment-Analysis.ipynb` in Jupyter Notebook or JupyterLab
   - Execute cells sequentially

3. **Key Steps**:
   - **Step 0**: Import libraries and read data
   - **Step 1**: Perform VADER sentiment scoring on all reviews
   - Visualize sentiment scores by star ratings

## Project Structure

```
Sentiment-Analysis/
├── README.md                    # Project documentation
├── Sentiment-Analysis.ipynb     # Main analysis notebook
└── archive/                      # Data directory (not included)
    └── Reviews.csv              # Amazon product reviews dataset
```

## Methodology

1. **Data Loading**: Loads Amazon reviews dataset and samples 500 reviews for analysis
2. **EDA**: Analyzes distribution of reviews by star ratings (1-5 stars)
3. **NLP Preprocessing**: 
   - Tokenizes text into words
   - Tags words with part-of-speech labels
   - Identifies named entities (e.g., organizations, products)
4. **Sentiment Analysis**: 
   - Uses VADER sentiment analyzer to compute sentiment scores
   - VADER provides four scores:
     - `pos`: Positive sentiment (0-1)
     - `neu`: Neutral sentiment (0-1)
     - `neg`: Negative sentiment (0-1)
     - `compound`: Normalized compound score (-1 to 1)
5. **Visualization**: Creates bar plots showing how sentiment scores correlate with star ratings

## Results

The analysis demonstrates that:
- Higher star ratings (4-5 stars) correlate with higher positive sentiment scores
- Lower star ratings (1-2 stars) correlate with higher negative sentiment scores
- The compound score provides a single metric that correlates well with star ratings

## Technologies Used

- **Python 3.x**
- **Jupyter Notebook**
- **NLTK** - Natural Language Processing
- **VADER Sentiment Analyzer** - Rule-based sentiment analysis tool
- **Pandas** - Data manipulation
- **Matplotlib & Seaborn** - Data visualization

## Notes

- The project uses a sample of 500 reviews for demonstration purposes
- VADER is particularly good at handling social media text and informal language
- The sentiment scores are normalized and range from -1 (most negative) to +1 (most positive)

## License

This is a practice project for educational purposes.