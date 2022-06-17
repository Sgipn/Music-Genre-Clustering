# Music-Genre-Clustering
Collaborators: Jeff Anderson, James Jiang, Kevin Xu

This is a final project for STA142B- Unsupervised Statistical Learning Methods at UC Davis. 

Music information retrieval is an emerging sub-topic of audio-clustering, a discipline that has grown in popularity in recent years. The purpose of this project is to build a robust unsupervised model that clusters music audio mp3 files by genre.

Our approach is to first extract and generate a selection of audio features based on spectral and rhythmic characteristics. To do this, we investigated various functions from the `librosa` Python package, and selected feature groups and associated features that we felt would be important for distinguishing genres. Next, we applied various combinations of linear and nonlinear dimension reduction techniques (Principal component analysis, Multidimensional Scaling, Local linear embedding) to our data which were tuned using scree-plots and quasi-scree plots that use stress. Finally, we utilized various clustering techniques to cluster our data. To tune our dimension- clustering hyperparameters, we created a grid-search using the silhouette score, observed the associated scatterplot color-coded by clustering index, and listened to how the audio files sound. 

We find that the PCA dimension reduction technique with 3 PCA components, with K-Means clustering and k=3 clusters, achieved the highest performing clustering results.


How to navigate this project:
* `data`: contains 90 mp3 audio files used in our analysis.
* `notebooks`: contains feature extraction, feature generation, dimension reduction, clustering implementation Jupyter notebooks.
* `report`: contains a pdf of our final report.
