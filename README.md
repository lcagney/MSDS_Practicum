# MSDS_Practicum_1
![dr who logo](https://github.com/lcagney/MSDS_Practicum/blob/9f9040d216187e4c9274f969115aaeee885b6311/Images/DoctorWhoLogo_WC.png)

Doctor Who Logo Word Cloud
## Introduction
This project analyzes Doctor Who fanfiction scraped from ArchiveOfOurOwn and seeks to create a topic model derived from the most popular published stories in the fandom. This project was completed over the 8 week capstone term using Python and scikit-learn's LatentDirichletAllocation model.

## Files Included
The following files are included as part of my submission:
- Jupyter Notbook: This file contains all code used to clean, explore, and model the data. Available as a ipynb or PDF format.
- CSV Files:
  - TopicThemes.xlsx: The final themes determined by the 30 topics generated from the model.
  - topics_2021-06-05.csv: The 30 topics and associated words.
- Final_Presentation.pdf: Final presentation with insights and process. The file must be downloaded for the links to work.

**Not Included** : Data was too large to upload here

## Methods Used
The data was scraped from AO3 and cleaned until only lemmatized nouns remained. The topics were created by tuning the max_df, min_df, n_components inputs and perplexity score output. The final model was created using 30 topics, with a min_df of 25, max_df of 70%. Additional information on tuning and the dataset is available in the [presentation deck](https://github.com/lcagney/MSDS_Practicum/blob/fc4f5865bdd294740ae267f661865b280631213f/Final_Presentation.pdf) and [presentation video](https://youtu.be/7F5ooAb74xI).


## Top 10 Topics
I named these topics after looking at the top words associated with each topic and validating that the words in teach topic accurately reflected what the stories were about. The topics-to-theme list is located in the CSV_Files folder.

| Topic #        | Theme         | Story Count | 
| ------------- | ------------- | ------------- |
| 18  | General Regeneration    | 366
| 0 | 13th Doctor Regeneration  | 176
| 14 | TenToo AU                | 144
| 7 | Rose as Bad Wolf          | 137
| 1 | River Song's Husband      | 113
| 21 | Falling in Love          | 77
| 13 | Heaven and Hell Collide  | 71
| 16 | The Family Pond          | 51
| 20 | Time Lords               | 43
| 12 | Friends of the Doctor    | 43

If you are not a fan of Doctor Who (specifically, Doctor Who post 2005), these topic themes will not make sense; however, someone who is a fan of the show and looking for something to read or write about, this can provide some helpful context on what fans are enjoying!

## Stories in each Topic
![storydist](https://github.com/lcagney/MSDS_Practicum/blob/c4e58fb9e231a434c3748ac2bbc88ce14d6a2de5/Images/storycountsbytopic.jpg)

No stories had the dominant topic for Topics 3, 8, 9, 10, 15, 25. Each story received a score for every topic created and the highest score is where the story ultimately got assigned to. This presents an opportunity viewing the topics as a hierarchy. Topic 18 ended up being a general catch-all topic, representing 26% of all stories.

## Next Steps
- There are opportunities for subtopic modeling to understand how closely each story resembled other topics. 
- Understanding the smaller topics. They seem to be crossovers with other fandoms and the presence of fandom specific words biased the creation of those topics.
- More comprehensive cleaning: merging bigrams or trigrams
- Testing other topic model paradigms
- Build a better dataset: full stories, no crossovers etc.
  -  I initially went with chapter ones because I could pull in a greater amount of variety than a smaller dataset with full stories of varying lengths.

## Conclusion
- Difficult to create interpretable topics
- Required **extensive** domain knowledge on the chosen fandom
  -  This means this is not easily scalable to other fandoms as I initally hoped.
-  It was fun to create names of themes!

## References
Chen, Yanlin. (2018). How to generate an LDA topic model for text analysis. Retrieved from https://medium.com/@yanlinc/how-to-build-a-lda-topic-model-using-from-text-601cdcbfd3a6

Ganesan, K. (n.d.). 10+ examples for using CountVectorizer. Retrieved from https://kavita-ganesan.com/how-to-use-countvectorizer/#.YMJZGJNKgl4.

James. (n.d). Topic modeling in python. Retrieved from https://ourcodingclub.github.io/tutorials/topic-modelling-python/#apply. 

Li, Jingyi. (2016). AO3 scraper. Retrieved from https://github.com/radiolarian/AO3Scraper 

scikit-learn. (n.d.). Topic extraction with Non-negative Matrix Factorization and Latent Dirichlet Allocation. Retrieved from https://scikit-learn.org/stable/auto_examples/applications/plot_topics_extraction_with_nmf_lda.html. 

sophros.https://stackoverflow.com/questions/65817456/lda-topic-model-gensim-gives-same-set-of-topics
    
Marcel. (2017). python scikit learn, get documents per topic in LDA. Retrieved from https://stackoverflow.com/questions/45145368/python-scikit-learn-get-documents-per-topic-in-lda
    
