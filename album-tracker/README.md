# Album Tracker

Album Tracker is a web application built using React and Vite that allows users to search for music albums, listen to song previews, and manage their personal album collection. Users can save albums, update their listening status, give star ratings, and write notes. The application also includes a Deezer player option and AI-powered music recommendations using Google Gemini based on the user's saved albums and ratings.

# Screenshot

![search result](image.png)
![album page](image-1.png)
![recommendation](image-2.png)

# Live Website

https://album-tracker-murex.vercel.app/

# GitHub Repository

https://github.com/rye-dev08/album-tracker

# Features

- Search for music albums using the iTunes API.
- View album information and track lists.
- Listen to 30-second song previews using the mini player.
- Save albums to a personal collection.
- Update album listening status.
- Give star ratings and add personal notes.
- Filter and sort saved albums.
- Keep saved collection data in browser local storage.
- Access the Deezer album player.
- Get personalized album recommendations using Google Gemini.

# Tech Stack

- React
- Vite
- React Context API
- iTunes API
- Deezer API
- Google Gemini API
- Vercel
- JavaScript, HTML, and CSS

# How to Run Locally

1. Clone the GitHub repository:

   `git clone https://github.com/rye-dev08/album-tracker.git`

2. Open the project directory:

   `cd album-tracker`

3. Install the required dependencies:

   `npm install`

4. Create a `.env.local` file in the project root.

5. Add your Gemini API key:

   `GEMINI_API_KEY=your_api_key_here`

6. Start the development server:

   `npm run dev`

7. Open the local URL displayed in the terminal.

# Limitations

- Music previews are limited to approximately 30 seconds.
- Saved albums, ratings, notes, and listening status are stored only in the user's browser.
- Collection data does not automatically sync between different devices or browsers.
- Deezer may require users to log in to access full tracks, depending on account and regional restrictions.
- AI recommendations require an internet connection and a valid Gemini API key.

# Privacy Note

The application stores the user's album collection locally in the browser. When users request AI recommendations, the application sends information about their saved albums, including album titles, artists, ratings, and listening status, to the Google Gemini API to generate recommendations. The Gemini API key is stored in environment variables and is not included in the public source code.

# Disclaimer

This project was developed for educational purposes as part of a React and Vite laboratory activity. It is not affiliated with, endorsed by, or officially connected to Apple, Spotify, Deezer, or Google.

# Reflection Question

1. Why is the audio element stored in a useRef instead of useState?

The audio element is stored in useRef because it allows us to access and control the audio directly without re-rendering the component. It is useful for playing, pausing, and controlling the audio without affecting the other parts of the application.

2. Why do all API calls live in services/ instead of inside components?

All API calls are placed inside the services folder to keep the code organized and easier to understand. It also helps us separate the API functions from the components, making the code easier to maintain and reuse.

3. Why can the Gemini key not be placed in React code? What could happen if you pushed it to GitHub?

The Gemini API key should not be placed in React code because other people might be able to see and use it. If we upload it to GitHub, someone could steal the key and use it without our permission, which could affect our API usage.

4. Why is this recommender an LLM prompt and not a trained machine learning model? Give one strength and one weakness.

The recommender uses an LLM prompt because it uses an existing AI model to analyze our saved albums instead of training our own machine learning model. One strength is that it can provide recommendations without needing to train a model, but one weakness is that the recommendations may not always be accurate.

5. Describe the hardest bug you hit and how you fixed it.

The hardest bug I encountered was when the Deezer API was not working and showed a Local API error instead of returning the album results. I fixed it by checking the code, correcting the errors from copying the PDF, and testing the API again until it successfully returned the album list.