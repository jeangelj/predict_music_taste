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

Initially, I planned on using a subset of the Million Song Dataset consisting of 10,000 songs (1%, 1.8GB).
The songs are saved in hdf5 format and had to be loaded a module created by Thierrry Bertin-Mahieux called hdf 5 getter. https://github.com/tbertinmahieux/MSongsDB/tree/master/PythonSrc/DatasetCreation

The main problem I was facing that although I was able to use the this subset in python, it began crashing when I wanted to combine the data with some of the other data sets. I especially struggled to merge it with the user data, since I couldn't use a sample of the user data (when I did that I didn't get all of the user data for the subset I had from the million song set - but user data for random songs). Even an inner join wouldn't work do to the size of the user data 3GB.

However, in 2012 a Kaggle competition called "Million Song Dataset Challenge" was started and provided both song information and user data in txt format. https://www.kaggle.com/c/msdchallenge/data

After experimenting a lot with the limited subsets, I decided to use AWS and pull the whole data sets. The Million Song Set it actually available as a public dataset on AWS. https://aws.amazon.com/datasets/million-song-dataset/

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
????

##Business / Practical applications

