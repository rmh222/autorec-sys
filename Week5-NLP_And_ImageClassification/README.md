# Week 5 README file

## Code Description: 
The code used for finding keywords from article text using NLP methods to classify images extracted previously from the Euronews website can be found in the Week5-NLP jupyter notebook file. In this file I used the csv file containing the images extracted from the business tagged articles in the euronews website in week3. For each image I extracted the text surrounding the image in the article. I then cleaned the text removing punctuation and stopwords and lemmatizing it. Using a TF-IDF vectorizer I extracted the most significant words in the text then used POS tagging to extract only the Nouns. 
I then added the extracted keywords to a copy of the csv file used. 

In the week5-ImageClassification jupyter notebook I used a library called Clip to label the images. The labelling options i used were the keywords previously extracted. 
I observed that the accuracy of the labels is often very good and the labels are meaningful. 

The next step is to explore using Deep Learning (CNN and LSTM) to extract features and labels from the image rather than the text in the article. 

