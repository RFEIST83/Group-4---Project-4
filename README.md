![Screenshot 2024-03-19 190937](https://github.com/RFEIST83/Group-4---Project-4/assets/145405658/e6484fde-fa5c-46c0-954b-0aa6b7fe2bb6)

## Taylor Swift

This project delves into an analysis of Taylor Swift's complete discography, focusing on the key musical attributes danceability, energy, valence, duration, volume, speech, and tempo gained from a Spotify dataset.
By utilizing machine learning techniques, we aim to investigate and uncover how these attributes could contribute to the popularity of her music. This study not only sheds light on the intricacies of Swift's songs but also underscores the potential of machine learning in understanding and predicting musical trends in the industry.
The Tools Used

•	Excel
•	Python
•	SQL
•	Tableau

#### The Data

The data consisted of Spotify data around every song released from 2006 to 2024 including things such as song name, album, duration, release date and most importantly the attributes Spotify had assigned to each song track. These attricbutes included:

•	Danceablity – How easy the song is to dance to.
•	Speechniness – How many words are used within the song.
•	Tempo – The speed of the song.
•	Energy – The energy level of the song.
•	Loudness – The volume of the song.
•	Acousticness – How acoustic the song sounds.
•	Instrumentalness – How much more music there is compared to singing.
•	Liveness – How live the song sounds.
•	Popularity – A popularity metric.
•	Valence – The mood of the song.

On top of this we also obtain and update listening of the Spotify streaming figures for each song, both total streams over the lifetime of the song and average daily streams for each song. 
There was some cleaning of the data that needed to take place with some incorrect characters and extreme outliers removed. Some new columns were also created to provide normalized values for the attributes so they could all be plotted together in a visualisation but the original figures were also left intact to be able to be used in models. 

The data was obtained from two Kaggle Datasets and the streaming numbers were obtained from a separate website then joined together. 

##### Kaggle Datasets:

[Kaggle Dataset 1](https://www.kaggle.com/datasets/jarredpriester/taylor-swift-spotify-dataset?select=taylor_swift_spotify.csv)
[Kaggle Dataset 2](https://www.kaggle.com/datasets/paakhim10/taylor-swift-the-myth-the-legend)

##### Streaming Numbers:

[Streaming Numbers](https://kworb.net/spotify/artist/06HL4z0CvFAxyc27GXpf02.html)

#### The Code

All the datasets were joined together on song name and placed in an SQLite database. From here each of us built multiple models using Linear Regression and Random Forrest to explore the dataset. 

