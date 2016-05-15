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

##Project Proposal
https://prezi.com/dldm6ttndwxh/one-million/

##Available Features

##Visualization

##Process

###get data

#### read in different data sets

##### hdf5 song details 
(see Getting the Million Song Dataset (HDF5).ipynb)

##### kaggle files

##### lyrics data

#####genre data
   
#### merge different data sets

### clean data

### visualize and analyze data

### get data ready for model

#### add additional features 

#### use k-means clustering to add additional features

####split into 3 portions
Split data into train, cross-validation and test sets. (what percentages?)

### decide on model

### test model 

##Conclusion

##Business / Practical applications
