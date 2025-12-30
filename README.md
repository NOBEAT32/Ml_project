I am a data science enthusiast with a strong interest in machine learning–driven recommendation systems. This repository showcases a RAM-efficient hybrid song recommendation system that combines audio feature similarity and text-based metadata similarity.
The system uses cosine similarity computed on demand (instead of precomputing N×N matrices) to ensure scalability and memory efficiency. Audio features are standardized and compared using cosine similarity, while song titles are vectorized using TF-IDF. The final recommendations are generated through a weighted hybrid approach.
Key highlights:
Content-based recommendation using Spotify-style audio features
Text similarity using TF-IDF on song titles
Hybrid similarity with tunable weights
Memory-efficient, scalable design (O(N) per query)
Clean, reproducible preprocessing and serialization
I enjoy building systems that balance theoretical correctness with practical constraints such as memory usage and scalability.

#Feature Engineering
The following feature engineering steps were applied:
Selected core audio features relevant for musical similarity (danceability, energy, loudness, tempo, etc.)
Created interaction features such as Energy × Liveness to capture live-performance intensity
Applied skew analysis to identify heavily skewed features and used appropriate transformations where necessary
Excluded popularity-based features from similarity computation to avoid recommendation bias
Merged metadata fields (title, artist, album, channel) for optional text-based similarity using TF-IDF
Standardized numeric features to ensure balanced cosine similarity computation
These steps improved interpretability, stability, and recommendation quality.
