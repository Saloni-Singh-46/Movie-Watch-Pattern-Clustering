# 🎬 Movie Watch Pattern Clustering

This project uses unsupervised machine learning (K-Means clustering) to group users based on their movie-watching behavior. The goal is to uncover distinct patterns from:
- 🕒 Time of watching
- 🎭 Genre preference
- ⭐ Rating behavior

These clusters can help drive personalized recommendations, targeted marketing, and behavioral insights for streaming platforms.

---

## 📂 Dataset

The dataset `movie_watch.csv` contains the following features:

| Column             | Description                                                  |
|--------------------|--------------------------------------------------------------|
| `watch_time_hour`  | Hour of the day (0–23) the user typically watches movies     |
| `genre_preference` | Preferred genre (e.g., action, comedy, thriller)             |
| `avg_rating_given` | Average movie rating given by the user (e.g., 1–5 scale)     |

---

## 🧠 Methodology

### 1. **Preprocessing**
- One-Hot Encoding for `genre_preference`
- StandardScaler for `watch_time_hour` and `avg_rating_given`

### 2. **Feature Matrix**
- Final feature set: scaled `watch_time_hour`, `avg_rating_given`, and genre binaries

### 3. **Clustering**
- K-Means algorithm
- Elbow method used to determine optimal `k=3`
- Users assigned to one of three clusters

### 4. **Visualization**
- PCA used to reduce dimensions for plotting
- Scatter plot to visualize clusters in 2D space

---

## 📊 Results

The analysis revealed 3 user clusters:

| Cluster | Viewing Time      | Genre Preference | Rating Behavior |
|---------|-------------------|------------------|-----------------|
| 0       | Afternoon          | Action/Thriller  | Average rater   |
| 1       | Early Morning      | Comedy           | Critical rater  |
| 2       | Late Night         | Thriller         | Generous rater  |

---

## 🛠 Technologies Used

- Python 3.x
- Pandas, NumPy
- Scikit-learn (KMeans, PCA, preprocessing)
- Matplotlib, Seaborn

---

## 🚀 How to Run

1. Clone this repo  
```bash
git clone https://github.com/yourusername/movie-watch-clustering.git
cd movie-watch-clustering
