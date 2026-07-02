# Trade Narratives in the UN General Debate Corpus

This project analyzes how trade is discussed in United Nations General Debate speeches from 1946 to 2024. It uses the United Nations General Debate Corpus (UNGDC) and applies text preprocessing, keyword-based filtering, sentiment analysis, TF-IDF, co-occurrence analysis, topic modelling, and event-focused keyword tracking. The notebook focuses especially on trade-related language, including concepts connected to liberalization, protectionism, markets, sanctions, supply chains, and global economic cooperation.

## Project Summary

The project starts by loading UN General Debate speeches and converting filenames into country, session, and year metadata. It cleans and tokenizes the texts, removes stopwords and speaker names, stems words, and creates speech-level token lists for analysis. It then explores corpus-level word frequencies, text lengths, trade-related term frequencies, and co-occurrences around trade-related target words. The main analysis identifies trade-related sentences, tracks the share of trade language over time, estimates sentiment in trade-related sentences, and compares liberalization-oriented and protection-oriented keyword patterns. The notebook also uses TF-IDF and LDA topic modelling to summarize recurring trade themes, then checks selected historical event narratives such as WTO-related language, financial crisis language, COVID/supply-chain language, and trade-war/sovereignty language. The results are presented as exploratory text-mining evidence rather than causal claims.

## Repository Structure

```text
.
├── tm-project.ipynb          # Main analysis notebook
├── README.md                 # Project description and usage notes
├── .gitignore                # Files excluded from version control
└── dataverse/                # Local UNGDC data directory, not recommended for GitHub
```

## Data

The analysis uses the United Nations General Debate Corpus (UNGDC), a publicly available corpus of speeches delivered during the annual United Nations General Debate. The dataset is available through Harvard Dataverse:

Jankin, Slava; Baturo, Alexander; Dasandi, Niheer, 2017, "United Nations General Debate Corpus 1946-2025", https://doi.org/10.7910/DVN/0TJX8Y, Harvard Dataverse, V14

The notebook expects the data to be stored locally in the following structure:

```text
dataverse/dataverse/UN General Debate Corpus/TXT/
dataverse/dataverse/Speakers_by_session.xlsx
```

## Methods

The notebook uses:

- text cleaning, tokenization, stopword removal, and stemming with NLTK;
- descriptive corpus statistics and frequency counts;
- trade-related keyword filtering and sentence extraction;
- co-occurrence and PMI analysis around trade-related terms;
- VADER sentiment analysis for trade-related sentences;
- TF-IDF indicators for trade vocabulary;
- keyword-ratio comparisons for liberalization and protectionism frames;
- LDA topic modelling for trade-related vocabulary;
- event-focused keyword tracking over time.

## How to Run

1. Clone the repository.
2. Download or place the UNGDC data in the expected local `dataverse/` structure.
3. Install the required Python packages:

```bash
pip install pandas numpy matplotlib nltk wordcloud scikit-learn statsmodels openpyxl
```

4. Open `tm-project.ipynb` in Jupyter Notebook or JupyterLab.
5. Run the notebook from top to bottom. If NLTK resources are missing, download `punkt`, `stopwords`, `wordnet`, `punkt_tab`, and `vader_lexicon` before running the analysis.


## License

The code in this repository is released under the MIT License.

The underlying UN General Debate Corpus data are not included in this repository and remain subject to the terms and citation requirements of the original data source.
