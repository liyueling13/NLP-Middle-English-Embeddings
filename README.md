# NLP-Middle-English-Embeddings

In the summer of 2022, I was a PhD Fellow at Duke's Center for Computational Thinking working with co-directors Matt Hirschey and Akshay Bareja. I worked on a few different projects on Middle English NLP in R and Python:

## EDA in R and Python with the 14th century poems Pearl and Patience
Pearl is a much-celebrated 14th-century medieval poem written in West Midlands Middle English, and Patience is a lesser-known poem by the same author. 

1. I scraped and got the text of Pearl (1212 lines) in a tibble organized by line number, stanza number, and section number. Using tidytext, tidyr, and dplyr, I explored line, sentence, and stanza length. I created simple visualizations in ggplot.

2. I used BeautifulSoup to scrape the prose text of Patience and performed text preprocessing: removed stopwords, numbers, and punctuation, and standardized similar words using stemming and lemmatization. Then I created n-grams (bigrams and trigrams).

![278739292-55e183fd-927b-4cb5-8f76-cce89475ac47](https://github.com/liyueling13/NLP-Middle-English-Embeddings/assets/81717153/36c80e0e-b668-49b9-a7ca-431d05bc035c)

My goal was to ultimately build a model to predict whether the anonymous poem St. Erkenwald was authored by the same poet who authored Pearl, Patience, Sir Gawain and the Green Knight,  and Cleanness. However, I ultimately decided that due to the high variance between the poems (completely different themes, settings, and style of poetry) this wasn't a good computational project.

## 2. I built a gensim word2vec embedding trained on a large Middle English corpus that returns Mikolav's arithmetic.

