# Emotipy

This project is an emotion-based music recommendation system that uses natural language processing (NLP), machine learning, and Spotify's API to recommend songs based on the user's mood. The system leverages a fine-tuned Distilled BERT model for emotion detection, clustering songs based on their musical features, and integrating these elements into an interactive chatbot.

## Project Overview
The system is structured around three primary components, each implemented in separate Python notebooks:

Spotipy API & Dataset Creation:

This notebook fetches a dataset of songs from Spotify using the Spotipy API.
The dataset contains information like song name, artist, album, genre, lyrics, tempo, energy, and other musical features.
Key features used for clustering include: valence, acousticness, danceability, energy, tempo, loudness, and instrumentalness.
The data is used to generate a set of songs tagged by emotional state (e.g., sadness, joy, love, anger, fear, surprise).

Emotion Clustering:

In this notebook, the songs are clustered into six core emotions: sadness, joy, love, anger, fear, and surprise.
The clustering is done using K-Nearest Neighbors (KNN), which groups the songs based on their similarity in musical features like energy, tempo, and danceability.
![image](https://github.com/user-attachments/assets/a6d5a141-7e2b-4b50-8d79-1a8200a1a332)


Distilled BERT Model for Emotion Detection:

A pre-trained Distilled BERT model is fine-tuned on a labeled dataset to identify emotions from user input (text or speech).
The model processes the user's response and predicts one of the six emotions. Fine-tuning involves training the model on the labeled dataset to optimize for emotion classification.

Chatbot & Music Recommendation Engine:

The chatbot uses the fine-tuned emotion detection model to interpret the user’s mood based on their responses.
The chatbot then queries the Spotify database for songs that match the identified mood.
Using machine learning techniques, the system provides personalized song recommendations based on the emotional state detected in the user's input.
![image](https://github.com/user-attachments/assets/64eb592f-0014-44a3-bb39-11e3c96bedbc)


## Key Features
Emotion-Based Music Clustering: Songs are categorized into six distinct emotions using features like tempo, energy, and danceability.

NLP for Emotion Detection: A fine-tuned Distilled BERT model is used to identify emotions in user inputs with high accuracy.

Spotify API Integration: Access to millions of songs via Spotify's API, which are tagged with various attributes like mood, genre, and popularity.

Interactive Chatbot: The chatbot uses the user’s responses to predict mood and recommend music accordingly.

Machine Learning: KNN clustering and emotion detection using NLP techniques like BERT enable the system to recommend songs based on mood.

## Dataset Details
The dataset used in this project contains the following columns:

song_id: Unique identifier for the song.

song_name: Name of the song.

artist_name: Artist who performs the song.

album_name: Album the song appears on.

release_year: Year the song was released.

duration: Length of the song in seconds.

genre: Genre of the song.

mood: Emotional state conveyed by the song.

lyrics: Text of the song's lyrics.

tempo: Beats per minute (BPM).

key: Musical key of the song.

mode: Major or minor mode of the song.

popularity: Popularity measure (e.g., play count).

acousticness: Measure of the song’s acoustic qualities.

danceability: Measure of the song’s danceability.

energy: Measure of the song’s energy.

instrumentalness: Measure of the song’s instrumental content.

liveness: Measure of the song’s live performance feel.

speechiness: Measure of the song’s spoken word content.

valence: Measure of the song’s positivity or cheerfulness.

## How It Works
Emotion Clustering: The system uses machine learning to cluster songs into different emotional categories based on their musical features. For example, songs with a higher valence are categorized as "happy," while those with more subdued features may be categorized as "sad."

Emotion Detection: The chatbot asks users a series of questions to determine their current mood. These responses are processed using the fine-tuned Distilled BERT model to classify the emotion.

Music Recommendation: Based on the detected emotion, the system recommends songs that match the mood. For example, if the user is feeling happy, the system might suggest upbeat, energetic songs, while a user feeling sad may be recommended slower, more mellow tracks.

## Technologies Used
Spotipy API: To fetch music data from Spotify.

Python (Jupyter Notebooks): For the data preprocessing, emotion clustering, and model training.

Distilled BERT: For emotion detection from text input.

K-Nearest Neighbors (KNN): For clustering songs based on musical features.

TensorFlow: For training and deploying the chatbot's emotion detection model
