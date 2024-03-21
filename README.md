![Screenshot 2024-03-19 190937](https://github.com/RFEIST83/Group-4---Project-4/assets/145405658/e6484fde-fa5c-46c0-954b-0aa6b7fe2bb6)

## Taylor Swift

This project delves into an analysis of Taylor Swift's complete discography, focusing on the key musical attributes danceability, energy, valence, duration, volume, speech, and tempo gained from a Spotify dataset.
By utilizing machine learning techniques, we aim to investigate and uncover how these attributes could contribute to the popularity of her music. This study not only sheds light on the intricacies of Swift's songs but also underscores the potential of machine learning in understanding and predicting musical trends in the industry.

The Tools Used

* Excel
* Python
* SQL
* Tableau

#### The Data

The data consisted of Spotify data around every song released from 2006 to 2024 including things such as song name, album, duration, release date and most importantly the attributes Spotify had assigned to each song track. These attricbutes included:

* Danceablity – How easy the song is to dance to.
* Speechniness – How many words are used within the song.
* Tempo – The speed of the song.
* Energy – The energy level of the song.
* Loudness – The volume of the song.
* Acousticness – How acoustic the song sounds.
* Instrumentalness – How much more music there is compared to singing.
* Liveness – How live the song sounds.
* Popularity – A popularity metric.
* Valence – The mood of the song.

On top of this we also obtain and update listening of the Spotify streaming figures for each song, both total streams over the lifetime of the song and average daily streams for each song. 
There was some cleaning of the data that needed to take place with some incorrect characters and extreme outliers removed. Some new columns were also created to provide normalized values for the attributes so they could all be plotted together in a visualisation but the original figures were also left intact to be able to be used in models. 

The data was obtained from two Kaggle Datasets and the streaming numbers were obtained from a separate website then joined together. 

##### Kaggle Datasets:

[Kaggle Dataset 1](https://www.kaggle.com/datasets/jarredpriester/taylor-swift-spotify-dataset?select=taylor_swift_spotify.csv)
[Kaggle Dataset 2](https://www.kaggle.com/datasets/paakhim10/taylor-swift-the-myth-the-legend)

##### Streaming Numbers:

[Streaming Numbers](https://kworb.net/spotify/artist/06HL4z0CvFAxyc27GXpf02.html)

#### The Code

##### The Ideal Song

The process of creating the "Ideal Song" involves gathering a comprehensive dataset of songs and their attributes, followed by preprocessing and feature engineering. This dataset is then analyzed using a Random Forest model to determine the importance of each attribute in predicting the streaming numbers of songs. Subsequently, a Linear Regression model is employed to predict the streaming numbers based on the attribute importance scores. Once predicted, a similarity score between each song and the "ideal" song is calculated, normalized to a 0-100 scale, and used to rank the songs. 
Visualizations in Tableau are then created to display the songs categorized as "perfect" based on their attributes and similarity scores. This iterative process combines machine learning techniques with data visualization to uncover insights into the characteristics contributing to a song's popularity, refining the models based on feedback and new data for continual improvement.

##### The Mood of a Song
The process of mood classification and song recommendation involves utilizing a dataset where each song is classified into categories such as Happy, Sad, Energetic, or Calm based on its valence and energy attributes. Initially, the dataset is preprocessed to handle missing values and encode categorical variables if necessary. Then, a Random Forest model is trained to classify songs into these mood categories and predict the mood of any song in the dataset.
Following the model training, interactive visualizations are constructed around this model. Users can select any song from the dataset, and the visualization will display similar songs with the same mood. This recommendation system leverages the Random Forest model's predictions to identify songs with similar valence and energy attributes. Additionally, users can choose a particular mood they desire, and the visualization will play songs from the dataset that match that mood, providing an immersive and personalized music listening experience.
Overall, this approach combines machine learning classification techniques with interactive data visualizations to enable users to explore songs based on their mood preferences, facilitating discovery and enjoyment of music tailored to their emotional preferences.

##### Future Predictions

A linear regression model was constructed to predict the future success of albums by analysing various features such as album name, song name, popularity, release date, total streaming figures, and average daily streaming figures. The dataset spans from 2006 to 2024, with the model aimed at forecasting album success for another 18 years into the future. 
The linear regression model is trained by fitting the data to understand the relationship between the provided features and album popularity. After fitting the model, predictions are made for future album popularity, considering a span of 18 years beyond the existing dataset. These predictions are then organized into a DataFrame for further analysis and visualization. 
The results are then integrated into Tableau to generate graphs and charts illustrating the projected success levels of different albums over the specified time period. By using this predictive model we can gain insights into potential trends in album popularity.

#### Visusalsations

All the data was outputted from the models in to separate CSV files. These were then imported in to Tableau and joined to the main csv on various coloumns but mainly Song name. This joining allowed for the interactive functionality to work in Tableau where visusalsations could be linked to each other. 

#### Results

The findings from the model analysis revealed that the speechiness of a song emerged as the most influential factor, closely followed by danceability, duration, valence, volume, tempo, and energy. However, the significance of these attributes doesn't solely lie in their order of importance; it's also about the actual values and their frequency in songs recognized for their popularity. After subjecting this data to the linear regression model, it successfully established the ranking of songs based on these attributes, which are deemed crucial for their success. Despite achieving an impressive accuracy rate of nearly 90%, there were intriguing instances where certain songs, despite aligning with the identified attributes of an ideal song, didn't attain the expected level of success. This suggests the presence of external factors influencing song popularity and underscores the subjective nature of art.

The linear regression model for future predictions was also able to successfully plot the potential future popularity of all albums 18 years in to the future. It showed the already successful albums would continue to increase in popularity over time however there were also some albums that would decrease in popularity most notably are the albums Taylor Swift re-recoreded and the album evermore which bottoms out with a very low score at the bottom of the dataset. 


