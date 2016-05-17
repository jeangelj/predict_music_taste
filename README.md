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

##Hypothesis

"Pandora was perhaps the frontrunner of combining the two when it started the 'Music Genome Project' way back in 1999 before terms like Big Data even existed. The project considers songs as datasets and analyzes each song using up to 450 distinct musical characteristics or “genes”. A person – a trained music analyst with an actual degree in music – and automated algorithms comb through the song and classify it as Pop/Rock, Hip-Hop/Electronica, Jazz, World Music, and Classical. Decoding the “genes” of the song helps Pandora find the similarities and then successfully predict what a user might like listening to next."
http://www.byteacademy.co/blog/item/121-the-music-industry-is-growing-more-reliant-on-data-science

With the Spotify's recent pruchase of Seed Scientific, the usage for improving music curation through data science in undeniable. 

prediction and curation

- predict popularity of song
- predict next song you will like 

##Project Proposal
https://prezi.com/dldm6ttndwxh/one-million/

##Available Features

from hdf5 10,000 subset:
song_id = 
song_title = 
song_duration = 
song_release_year = 
song_hot = 
song_speed = 
song_energy = 
artist_name = 
song_dance = 
song_bar = 
song_beat = 
song_time_signature = 
song_tat = 
song_mode = 
song_key = 
artist_familar = 
artist_hot = 

##Visualization

##Process

### 1.get data

#### read in different data sets

##### hdf5 song details 
(see Getting the Million Song Dataset (HDF5).ipynb)

Used https://github.com/tbertinmahieux/MSongsDB/blob/master/PythonSrc/hdf5_getters.py 


genre data

##### kaggle files


##### lyrics data

I currently managed to get all of the lyrics data as a sqlite database in AWS EC2 python. 
https://github.com/tbertinmahieux/MSongsDB/blob/master/Tasks_Demos/Lyrics/mxm_dataset_to_db.py

However, I haven't managed to get it into a format where I can merge it with the rest of the data. 

#####genre data
   
#### merge different data sets

### 2. clean data

### 3. visualize and analyze data

### 4. get data ready for model

#### add additional features 

#### use k-means clustering to add additional features

####split into 3 portions
Split data into train, cross-validation and test sets. (what percentages?)

### 5. decide on model

### 6. test model 

##Conclusion
????

##Business / Practical applications

