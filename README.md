# 🎥 Predictive Analytics for Movie Box Office Success

Welcome to the **Predictive Analytics for Movie Box Office Success** project! This repository showcases the implementation of advanced data-driven methodologies to analyze and predict movie box office performance using a variety of cutting-edge techniques and visualizations.

---

## 📜 Project Overview
This project aims to provide actionable insights and predictions about box office success by leveraging movie-related data. By incorporating advanced feature engineering and sophisticated visualization tools, this project presents a comprehensive analysis for stakeholders in the film industry.

---

## 🧩 Key Features
- **Feature Engineering**: Inclusion of relevant attributes to boost predictive capabilities.
- **Global Market Analysis**: Insights into how production countries and genres influence popularity.
- **Influencer Impact Assessment**: Role of key actors, directors, and producers in determining success.
- **Sentiment Analysis**: Deep learning-based sentiment analysis of movie reviews.
- **Interactive Dashboard**: (Upcoming) A Streamlit-based dashboard for enhanced user experience.

---

## 📂 Repository Structure
```
project-root
│
├── data
│   ├── feature_engineered_movie_data.csv  # Processed dataset used for analysis
│
├── notebooks
│   ├── feature_engineering.ipynb          # Notebook for feature engineering
│   ├── data_visualization.ipynb           # Notebook for advanced visualizations
│
├── visualizations
│   ├── top_genres_by_country.png          # Chart showing genre popularity by country
│
├── scripts
│   ├── data_preprocessing.py              # Script for cleaning and preprocessing data
│   ├── visualization_script.py            # Script for generating visualizations
│
└── README.md                              # Project documentation (you are here!)
```

---

## 📊 Insights from Visualizations
- **Box Office Revenue vs Budget with Popularity**:
~~~
import plotly.express as px

# Load your dataset (replace with the appropriate file path)
file_path = '/content/feature_engineered_movie_data.csv'
movie_data = pd.read_csv(file_path)

# Select relevant columns
bubble_data = movie_data[['budget', 'revenue', 'popularity', 'genres', 'original_title']]

# Create the bubble chart
fig = px.scatter(
    bubble_data,
    x='budget',                # X-axis: Budget
    y='revenue',               # Y-axis: Box Office Revenue
    size='popularity',         # Bubble Size: Popularity
    color='genres',             # Bubble Color: Genre
    hover_name='original_title', # Tooltip: Movie Name
    title='Box Office Revenue vs Budget with Popularity',
    labels={'budget': 'Budget', 'revenue': 'Revenue'},
    size_max=60                # Max size of bubbles
)

# Customize the chart layout
fig.update_layout(
    title_font=dict(size=20, family='Arial', color='black'),
    xaxis=dict(title='Budget (in $)', tickprefix='$', showgrid=True),
    yaxis=dict(title='Revenue (in $)', tickprefix='$', showgrid=True),
    paper_bgcolor='rgb(240, 242, 245)'  # Background color
)

# Show the chart
fig.show()

~~~
![image](https://github.com/user-attachments/assets/d2d8d8cd-dd8c-4d77-bf36-9001a60c30ff)

- **Box Office Revenue vs Budget with Popularity**:

---

## 🛠️ Tech Stack
- **Python**: Primary programming language.
- **Libraries**: 
  - `pandas`, `numpy`: For data manipulation.
  - `plotly.express`: For creating professional and interactive visualizations.
  - `sklearn`, `tensorflow`: For predictive modeling and sentiment analysis.
- **Streamlit**: (Upcoming) For dashboard implementation.

---

## 📈 How to Run the Project
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/movie-box-office-analytics.git
   ```

2. Navigate to the project directory:
   ```bash
   cd movie-box-office-analytics
   ```

3. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

4. Run the scripts in `notebooks` or execute visualizations directly from `scripts`.

---



> "Movies are a window into the culture of the world; let data be the key to understanding them!"
