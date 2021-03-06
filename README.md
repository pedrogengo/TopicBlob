
TopicBlob: Simplified Topic Modeling
====================================


`TopicBlob` is a Python 3 library for processing textual data. It provides a simple API for diving into common natural language processing (NLP) taks around topic modeling such as finding similar documents and provide a list of topics givne input text.


```
    from topicblob import TopicBlob
  
    text1 = "The titular threat of The Blob has always struck me as the ultimate moviemonster: an insatiably hungry, amoeba-like mass able to penetrate virtually any safeguard, capable of as a doomed doctor chillingly describes it assimilating flesh on contact. Snide comparisons to gelatin be damned, it's a concept with the most devastating of potential consequences, not unlike the grey goo scenario proposed by technological theorists fearful of artificial intelligence run rampant."

    text2 = "Myeloid derived suppressor cells (MDSC) are immature myeloid cells with immunosuppressive activity. They accumulate in tumor-bearing mice and humans with different types of cancer, including hepatocellular carcinoma (HCC)."
    
    
    docs = [text1, text2]
    
    
    tb = TopicBlob(docs, 5, 5)
    tb.topics # {"['able', 'grey', 'capable', 'gelatin', 'titular']": 0, "['cells', 'myeloid', 'immunosuppressive', 'suppressor', 'hepatocellular']": 1}
    
    tb.sims # {0: 1.0, 1: 0.0} TODO: get better examples
  ```  

TopicBlob leverages  `NLTK` and `gensim` , for the heavy lifting

Features
--------

- Topic Extraction
- Similarity Search
- BM25 search ( word ranking search)
- Topic Search

Get it now
----------
    #TODO push to pip
    $ git clone https://github.com/banjtheman/TopicBlob/
    $ pip install --editable . 

Requirements
------------

- Python  >= 3.5


