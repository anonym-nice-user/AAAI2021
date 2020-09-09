In this dataset, we crowdsource 1000 amazon reviews and the task was to identify whether a  review was written on a book or other product.
To train classifiers, we used only "_golden"==False reviews as these reviews were used as test questions in crowdsourcing jobs.

If you use this data please cite this paper.

- 2 Classes: isBook {0, 1}
- Train size: 1000
- Val size: 1000
- Test size:4000
- Train size crowdsourced: 1000
- Num of workers: 263
- Total num. answers: 4907
- Num. answers per worker (± stddev.): 18.6 ± 4.6
- Num. answers per instance (± stddev.): 4.9 ± 0.41
- Mean annotators accuracy (± stddev.): 0.946 ± 0.076
- Maj. vot. accuracy: MV acciracy: 0.964,
- DS accuracy: 0.961,
- GLAD accuracy: 0.964,
- LFC accuracy: 0.961 

Where MV- Majority voting, DS - Dawid and Skene, LFC - learning from crowd (without data features).


#### Data cleaning
We performed different data preprocessing techniques:
-   "raw" - original textual data
-   "clean"- textual data were preprocessed with the following steps:

        - make lowercase
        - remove punctuation marks
        - replace english contractions by full words
        - substitute numbers
        - remove english stopwords
        - words lemmatization
        - words stemming
        - strip html
        - removing accented characters
        - substitute URLs
        - substitute usernames
- "tobert" - textual data were preprocessed to feed Transformer models (e.g., BERT):

        - ASCII letters are removed
        - URLs, @[NAME], HTML tags are substituted by tokens



BERT tokenizer:
-   90th percentile: 357.0 tokens
- 95th percentile: 524.09 tokens