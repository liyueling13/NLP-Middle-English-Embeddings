# NLP-Middle-English-Embeddings

In the summer of 2022, I was a PhD Fellow at Duke's Center for Computational Thinking working with co-directors Matt Hirschey and Akshay Bareja. I worked on a few different projects on Middle English NLP in R and Python:

## EDA in R and Python with the 14th century poems Pearl and Patience
Pearl is a much-celebrated 14th-century medieval poem written in West Midlands Middle English, and Patience is a lesser-known poem by the same author. 

1. I scraped and got the text of Pearl (1212 lines) in a tibble organized by line number, stanza number, and section number. Using tidytext, tidyr, and dplyr, I explored line, sentence, and stanza length. I created simple visualizations in ggplot.

2. I used BeautifulSoup to scrape the prose text of Patience and performed text preprocessing: removed stopwords, numbers, and punctuation, and standardized similar words using stemming and lemmatization. Then I created n-grams (bigrams and trigrams).

![278739292-55e183fd-927b-4cb5-8f76-cce89475ac47](https://github.com/liyueling13/NLP-Middle-English-Embeddings/assets/81717153/36c80e0e-b668-49b9-a7ca-431d05bc035c)

My goal was to ultimately build a model to predict whether the anonymous poem St. Erkenwald was authored by the same poet who authored Pearl, Patience, Sir Gawain and the Green Knight,  and Cleanness. However, I ultimately decided that due to the high variance between the poems (completely different themes, settings, and style of poetry) this wasn't a good computational project.

## Middle English gensim word2vec embedding

When working on Pearl and Patience, I researched pretrained Middle English tokenizers, but couldn't find anything. The Classical Language Toolkit offers embeddings for a variety of ancient languages including Latin, Greek, Old Norse, Classical Chinese, and more, but did not have anything for Middle English (I later [contributed to this project!]([url](https://docs.cltk.org/en/latest/cltk.embeddings.html#cltk.embeddings.processes.MiddleEnglishEmbeddingsProcess)https://docs.cltk.org/en/latest/cltk.embeddings.html#cltk.embeddings.processes.MiddleEnglishEmbeddingsProcess)).

I decided to build my own Middle English embedding. I found a sizeable Middle English corpus, scraped from the University of Michigan's Corpus of Middle English Prose and Verse and assembled by Nathan Stringham at the University of Utah. With assitance from Akshay Bareja and Danai Adkisson (Duke), I built my own gensim word2vec embedding. It returns Mikolov's arithmetic: king-man+woman = queen. 

![image](https://github.com/liyueling13/NLP-Middle-English-Embeddings/assets/81717153/0d068640-6073-4d48-a322-8e8424e4da9d)
![image](https://github.com/liyueling13/NLP-Middle-English-Embeddings/assets/81717153/61cc7398-fcbf-4c49-a3a1-768185b41b14)

The drawings are from [this blog.]([url](https://blog.acolyer.org/2016/04/21/the-amazing-power-of-word-vectors/))

Here's the arithmetic on my word2vec model:

![image](https://github.com/liyueling13/NLP-Middle-English-Embeddings/assets/81717153/ad169868-e00f-41a1-97d1-0aeb03c5153e)
