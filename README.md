# Spotify Music Recommendation with Machine Learning

Shiny app that connects with Spotify's API and provides personalized playlist recommendation through machine learning and data visualization 📊.

The app can be seen at http://dungates.shinyapps.io/Spotify.

It is a bit messy now as I used it to learn some stuff, but it could be helpful. I will clean it up in the short future.

Some of the code to access the Spotify data and inspiration is due this post from RCharlie: http://www.rcharlie.com/post/fitter-happier/. Dean Attali's blog was also helpful https://deanattali.com/.

### Pick one or multiple artists

Pick one artist to compare their songs and albums or pick multiple artists to compare them.

### Playlist recommendation

The app recommends two playlists using songs from the selected artists. The recommendation is very naive and it was developed using data from Spotify.

The recommendation engine uses playlists with the keywords "running" and "relax" through Spotify's API and labelled the songs accordingly. Spotify handily provides a set of features for all of their songs so I used these to create a training set where the Spotify features were the predictor variables and the labels "running" and "relax" are the response variables. A logistic regression was trained to predict which playlist songs are most likely to be a match.