# 🎬 Movie Recommendation System

## 📖 Overview
This project is a **Movie Recommendation System** that suggests similar movies based on your favorite titles.  
It uses **content-based filtering** — understanding the metadata of each movie (like genres, cast, keywords, and overview) and recommending films that share similar features.  

The app is powered by **Streamlit** for the frontend, and **scikit-learn** for machine learning — all wrapped into a simple, interactive web interface.

---

## 🚀 Features
- 🔍 **Search any movie** from the TMDB 5000 dataset  
- 🎯 **Get top movie recommendations** based on similarity  
- 🖼️ **Fetch movie posters dynamically** using TMDb API  
- ⚡ **Fast, lightweight, and easy to deploy** (Streamlit-based)  
- 🧠 **Content-based filtering model** using cosine similarity  

---

## 🧩 Tech Stack
| Layer | Technologies |
|--------|--------------|
| **Frontend** | Streamlit |
| **Backend / ML** | Python, scikit-learn, pandas, numpy |
| **Data** | TMDb 5000 Movies Dataset |
| **Deployment (Optional)** | Streamlit Cloud / Heroku / Localhost |

---

## 🧠 How It Works

1. **Data Preprocessing**  
   - The dataset `tmdb_5000_movies.csv` is cleaned and relevant columns are extracted (like *overview*, *genres*, *keywords*, *cast*, *crew*).  
   - These textual features are combined into a single “bag of words” per movie.

2. **Feature Extraction**  
   - The text data is converted into numerical vectors using **CountVectorizer**.  
   - Each movie becomes a point in a multi-dimensional feature space.

3. **Similarity Computation**  
   - The system uses **cosine similarity** to measure how close two movies are in feature space.  
   - When a user selects a movie, the system finds and ranks the most similar ones.

4. **Frontend Visualization**  
   - Streamlit provides a clean, responsive UI.  
   - The app fetches movie posters using the **TMDb API** and displays them with movie names.

---

## 🛠️ Installation & Usage

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/yourusername/movie-recommendation-system.git
cd movie-recommendation-system
```

### 2️⃣ Create a Virtual Environment (optional but recommended)
```bash
python -m venv venv
venv\Scripts\activate      # on Windows
source venv/bin/activate   # on macOS/Linux
```

### 3️⃣ Install Dependencies
```bash
pip install -r requirements.txt
```

### 4️⃣ Run the App
```bash
streamlit run app.py
```

Then open the link shown in your terminal (usually `http://localhost:8501`).

---

## 📁 Folder Structure
```
movie-recommendation-system/
│
├── app.py                  # Main Streamlit app
├── movie.pkl               # Pickled similarity model
├── tmdb_5000_movies.csv    # Dataset
├── requirements.txt        # Dependencies
└── venv/                   # Virtual environment (exclude in Git)
```

---

## 🧰 Dependencies
Listed in `requirements.txt`:
```
streamlit
pandas
numpy
scikit-learn
requests
pickle
```

---

## 🧑‍💻 Future Improvements
- 🌍 Add user-based collaborative filtering  
- 🤖 Integrate NLP-based contextual similarity  
- 💾 Use a database for movie metadata storage  
- 📱 Deploy as a web app using Streamlit Cloud  

---

## 🏆 Credits
- **Dataset:** [TMDb 5000 Movie Dataset](https://www.kaggle.com/tmdb/tmdb-movie-metadata)  
- **API:** [The Movie Database (TMDb)](https://www.themoviedb.org/)  
- **Developed by:** *Your Name*  

---

## 💡 Example Screenshot (Optional)
_Add a screenshot here after running the app locally._

```markdown
![App Screenshot](assets/screenshot.png)
```
