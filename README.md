# movie-recommended-system
🎬 Personalized Movie Recommendation System

This project builds a personalized content-based movie recommender system. It suggests movies similar to the one selected by a user, based on text features from movie metadata. Recommendations are displayed interactively with posters using Streamlit as the frontend.

📂 Project Structure

app.py — Streamlit app that powers the interface and recommendation logic

movies.pkl — Preprocessed movie metadata (titles, IDs, etc.)

similarity.pkl — Precomputed similarity matrix between movies 

requirements.txt — Dependencies required to run the project

README.md — Documentation

⚙️ Data Processing

Movie Dataset
Begin with a dataset that includes movie details such as titles, genres, overviews, cast, and crew. A dataset like TMDB 5000 Movies is a common starting point.

Cleaning & Preprocessing
Handle missing values, normalize text (lowercasing, removing stopwords, stemming/lemmatization), and merge relevant features (overview, genres, keywords, cast, and crew) into a single textual representation for each movie.

Feature Engineering
Create a combined “tags” column that captures the essence of each movie. This serves as the basis for vectorization.

🔢 Vectorization

The textual data is converted into numerical vectors using methods such as Bag-of-Words or TF-IDF. These vectors capture similarities between movies. A similarity matrix is then generated, which forms the foundation for recommendations.

🧠 Recommendation Logic (Backend)

The system loads movie data and the precomputed similarity matrix.

When a user selects a movie, the system finds its vector representation.

It then retrieves the most similar movies by comparing vector similarity scores.

The system also fetches posters for each recommended movie using the TMDB API.

🖥️ Frontend (Streamlit)

The user interface is designed with Streamlit:

A dropdown menu lets users select a movie.

A button triggers the recommendation process.

Recommended movies are displayed in a grid with both titles and posters.
