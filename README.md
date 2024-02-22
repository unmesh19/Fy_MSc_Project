# Movie Recommendation System using IMDb Dataset

## Overview
This project is a movie recommendation system based on cosine similarity using a dataset extracted from IMDb. It suggests similar movies to a user based on the movie they input.

## Dataset
The dataset used in this project is a subset of IMDb movies containing information such as genres, overview, plot keywords, director, top cast members, and writers.

## Workflow
1. **Data Preprocessing**: 
    - Selected relevant columns such as `Genres`, `Overview`, `Plot Keyword`, `Director`, `Top 5 Casts`, and `Writer`.
    - Created a new DataFrame and concatenated selected columns.
    - Converted text data to lowercase and filled missing values with empty strings.
  
2. **Text Processing**:
    - Utilized CountVectorizer to convert text data into a matrix of token counts.
    - Computed cosine similarity between movie descriptions to find similarities.

3. **Recommendation**:
    - Prompted the user to enter a movie name.
    - Used the `difflib` library to find the best match for the entered movie name.
    - Suggested similar movies based on cosine similarity scores.

## Usage
1. Ensure you have Python installed along with the required libraries (`pandas`, `scikit-learn`).
2. Download the IMDb dataset (`25k IMDb movie Dataset.csv`) and place it in the same directory as the Python script.
3. Run the script and enter the name of the movie you want recommendations for.

## Example
```
Enter the movie name : Star Wars
Star Wars
Movies suggested for you : 

1. Star Wars: Episode I - The Phantom Menace
2. Star Wars: Episode VI - Return of the Jedi
3. Star Wars: Episode III - Revenge of the Sith
4. Star Wars: Episode II - Attack of the Clones
5. Untitled Star Wars/Kevin Feige Project
```
