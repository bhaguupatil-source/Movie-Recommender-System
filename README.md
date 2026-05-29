
# Movie Recommender System 🎬

A content-based movie recommendation engine built with Python and deployed as an interactive web application using Streamlit. This project analyzes movie metadata to suggest films similar to a user's selection.

## 🚀 Overview
This system uses the **TMDB 5000 Movies Dataset** to recommend movies based on their content (genres, keywords, cast, and crew). It transforms text-based metadata into numerical vectors to calculate similarity.

## ✨ Features
* **Interactive UI**: Built with Streamlit for a seamless user experience.
* **Content-Based Filtering**: Recommendations are based on movie attributes rather than user ratings.
* **Fast Retrieval**: Uses a pre-computed similarity matrix for near-instant recommendations.
* **Poster Integration**: (Optional) Fetches movie posters via the TMDB API to enhance the UI.

## 🛠️ Tech Stack
* **Frontend**: [Streamlit](https://streamlit.io/)
* **Data Analysis**: Pandas, NumPy
* **Machine Learning**: Scikit-learn (CountVectorizer, Cosine Similarity)
* **Natural Language Processing**: NLTK (PorterStemmer)
* **Serialization**: Pickle

## 📂 Project Structure
* `movie-recommender-system.ipynb`: The core notebook containing data cleaning, preprocessing, and model building.
* `app.py`: The Streamlit script to run the web application.
* `movie_dict.pkl`: Serialized dictionary containing processed movie data.
* `similarity.pkl`: Serialized cosine similarity matrix.

## ⚙️ Setup and Installation

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/movie-recommender-system.git](https://github.com/your-username/movie-recommender-system.git)
    cd movie-recommender-system
    ```

2.  **Install dependencies:**
    ```bash
    pip install streamlit pandas scikit-learn nltk
    ```

3.  **Run the application:**
    ```bash
    streamlit run app.py
    ```

## 🧠 How It Works
1.  **Data Preprocessing**: Relevant features (genres, keywords, cast, crew) are extracted and cleaned.
2.  **Tag Creation**: All features are combined into a single "tags" column and converted to lowercase.
3.  **Stemming**: NLTK's PorterStemmer is used to reduce words to their root form (e.g., "loving" and "love" become "love").
4.  **Vectorization**: Text tags are converted into a 5000-dimensional vector space using `CountVectorizer`.
5.  **Similarity**: Cosine Similarity is calculated between all movie vectors. The movies with the smallest "distance" to the selected film are recommended.

---
*Developed as a Data Science & AI project.*
```# Movie-Recommender-System
