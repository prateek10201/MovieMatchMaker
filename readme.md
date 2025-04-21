# Personalized Movie Recommendation System

## Overview
This project implements a sophisticated movie recommendation system that provides personalized movie suggestions based on user preferences, mood, regional cinema interests, and discovery options. Using a combination of content-based filtering, collaborative filtering, and contextual awareness, the system delivers highly relevant movie recommendations.

## Features

### Multiple Recommendation Approaches
* **Content-based Recommendations**: Find movies similar to ones you already enjoy
* **Mood-based Suggestions**: Get recommendations that match your current mood
* **Hidden Gems Discovery**: Uncover highly-rated but lesser-known films
* **Regional Cinema Exploration**: Browse movies from specific film industries (Hollywood, Bollywood, Tollywood, etc.)

### Advanced Personalization
* Hybrid recommendation algorithm combining movie content and genre similarity
* Multi-level preference selection for detailed customization
* Rating-based filtering to focus on highly-rated content
* Contextual recommendations based on mood and viewing context

### Interactive Interface
* User-friendly command-line interface
* Step-by-step preference selection
* Detailed movie information in recommendations

## Installation

### Prerequisites
* Python 3.8+
* Pandas
* NumPy
* Scikit-learn
* SciPy

### Setup
1. Clone this repository:
```
git clone https://github.com/yourusername/movie-recommendation-system.git
cd movie-recommendation-system
```

2. Download the dataset and models:
   * Ensure `movies2024.csv` is placed in the project root directory
   * Add models to the `/models` directory (or adjust paths in the code)

## Usage
1. Run the application:
```
python movie_recommender.py
```

2. Follow the interactive prompts to:
   * Select a recommendation type
   * Specify preferences (genres, mood, era, etc.)
   * Refine results (rating threshold, region, etc.)
   * View personalized recommendations

## Project Structure
```
movie-recommendation-system/
├── README.md
├── movie_recommender.py  # Main application
├── data_preprocessing.py # Data processing utilities
├── models/              # Saved model files
│   ├── tfidf_vectorizer.pkl
│   ├── cosine_sim_sample.npy
│   ├── user_features.npy
│   ├── movie_features.npy
│   ├── tfidf_matrix.npz
│   └── genre_mlb.pkl
└── movies2024.csv      # Movie dataset
```

## Technical Implementation

### Recommendation Algorithms
* **Content-Based Filtering**: TF-IDF vectorization of movie overviews and genre encoding
* **Collaborative Filtering**: Matrix factorization using TruncatedSVD
* **Hybrid Approach**: Weighted combination of content-based and collaborative filtering
* **Contextual Recommendations**: Mood-to-genre mapping for contextual suggestions

### Model Optimization
* Memory-efficient sparse matrix representation
* On-demand similarity computation
* Reduced precision (float16) for numeric arrays
* Sampling techniques for large matrices

### Dataset Information
The system uses a comprehensive movie dataset with 9,000+ movies containing:
* Basic movie information (title, year, vote average)
* Genre classifications
* Movie overviews and descriptions
* Regional cinema classification

## Acknowledgments
* Based on the user needs assessment conducted as part of the project requirements
* Optimized for GitHub deployment with models under 100MB
* Designed for educational purposes to demonstrate recommendation system techniques

## Future Improvements
* Web interface for easier interaction
* User profile persistence
* More sophisticated collaborative filtering
* Additional recommendation contexts (e.g., time of day, watching companions)
