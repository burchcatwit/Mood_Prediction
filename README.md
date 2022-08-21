# Mood Prediction/Classification of Music Using Mel-Spectrogram Based CNN
C. Lo-Badal Burch


#### Updated Model Notebook in Google Colab Here: https://colab.research.google.com/drive/1lsUf4i0VQB49EtdcJ4R6yJT_0LeUSE-X#scrollTo=00f1cc10

## Project Overview
Building upon my previous project: [SEND/RETURN: A simple, multiplayer audio experience powered by content-based song recommendations](https://github.com/Siberian-Breaks/SEND-RETURN) this project aims to predict/categorize the mood of a song, to better dictate the post-processing effect of SEND/RETURN's virtual environment. Currently, the project relies on the Spotify API's audio features, such as **valence**: 
> A measure from 0.0 to 1.0 describing the musical positiveness conveyed by a track. Tracks with high valence sound more positive (e.g. happy, cheerful, euphoric), while tracks with low valence sound more negative (e.g. sad, depressed, angry).
While this has served the project demo well, our testing has proved this to be an innacurate measure at times. This project turns its focus towards building a CNN from scratch, using Mel-Spectrograms created from audio previews of songs, to explore whether Mel-Spectrograms can better predict/classify mood compared to Spotify's valence and a NN built off Spotify's audio features [seen here](https://towardsdatascience.com/predicting-the-music-mood-of-a-song-with-deep-learning-c3ac2b45229e).

## Dataset
The dataset was built using the [create_dataset notebook](https://github.com/burchcatwit/Mood_Prediction/blob/main/create_dataset.ipynb). It will need an updated Spotify Access Token and for directories to be set up for dumping the mp3 audio previews and later created Mel-Spectrogram images. The script works as follows:
- Searches Spotify for the top 5 playlists for a given 'mood'
- Scrapes all songs in each playlist and located their corresponding audio preview url for downloading
- Downloads all audio previews and stores in respective mood folder
- Reads in and converts mp3 to Mel-Spectrogram and stores image in same mood folder

*Note: Once the dataset is created, the audio previews can be deleted as the model is built off images.*

## Process
1) Preprocessing: Once the dataset is created, the images are read in and labeled according to their mood. 325 images are randomly sampled from each mood folder and split 250/75 for training/testing (or 0.77/0.23). The current model uses VGG's ImageNet as its base.

## Conclusion


## Limitations


## Next Steps


