# Music Recommender System using Cosine Similarity

Cosine similarity is typically used in NLP to measure the 
similarity between text and documents. I wanted to explore 
whether it could be applied to music audio features instead 
to recommend songs without needing any user behavior data.

The idea: if two songs share similar acoustic characteristics 
(bpm, energy, danceability, etc.), cosine similarity should 
be able to identify them as similar and recommend them together.

I wrote a full research blog on Medium about this project:
[Cosine Similarity for Recommender Systems](https://medium.com/@edhuang392/recommender-system-using-cosine-similarity-an-honors-research-project-on-music-recommendation-120bfc8806ba)

## How it works

1. User selects an artist
2. User selects a song from that artist
3. The system normalizes all audio features between 0 and 1
4. Cosine similarity is calculated between the selected song 
   and every other song in the dataset
5. Songs are ranked by similarity score and recommended

## Key finding

Songs with similar bpm, energy, and danceability scored high 
cosine similarity values and sounded genuinely similar when 
played together. For example Yellow by Coldplay and The Climb 
by Miley Cyrus scored 0.996, and when played simultaneously 
the bpm matched almost perfectly.

## Dataset

Kaggle: Best Songs on Spotify 2000-2023 (~600 songs)
Audio features include: bpm, energy, danceability, loudness, 
liveness, valence, duration, acousticness, speechiness, 
popularity

## Project Structure

| Folder | Description |
|--------|-------------|
| data/ | Spotify songs dataset |
| src/ | Main recommender system |
| trials/ | Early experiments and approaches |
| tests/ | Testing individual components |

## Tech Stack

Python, Pandas, Scikit-learn, Matplotlib, Seaborn, ipywidgets

## Acknowledgements

Thanks to Professor Bryan Swartout at Skyline College for 
his guidance and peer review on this research project.

## Personal Project
Skyline College · 2023