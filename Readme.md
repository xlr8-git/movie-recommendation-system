# Movie Recommendation System

A comprehensive movie recommendation system that uses content-based filtering to suggest movies based on user preferences. The system includes a web application built with Streamlit and leverages The Movie Database (TMDB) API for rich movie information.

## Project Overview

This movie recommendation system analyzes movie features such as genres, cast, crew, keywords, and plot descriptions to find similar movies. It provides personalized movie recommendations through an interactive web interface with movie posters, trailers, and detailed information.

## Features

- **Content-Based Filtering**: Recommends movies based on similarity in genres, cast, crew, and plot
- **Interactive Web Interface**: User-friendly Streamlit application with dropdown selection
- **Rich Movie Information**: Displays movie posters, trailers, ratings, release dates, and descriptions
- **TMDB Integration**: Fetches real-time movie data from The Movie Database API
- **Responsive Design**: Clean and modern UI with side-by-side poster and trailer display

## Project Structure

```
movie-recommendation-system/
├── dataset/
│   ├── tmdb_5000_movies.csv      # Movie dataset with features
│   └── tmdb_5000_credits.csv     # Cast and crew information
├── web_app/
│   └── movie-recommendation-system.py  # Streamlit web application
├── Jupyter_notebook/
│   └── notebook86c26b4f17.ipynb  # Data analysis and model development
├── model/                        # Directory for trained models
├── README.md                     # Project documentation
└── LICENSE                       # Project license
```

## Dataset

The system uses the TMDB 5000 Movies dataset which includes:

- **tmdb_5000_movies.csv**: Contains movie metadata including:
  - Movie titles, genres, keywords
  - Plot descriptions and taglines
  - Budget, revenue, and runtime information
  - Release dates and ratings

- **tmdb_5000_credits.csv**: Contains cast and crew information including:
  - Actor and actress names
  - Director and crew details
  - Character names and job roles

## Technology Stack

- **Python**: Core programming language
- **Streamlit**: Web application framework
- **Pandas**: Data manipulation and analysis
- **Scikit-learn**: Machine learning algorithms for similarity computation
- **Requests**: HTTP library for API calls
- **Pickle**: Model serialization
- **TMDB API**: Movie database for additional information

## Prerequisites

Before running this project, ensure you have:

- Python 3.7 or higher
- TMDB API key (free registration at [themoviedb.org](https://www.themoviedb.org/settings/api))
- Required Python packages (see Installation section)

## Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/movie-recommendation-system.git
   cd movie-recommendation-system
   ```

2. **Install required packages**
   ```bash
   pip install streamlit pandas scikit-learn requests numpy
   ```

3. **Set up TMDB API key**
   - Register at [themoviedb.org](https://www.themoviedb.org/settings/api)
   - Get your API key from the settings
   - Update the `API_KEY` variable in `web_app/movie-recommendation-system.py`

4. **Prepare the model files**
   - Ensure you have the trained model pickle files
   - Update the pickle file paths in the web application

## Usage

### Running the Web Application

1. **Navigate to the web_app directory**
   ```bash
   cd web_app
   ```

2. **Run the Streamlit application**
   ```bash
   streamlit run movie-recommendation-system.py
   ```

3. **Access the application**
   - Open your web browser
   - Go to `http://localhost:8501`
   - Select a movie from the dropdown
   - Click "Show Recommendation" to get similar movies

### Using the Jupyter Notebook

1. **Open the notebook**
   ```bash
   cd Jupyter_notebook
   jupyter notebook notebook86c26b4f17.ipynb
   ```

2. **Run the cells** to explore the data analysis and model development process

## How It Works

1. **Data Preprocessing**: The system processes movie features including genres, keywords, cast, and crew information
2. **Feature Engineering**: Text features are vectorized using TF-IDF or similar techniques
3. **Similarity Computation**: Cosine similarity is calculated between movies based on their feature vectors
4. **Recommendation Generation**: For a selected movie, the system finds the most similar movies and returns them as recommendations
5. **Rich Information Display**: The web app fetches additional details from TMDB API including posters, trailers, and ratings

## Model Details

The recommendation system uses content-based filtering with the following approach:

- **Text Vectorization**: Converts movie descriptions, genres, and keywords into numerical vectors
- **Similarity Metrics**: Uses cosine similarity to measure movie similarity
- **Recommendation Algorithm**: Selects top-k most similar movies for recommendations

## API Integration

The system integrates with The Movie Database (TMDB) API to provide:

- Movie posters and images
- YouTube trailers
- Detailed movie descriptions
- Release dates and ratings
- Additional metadata

## Customization

You can customize the system by:

- **Adding new features**: Include additional movie attributes in the similarity calculation
- **Modifying the UI**: Customize the Streamlit interface layout and styling
- **Changing recommendation count**: Adjust the number of recommended movies displayed
- **Adding filters**: Implement genre, year, or rating filters

## Troubleshooting

### Common Issues

1. **API Key Error**: Ensure your TMDB API key is correctly set in the application
2. **Missing Model Files**: Verify that the pickle files are in the correct location
3. **Package Dependencies**: Install all required packages using pip
4. **Port Conflicts**: If port 8501 is busy, Streamlit will automatically use the next available port

### Performance Optimization

- Use caching for API calls to improve response times
- Consider using a local database for frequently accessed data
- Implement pagination for large datasets

## Contributing

Contributions are welcome! Please feel free to submit pull requests or open issues for:

- Bug fixes and improvements
- New features and enhancements
- Documentation updates
- Performance optimizations

## License

This project is licensed under the terms specified in the LICENSE file.

## Acknowledgments

- The Movie Database (TMDB) for providing the dataset and API
- Streamlit for the web application framework
- The open-source community for various libraries and tools

## Contact

For questions, suggestions, or support, please open an issue on the GitHub repository.

---

**Note**: This project is for educational and demonstration purposes. The movie recommendations are based on content similarity and may not reflect personal preferences or current availability.
