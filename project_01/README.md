# What Makes a Song a Bop?

## Project Overview
This project investigates whether specific audio features can explain why some songs become popular or “bops.” Using a dataset of over 114,000 tracks scraped from the Spotify API, we explored the relationship between **tempo**, **explicit content**, and **song popularity**. Through data cleaning, correlation analysis, and regression modeling, we tested whether these features significantly contribute to a song’s success.

## Dataset
- **Source**: [Spotify Dataset (Kaggle)](https://www.kaggle.com/datasets/priyamchoksi/spotify-dataset-114k-songs/data)  
- **Size**: 114,000 tracks × 21 features  
- **Unit of Observation**: Song  
- **Key Features**:
  - `popularity` – Spotify popularity score (0–100)  
  - `tempo` – tempo of the track (BPM)  
  - `explicit` – whether the track is explicit (binary)  
  - Other features: danceability, energy, loudness, speechiness, valence, etc.  
- **Limitations**:
  - Some values are estimated (e.g., time signature).  
  - Over 100 unique genres → noisy category variable.  
  - Popularity is subjective and influenced by external factors (e.g., marketing, culture).  

## Methodology
1. **Data Cleaning**
   - Removed a single row with missing `artist`, `album_name`, and `track_name`.  
   - Dropped songs with `tempo = 0` (invalid values).  
   - Converted `explicit` to binary (0 = not explicit, 1 = explicit).  

2. **Exploratory Data Analysis**
   - Distribution of song features.  
   - Comparison of explicit vs non-explicit tracks.  
   - Boxplots and correlation analysis of tempo, explicitness, and popularity.  

3. **Modeling**
   - Correlation matrix of `tempo`, `explicit`, and `popularity`.  
   - Simple **linear regression** with predictors: `tempo` and `explicit`.  
   - Visualization of residuals and fitted values.  

## Results
- **Correlation Findings**:
  - Popularity vs Tempo: ~0.014 → no meaningful relationship.  
  - Popularity vs Explicit: ~0.044 → very weak positive relationship.  
- **Regression Findings**:
  - Neither tempo nor explicit content significantly predicts popularity.  
  - Residual plots and fitted values confirm lack of linearity.  
- **Visualization**:
  - Tempo vs Popularity plot shows almost no trend.  
  - Boxplots show explicit and non-explicit songs have nearly identical popularity distributions.  

## Conclusion
- Tempo and explicit content do **not** strongly influence whether a song becomes a “bop.”  
- Popularity is likely driven by other factors such as **genre, artist reputation, cultural trends, and marketing strategies**.  
- Future work could:
  - Expand features (e.g., genre grouping, lyrical sentiment, artist-level popularity).  
  - Apply advanced models (Random Forest, Neural Networks) to capture non-linear patterns.  
  - Incorporate listener feedback and social media sentiment for richer context.  

## Tools and Technologies
- **Language**: Python  
- **Libraries**: Pandas, NumPy, Scikit-learn, Seaborn, Matplotlib  
- **Techniques**: Data cleaning, correlation analysis, linear regression, visualization  

## How to Run
1. Clone the repository:  
   ```bash
   git clone https://github.com/your-username/data-science-projects.git
   cd data-science-projects/song-popularity
   ```
2. Install dependencies:
  ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn
  ```
3. Open the Jupyter Notebook and run all cells to reproduce the analysis.

## Author

Trustan Gabriel Price

University of Illinois Urbana-Champaign

B.S. in Statistics, Minors in Computer Science and Data Science
