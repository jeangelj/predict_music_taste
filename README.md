# predict_music_taste
Predict music taste based on a subset of the one million song set. 
General Assembly Data Science Program 2016 
Julia Engel-Dagher

##intro 
The Million Song Dataset is a freely-available collection of audio features and metadata for a million contemporary popular music tracks.
Most of the information is provided by The Echo Nest. The dataset is the result of a collaboration between The Echo Nest and LabROSA at Columbia University, supported in part by the NSF. (last update November 2015)


The data set consists of several subsets of various types of data:
- Million Song Dataset (280 GB) 
- SecondHandSongs dataset -> cover songs
- musiXmatch dataset -> lyrics
- Last.fm dataset -> song-level tags and similarity
- Taste Profile subset -> user data (3GB)
- thisismyjam-to-MSD mapping -> more user data
- tagtraum genre annotations -> genre labels
- Top MAGD dataset -> more genre labels
- There are even more additional data sets which can be bundled with the original data set. http://labrosa.ee.columbia.edu/millionsong/pages/getting-dataset
- For example, for some artists the longitude and langitude are known. http://labrosa.ee.columbia.edu/millionsong/sites/default/files/AdditionalFiles/artist_location.txt

#####Links:
http://labrosa.ee.columbia.edu/millionsong/pages/getting-dataset#subset
https://aws.amazon.com/datasets/million-song-dataset/

#####Source: 
Thierry Bertin-Mahieux, Daniel P.W. Ellis, Brian Whitman, and Paul Lamere. 
The Million Song Dataset. In Proceedings of the 12th International Society
for Music Information Retrieval Conference (ISMIR 2011), 2011.

##Hypothesis

"Pandora was perhaps the frontrunner of combining the two when it started the 'Music Genome Project' way back in 1999 before terms like Big Data even existed. The project considers songs as datasets and analyzes each song using up to 450 distinct musical characteristics or “genes”. A person – a trained music analyst with an actual degree in music – and automated algorithms comb through the song and classify it as Pop/Rock, Hip-Hop/Electronica, Jazz, World Music, and Classical. Decoding the “genes” of the song helps Pandora find the similarities and then successfully predict what a user might like listening to next."
http://www.byteacademy.co/blog/item/121-the-music-industry-is-growing-more-reliant-on-data-science

With Spotify's recent pruchase of Seed Scientific, the usage of data science for improving music curation is undeniable. Data science gives the power of curation and predition - two aspects of data which are continusously increasing in importance due to larger and larger datasets. 

The goal of this project is to predict the popularity of a song and curate the next song a user might like, not only based on musical attributes of the song, but also based on sentiment analysis of the lyrics. 

##Project Proposal
https://prezi.com/dldm6ttndwxh/one-million/

##Process
Please go to the wiki to see more details about the process. 
https://github.com/jeangelj/predict_music_taste/wiki

##Conclusion
1. In Machine Learning, 50% of success is the data set. The quantity of data was definitely the biggest hurdle. 
2. Due to the quantity of data and possible features, music should be considered big data and analyzed as such (Hadoop/Spark)
3. I couldn't surpass the accuracy rate of 37% for predicting song popularity (Supervised learning)  
  i. For supervised learning machine learning methods the feature selection is essential  
  ii. I was missing the mood of the song (based on lyrics) - I believe this would hav eimproved my model substantially  
  iii. I also established early on that artist_familiarity and artist_hotness had the biggest impact and I kept on using these   features; this could have been restritive to my models and the whole approach (the idea is to find songs the user doesn't know, but will like)  
4. Unsupervised learning methods were perfect for song recommendation. Unfortunately, the jupyter notebook kernel would die, if I included too many freatues, so I used only 4. But I was still able to recommend songs to a user.

##Final Presentation
http://slides.com/jdagher/predicting-music-preferences#/

##Business / Practical applications
While Pandora has more than 450 features and Spotify has unlimited user behavior data, they 
a. still need a music professional for recommendations
b. do not manage to predict music taste
It seems that the features these companies are using are not capturing the essence of taste. 
This project was an attempt to combine different types of features and predict music taste. 
While just a small attempt, it definitely stresses the point that we are looking at music one dimensionally. 
Given the necessary resources, the idea would be to analyze music from a different point of view and establish a model that can actually recommend songs the user will like and would not have found otherwise. 
Some proposals would be:
- more detailed user listening behavior  
  - number of times song was skipped vs. listened to until the end 
  - on average was song listened to 25%,50%,75% vs. 100%
  - if song was listened to right away again (or even repeat song option chosen)
  - what users don't like (questionnaire + memory of any song the user marked as did not like and/or skipped) 
  - user's historical listening data beyond user behvior (questionnaire of songs that defined important moments for them, or trigger memories)
- song wave length
- lyrics sentiment (mood)
- emotion calculation
- cross content user behavior (for example movie taste influence on music taste) 

change

