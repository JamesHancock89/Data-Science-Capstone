Word Prediction Presentation
========================================================
author: James Hancock
date: 22/03/2017
autosize: true
Coursera Data Science Specialization Capstone Project April 2017

Creating A Predictive Text Algorithm 
========================================================

The word prediction algorithm  [View the Word Prediction Shiny App here] (https://james-hancock.shinyapps.io/Word_Prediction_App/) was created through the below key tasks:

- The word prediction model was an advancement on the milestone report analysis completed as part of learning natural language processing with data science specialization.
- A large corpus of more than 4 million documents was loaded and analyzed which included data from blogs, news and twitter. 
- N-grams were extracted from the corpus and used to build the word prediction model.
- Several Methods to improve accuracy and improvement of the models performance were explored before settling on the final model (see next slide for details).


Designing And Improving The Algorithm
========================================================

The methods for designing the word prediction model are explained below:

- N-gram model with back-off strategy was used.
- Dataset was cleaned, then lower-cased, then all links were removed, twitter handles, punctuations, numbers and extra whitespaces were all removed.
- Matrices from hexa-gram (6gram) to uni-gram were extracted.
- N-grams were sorted by frequency of their occurrence.
- The size of model was reduced to improve performance by dropping the least frequent N-grams.
- Finally, I further optimized speed and memory by dropping the least frequent bigrams and unigrams. As the very large matrices observed within the bigrams and unigrams do not appear to improve accuracy of the overall word prediction model.

Word Prediction Algorithm Shiny App Instructions
========================================================

The word prediction algorithms functionality and instructions for use are explained below:

- App provides a text input box for user to type a phrase.
- Detects words typed and predicts the next word reactively.
- Iterates from longest N-gram (hexagram) to shortest (bigram).
- Uses last word in matching N-gram as predicted word.
- Predicts using the longest, most frequent, matching N-gram.
- If no match is found using hexa, penta,quad,tri, and bigrams, the app randomly selects most frequent word (unigram).
- Allows users to configure how many words the app should suggest, through using the slider option.
- Showcases the last word being typed, so users can make sure they haven't input an incorrect word or phrase etc...


Application Performance
========================================================
- Final model size from the corpus:
    - ~83k hexagrams.
    - ~184k grams.
    - ~475k quadgrams.
    - ~440k trigrams. 
    - ~200k bigrams 
    - ~20k wordsunigrams.
- Average response time is usually less than 2 seconds.
- Application memory usage under 250MB.
- [You can view the Word Prediction Shiny App here](https://james-hancock.shinyapps.io/Word_Prediction_App/)
