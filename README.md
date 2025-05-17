# Movies React App

A modern ReactJS application that lets you search for movies, view details, manage your profile, and add or remove favorites.

![Movies App Screenshot](https://github.com/benrigaud/react-movies/blob/main/screenshot.png?raw=true)

## Features

- **Movie Search**: Search for movies using the OMDB API
- **Movie Details**: View comprehensive information about each movie
- **Favorites System**: Add and remove movies from your favorites list
- **User Profile**: Save and manage your profile information
- **Responsive Design**: Looks great on both desktop and mobile devices

## Tech Stack

- **React**: Frontend library for building the user interface
- **React Router DOM**: For client-side routing
- **React Hook Form**: Form validation and handling
- **Font Awesome**: Icons and graphics
- **OMDB API**: Movie data source
- **Local Storage**: For persisting user data and favorites
- **Vite**: Fast development and building tool

## Installation

1. Clone the repository
   ```bash
   git clone https://github.com/yourusername/movies-react.git
   cd movies-react
   ```

2. Install dependencies
   ```bash
   npm install
   ```

3. Start the development server
   ```bash
   npm run dev
   ```

4. Open your browser and navigate to `http://localhost:5173`

## Project Structure

```
src/
├── assets/
│   ├── components/      # Reusable UI components
│   ├── views/           # Page components
│   ├── routes/          # Routing configuration
│   ├── utils/           # Helper functions and constants
│   └── react.svg        # React logo
├── hooks/               # Custom React hooks
├── App.jsx              # Main app component
├── App.css              # App styles
├── main.jsx             # Entry point
└── index.css            # Global styles
```

## Key Components

### Header
Contains the website title, navigation menu, and search functionality.

### MovieCard
Displays individual movie information in a grid layout with like/favorite functionality.

### MovieDetail
Shows detailed information about a selected movie including plot, ratings, and cast.

### Favorites
Displays all movies that the user has marked as favorites.

### MovieSearch
Allows users to search for movies by title.

## API Usage

This application uses the OMDB API to fetch movie data. The app is currently using a public API key for demonstration purposes. For production use, please obtain your own API key from [OMDB API](http://www.omdbapi.com/).

Example API usage:
```javascript
const fetchMovies = async (searchTerm) => {
  const response = await fetch(
    `http://www.omdbapi.com/?apikey=f322a02a&s=${searchTerm}`
  );
  const data = await response.json();
  return data.Search;
};
```

## State Management

The application uses React's built-in state management with hooks:
- `useState` for component-level state
- `useEffect` for side effects like API calls
- Custom hooks for shared logic (e.g., `useLikeEvents`)

## Local Storage

The app uses browser local storage to persist data:
- User profile information
- Favorite movies list

## Future Enhancements

- User authentication and server-side persistence
- Movie recommendations based on user preferences
- Advanced filtering and sorting options
- Movie trailer integration
- User reviews and ratings

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- [OMDB API](http://www.omdbapi.com/) for providing movie data
- [Font Awesome](https://fontawesome.com/) for the icons
- [React Hook Form](https://react-hook-form.com/) for form handling
