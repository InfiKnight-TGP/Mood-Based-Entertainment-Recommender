# R.E.T.R.O - Entertainment Recommender

A personalized content recommendation system that suggests entertainment options based on users' emotional state, age, and language preferences. The system currently focuses on YouTube content, movies, and music with plans for expansion to other platforms.

## Features

- **Mood-Based Recommendations**: Content suggestions based on 7 emotional states
- **Multi-language Support**: Content delivery in 8 languages
- **Age-Appropriate Content**: Customized content for different age groups
- **Clean UI**: Intuitive Streamlit-based interface
- **YouTube Integration**: Video search and filtering with embedded player
- **Movie Recommendations**: Personalized movie suggestions with detailed information
- **Music Recommendations**: Mood-based music playlist suggestions
- **Coming Soon**: Spotify integration for personalized music recommendations

## Prerequisites

- Python 3.8 or higher
- YouTube Data API v3 key
- TMDB API key and Access Token
- OMDB API key

## Setup

1. Clone the repository:
```bash
git clone <repository-url>
cd R.E.T.R.O
```

2. Create and activate a virtual environment:
```bash
python -m venv .venv
# On Windows
.venv\Scripts\activate
# On Unix or MacOS
source .venv/bin/activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Set up environment variables:
   - Copy `.env.example` to `.env`:
     ```bash
     cp .env.example .env
     ```
   - Fill in your API keys in the `.env` file:
     ```
     YOUTUBE_API_KEY=your_youtube_api_key_here
     TMDB_API_KEY=your_tmdb_api_key_here
     TMDB_ACCESS_TOKEN=your_tmdb_access_token_here
     OMDB_API_KEY=your_omdb_api_key_here
     ```
   - Never commit your `.env` file to version control

5. Run the application:
```bash
streamlit run Home.py
```

## Project Structure

- `Home.py`: Main Streamlit application entry point
- `pages/`: Directory containing different pages of the application
  - `1_YouTube_Videos.py`: YouTube video recommendations
  - `2_YouTube_Music.py`: Music playlist recommendations
  - `3_Movie_Recommendations.py`: Movie recommendations
- `Coming Soon/`: Directory for upcoming features
  - `Spotify.py`: Future Spotify integration
  - `Anime_Recommendations.py`: Future anime recommendations
- `search_queries.json`: Predefined search queries for different moods and age groups
- `music_queries.json`: Predefined music search queries
- `video_fallback_videos.json`: Fallback videos for different moods
- `music_fallback_videos.json`: Fallback music videos
- `requirements.txt`: Project dependencies
- `.env`: Environment variables (create this file)
- `.env.example`: Example environment variables template

## Security Best Practices

### Environment Variables
- Never commit API keys or sensitive credentials to version control
- Keep your `.env` file secure and never share it publicly
- Use `.env.example` as a template for required environment variables
- Regularly rotate your API keys and tokens

### Git Security
- The `.env` file is automatically ignored by git (configured in `.gitignore`)
- If you accidentally commit sensitive information:
  1. Immediately revoke the exposed credentials
  2. Generate new credentials
  3. Update your local `.env` file
  4. Use `git filter-branch` or BFG Repo Cleaner to remove sensitive data from git history
  5. Force push the changes to remove sensitive data from remote repository

### API Key Management
- Use separate API keys for development and production
- Set appropriate API key restrictions (IP, domain, etc.)
- Monitor API usage for any suspicious activity
- Regularly audit and rotate API keys

## Usage

1. Select your current mood from the sidebar
2. Choose your age group
3. Select your preferred language
4. Browse through the recommended content
5. Click on videos to watch them directly in the app

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [Streamlit](https://streamlit.io/) for the amazing web framework
- [YouTube Data API](https://developers.google.com/youtube/v3) for video content
- [TMDB API](https://www.themoviedb.org/documentation/api) for movie data
- [OMDB API](http://www.omdbapi.com/) for additional movie information
- [Spotify API](https://developer.spotify.com/documentation/web-api) for upcoming music features 
