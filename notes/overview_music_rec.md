## Overview of Music Recommender System

#### My Own Category
- All user's usage pattern to music recommendation (CF)
- One user's usage pattern (Genre or Artist) to music recommendation
- User's emotion to music recommendation 
  
**Here, I focus on the third one, user's emotion to music recommendation**

#### User's emotion to music recommendation 
- Recommend music appropriate for user's current emotion.
- Workflow : Music (audio, lyrics) -> Emotion <- User's emotion
- Advantage
  - Conventional music streaming services provide users keywords-based search for music. Accordingly it strongly relies on user’s prior knowledge and experience. It often fails to expose non-expert users to the music that the users are not familiar with.
- Disadvantage
  - 
- Lyrics to Emotion
  - MusicMood: Predicting the mood of music from song lyrics using machine learning [[arXiv](https://arxiv.org/pdf/1611.00138.pdf)] [[slideshare](http://www.slideshare.net/SebastianRaschka/musicmood-20140912)] 
    - Use Various Naive Bayes model
    - Dataset: MSD (emotion labeled by the author)
  - Identifying the Emotional Polarity of Song Lyrics through Natural Language Processing [[NLP](https://people.eecs.berkeley.edu/~schasins/papers/identifyingEmotionalPolarity.pdf)]
    - Word List, Word Dictionary, Cosine Similarity of TF-IDF scores, Path similarity(WordNet), which is TF-IDF weight with a word-sense similarity weight
    - Dataset: Lyrics.com (emotion labeled by Last.fm tag data or hand)
  
- Tips
  - Mood labels in Last.fm?
  - Or manual labeling based on lyrics and audio from Million Song Dataset.
