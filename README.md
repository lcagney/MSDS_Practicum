# MSDS_Practicum_1
![dr who logo](https://github.com/lcagney/MSDS_Practicum/blob/9f9040d216187e4c9274f969115aaeee885b6311/Images/DoctorWhoLogo_WC.png)
## Introduction
This project analyzes Doctor Who fanfiction scraped from ArchiveOfOurOwn and seeks to create a topic model derived from the most popular published stories in the fandom. This project was completed over the 8 week capstone term using Python and scikit-learn's LatentDirichletAllocation model.

## Methods Used
The data was scraped from AO3 and cleaned until only lemmatized nounds remained. The topics were created by tuning the max_df, min_df, n_components inputs and perplexity score outputs. The final model was created using 30 topics, with a min_df of 25, max_df of 70%. 

## Top 10 Topics
| Topic #        | Theme         |
| ------------- | ------------- |
| 18  | General Regeneration  |
| 0 | 13th Doctor Regeneration  |
| 14 | TenToo AU |
| 7 | Rose as Bad Wolf |
| 1 | River Song's Husband |
| 21 | Falling in Love |
| 13 | Heaven and Hell Collide | 
| 16 | The Family Pond | 
| 20 | Time Lords |
| 12 | Friends of the Doctor | 

## Stories in each Topic
![storydist](https://github.com/lcagney/MSDS_Practicum/blob/c4e58fb9e231a434c3748ac2bbc88ce14d6a2de5/Images/storycountsbytopic.jpg)

No stories had the dominant topic for Topics 3, 8, 9, 10, 15, 25.

## Files Included
The following files are included as part of my submission:
- Jupyter Notbook: This file contains all code used to clean, explore, and model the data.
- CSV Files:
  - fic_lem_nounonly_tokens_2021-05-28.csv: Cleaned, lemmatized, noun only data.
  - topics_2021-06-05.csv: The 30 topics and associated words.
- PowerPoint Presentation: Final presentation with insights and process

## References
Chen, Yanlin. (2018). How to generate an LDA topic model for text analysis. Retrieved from https://medium.com/@yanlinc/how-to-build-a-lda-topic-model-using-from-text-601cdcbfd3a6

Ganesan, K. (n.d.). 10+ examples for using CountVectorizer. Retrieved from https://kavita-ganesan.com/how-to-use-countvectorizer/#.YMJZGJNKgl4.

James. (n.d). Topic modeling in python. Retrieved from https://ourcodingclub.github.io/tutorials/topic-modelling-python/#apply. 

Li, Jingyi. (2016). AO3 scraper. Retrieved from https://github.com/radiolarian/AO3Scraper 

scikit-learn. (n.d.). Topic extraction with Non-negative Matrix Factorization and Latent Dirichlet Allocation. Retrieved from https://scikit-learn.org/stable/auto_examples/applications/plot_topics_extraction_with_nmf_lda.html. 

sophros.https://stackoverflow.com/questions/65817456/lda-topic-model-gensim-gives-same-set-of-topics
    
Marcel. (2017). python scikit learn, get documents per topic in LDA. Retrieved from https://stackoverflow.com/questions/45145368/python-scikit-learn-get-documents-per-topic-in-lda
    
