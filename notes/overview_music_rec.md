## Overview of Music Recommender System

#### My Own Category
- All user's usage pattern to music recommendation (CF)
- One user's usage pattern (Genre, Artist, Trend) to music recommendation (Neighborhood method)
- User's emotion to music recommendation 
  
**Here, I focus on the third one, user's emotion to music recommendation**

#### User's emotion to music recommendation 
- Recommend music appropriate for user's current emotion.
- Workflow : Music (audio, lyrics) -> Emotion <- User's emotion
- Advantage
  - Conventional music streaming services provide users keywords-based search for music. Accordingly it strongly relies on user’s prior knowledge and experience. It often fails to expose non-expert users to the music that the users are not familiar with.
- Disadvantage
  - Difficult to implement and experiment.
  
- Lyrics to Emotion
  - LYRIC TEXT MINING IN MUSIC MOOD CLASSIFICATION [[ISMIR09](http://www.ismir2009.ismir.net/proceedings/PS3-4.pdf)]
    - 18 mood categories (consistent with Russel's mood model), Execellent pre-processing, LIBSVM as a classifier
    - Dataset: In-house audio tracks, lyrics from LyricWiki.org
  - WHEN LYRICS OUTPERFORM AUDIO FOR MUSIC MOOD CLASSIFICATION: A FEATURE ANALYSIS [[ISMIR10](http://ismir2010.ismir.net/proceedings/ismir2010-106.pdf)]
    - 18 mood categories (consistent with Russel's mood model)
    - Dataset: same as in ISMIR 09 paper
  - Improving Mood Classification in Music Digital Libraries by Combining Lyrics and Audio [[JCDL10](http://dl.acm.org/citation.cfm?id=1816146)]
    - 18 mood categories, used complex text feature.
    - Dataset: same as in ISMIR 09 paper
  - MusicMood: Predicting the mood of music from song lyrics using machine learning [[arXiv](https://arxiv.org/pdf/1611.00138.pdf)] [[slideshare](http://www.slideshare.net/SebastianRaschka/musicmood-20140912)] 
    - Use Various Naive Bayes model
    - Dataset: MSD (emotion labeled by the author)
  - Identifying the Emotional Polarity of Song Lyrics through Natural Language Processing [[NLP](https://people.eecs.berkeley.edu/~schasins/papers/identifyingEmotionalPolarity.pdf)]
    - Word List, Word Dictionary, Cosine Similarity of TF-IDF scores, Path similarity(WordNet), which is TF-IDF weight with a word-sense similarity weight
    - Dataset: Lyrics.com (emotion labeled by Last.fm tag data or hand)
  - Multimodal Music Mood Classification using Audio and Lyrics [[ICMLA08](http://ieeexplore.ieee.org/abstract/document/4725050/?part=1)]
    - SVM, k-NN, 4 categories
    - Dataset: LyricWiki, Last.fm tag, Human checking

- Sentiment categories
  - 4 categories looks plausible.
  
- Audio Features
  - Timbral(MFCC, spectral centroid), rhythmic (tempo, onset rate), tonal (like Harmonic Pitch Class Profiles), and temporal description
    
- Tips
  - Mood labels in Last.fm?
  - Or manual labeling based on lyrics and audio from Million Song Dataset.
