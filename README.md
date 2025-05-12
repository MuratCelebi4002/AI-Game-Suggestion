Advanced Python Project
Game Recommendation System Using TF-IDF Algorithm

1. Project Overview
A system has been developed to recommend similar games based on games the user has played or specified.
The recommendations are based on text-based data such as game descriptions, genres, tags, and screenshots, using similarities calculated with the TF-IDF (Term Frequency-Inverse Document Frequency) algorithm.
User feedback (like or dislike) is also incorporated into the recommendation system to provide more personalized results.

2. Technologies and Libraries Used
Python: The primary programming language for the project.

Tkinter: Used for creating the graphical user interface (GUI).

Pandas: Used for data processing and reading CSV files.

Requests: Used for making HTTP requests to the Steam API and other web services.

BeautifulSoup: Used for HTML cleaning and web scraping.

Scikit-learn: Used for TF-IDF vectorization and similarity calculations.

Threading and ThreadPoolExecutor: Used to speed up API requests and computations with multithreading.

3. Main Components of the Code
a. Cache Management

load_cache and save_cache functions store game information in a JSON file to reduce API requests and improve performance.

b. Steam API Integration

Retrieves the most recently played games based on the user's Steam ID.

son_oynanan_oyuna_oneri function returns the AppIDs of the user's recently played games.

c. Fetching Game Information

bilgi_cek function retrieves a game's description text from the Steam store and cleans it of HTML tags.

This data is used to calculate similarities between games.

d. Similarity Calculation with TF-IDF

onerilen_oyun_mantigi function calculates similarities between the user-specified game and other games.

The TF-IDF algorithm vectorizes the game descriptions, and cosine similarity is used to calculate similarity scores.

e. User Feedback

Users can mark recommended games as "Liked" or "Disliked".

These feedback entries are stored in a CSV file and influence the recommendation scores.

f. Price-Performance Recommendation

onerilen_fiyat_performans_mantigi function retrieves game price data from SteamDB and performs a price-performance analysis.

The game with the best price-to-performance ratio is recommended to the user.

g. User Interface (GUI)

A graphical interface is built using Tkinter.

Users can input a game name or Steam ID to get recommendations.

Recommendations are listed in the interface, and user feedback can be collected.

4. Workflow
Recommendation by Game Name:

The user inputs a game name.

The system analyzes games similar to the input using the TF-IDF algorithm and provides recommendations.

Recommendation by Steam ID:

The user inputs their Steam ID.

The system identifies recently played games and recommends similar ones.

Feedback:

Users can mark recommended games as liked or disliked.

This feedback influences future recommendation results.

Price-Performance Recommendation:

The system determines the game with the best price-performance ratio among the recommendations and presents it to the user.

5. Conclusion
This project aims to recommend the most suitable games to users by analyzing their gaming preferences. With features such as user feedback and price-performance analysis, the recommendation system has been further enhanced. As a result, users can find games that match both their interests and budget.
