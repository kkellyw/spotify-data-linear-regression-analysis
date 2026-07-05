## **Linear & Logistic Regression Analysis of Spotify Chart Data**

Team Project for STAT 207 Data Science Exploration

### **Dataset**

This dataset contains audio characteristics of the top 2000 Spotify songs
from 2000–2019. Across 18 columns, things like danceability, genre, and
tempo are recorded. Each row represents one song, and we're also given
the artist name and how popular it was.

### **Research Questions**

#### **Linear Regression**: 
What is the relationship between a song's
danceability and its popularity, after controlling for energy, loudness,
tempo, and acousticness, both in the sample and in the underlying
population? How well does this model predict popularity on new data?

#### **Logistic Regression**: 
How do energy, loudness, and tempo relate to the
log-odds of a song being explicit in the training data? How does a
classifier built on this model perform on new data?

#### **Why this Matters:** 
If someone is trying to increase their odds of
making a very popular song, they may want to look at previously
successful songs and try to determine if there are any patterns that
could be incorporated to increase a song's likelihood of being a hit.
It could also be useful to understand what variables or characteristics
are associated with explicit content, since that's useful for music
platforms or radio stations that mainly appeal to younger audiences and
need to censor their music.

#### **Are we satisfied with this classifier?** 
No. Even with 70% accuracy and 98.6% specificity, a sensitivity of 0.88% means the model fails at the one
thing it needed to do. In the radio host scenario above, nearly every explicit song would be incorrectly cleared as safe to play, which defeats the entire purpose of the classifier.

### **Conclusion**

Both models performed poorly, not as well as we'd hoped: a very low R²
and high RMSE for the linear model, and a low AUC with an extremely low
sensitivity for the logistic model's classifier.

### **Limitations:** 
This dataset is small relative to all songs ever
released, and every song in it already has relatively high popularity
since it's a compilation of top Spotify songs from 2000-2019, and that high
popularity baseline likely made the analysis harder. Findings also can't
be generalized beyond Spotify, since other ways of listening to music
(Apple Music, radio, vinyl) are harder to collect data on and aren't
represented here. We don't want to extrapolate these findings beyond the
reach of this dataset.

### **Continuing this Project:** 
Try forward or backward variable selection to see if
other variables would better predict popularity or explicitness, and
cross-reference with other data sources to see if additional variables
beyond the ones used here matter.
