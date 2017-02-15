## [Deep content-based music recommendation](http://papers.nips.cc/paper/5004-deep-content-based-music-recommendation.pdf)

#### Problem
- Cold start problem in automatic music recommendation 

#### Why is this important and difficult?
- When no usage data is available, it is not effective for recommending new and unpopular songs.

#### Solution
- Audio signal -> intermediate time-frequency representation (input to the network), which is log-compressed mel-spectrograms with 128 components and the same window size and hop size that we used for the MFCCs (1024 and 512 audio frames respectively) -> Pretraining with windows of 3 seconds sampled randomly from the audio clips to speed up training -> averaged over the predictions for consecutive windows. (latent factors)
- Why CNNs? They allow for intermediate features to be shared between different factors, and because their hierarchical structure consisting of alternating feature extraction layers and pooling layers allows them to operate on multiple timescales. (I don't fully understand this yet)

#### Result
- Datasets : Million Song Datasets (MSD), The Taste Profile Subset used for CF (play counts per song, per user).
- Evaluation scheme : mAP (cut-off : 500), AUC
- Ground truth : Latent factor vectors obtained by applying WMF to the available usage data
- Comparing methods : Multidimensional Linear Regression (MLR), linear regression with Multi-Layer Perceptron (MLP), CNN with MSE, CNN with WPE

### Thoughts
- Content-based recommendation with no use of meta data shows pretty impressive results even though it shows worse performance than CF methods purportedly.
- The proposed model employs latent factors learned from WMF as ground truth to train a deep CNN. However, while it is efficiuent, is it accurate enough to be used as ground truth?
- I want to know why the predicted latent factors seem to be a bit more varied. Does this come from the listening habit of users to listen to songs from the same artist? (WMF follows it while predicted latent factors from CNN doesn't)
