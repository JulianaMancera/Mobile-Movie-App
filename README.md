# 📱 Mobile Movie App - MovieVerse

## LANGUAGES

![TypeScript](https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white)
![React Native](https://img.shields.io/badge/react_native-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB)
![Node.js](https://img.shields.io/badge/node.js-%2343853D.svg?style=for-the-badge&logo=node.js&logoColor=white)

## About

**MovieVerse** is a React Native application designed to provide users with a seamless experience for browsing and discovering movies. This app aims to solve the problem of scattered movie information across various platforms by centralizing movie details, trailers, and ratings in one convenient mobile application.

This project targets movie enthusiasts, casual viewers, and anyone looking for a quick and easy way to find information about movies. Built using React Native, the app leverages the power of TypeScript for type safety and modern JavaScript features. It follows a component-based architecture, making it highly maintainable and scalable. The app uses external APIs to fetch movie data, ensuring users have access to the latest information.

The unique selling point of this app is its focus on simplicity and ease of use, providing a clean and intuitive interface for users to quickly find the movies they are interested in.

## ✨ Features

- 🎯 **Movie Discovery**: Browse a vast catalog of movies with detailed information.
- ⚡ **Performance**: Optimized for smooth scrolling and fast loading times.
- 🎨 **UI/UX**: User-friendly interface for easy navigation.
- 📱 **Responsive**: Designed for both iOS and Android platforms.
- 🛠️ **Search**: Quickly find movies by title, genre, or actor.

## 🎬 Demo

🔗 **Live Demo**: (placeholder

### Screenshots
![Main Interface]

![Movie Details]


## 🚀 Quick Start

Clone and run in 3 steps:
```bash
git clone https://github.com/JulianaMancera/Mobile-Movie-App.git
cd Mobile-Movie-App
npm install && npm start
```

Follow the on-screen instructions to run the app on your emulator or device.

## 📦 Installation

### Prerequisites
- Node.js 18+ and npm
- Git
- Expo CLI (`npm install -g expo-cli`)

### Steps

```bash
# Clone repository
git clone https://github.com/JulianaMancera/Mobile-Movie-App.git
cd Mobile-Movie-App

# Install dependencies
npm install

# Start development server
npm start
```

You can then scan the QR code with the Expo Go app on your iOS or Android device, or run it in an emulator.

## 💻 Usage

### Basic Usage

After installation, simply run `npm start` to start the development server. The app will automatically reload when you make changes to the code.

```typescript
// Example: Fetching movie data
import { useEffect, useState } from 'react';

const MovieList = () => {
  const [movies, setMovies] = useState([]);

  useEffect(() => {
    const fetchMovies = async () => {
      // Replace with actual API call
      const response = await fetch('https://api.example.com/movies');
      const data = await response.json();
      setMovies(data);
    };

    fetchMovies();
  }, []);

  return (
    <ul>
      {movies.map(movie => (
        <li key={movie.id}>{movie.title}</li>
      ))}
    </ul>
  );
};

export default MovieList;
```

## ⚙️ Configuration

### Environment Variables

Create a `.env` file in the root directory:

```env
API_KEY=your_api_key_here
BASE_URL=https://api.themoviedb.org/3/
IMAGE_BASE_URL=https://image.tmdb.org/t/p/w500
```

### Configuration File

```json
{
  "name": "mobile-movie-app",
  "version": "1.0.0",
  "expo": {
    "name": "Mobile Movie App",
    "slug": "mobile-movie-app",
    "version": "1.0.0",
    "orientation": "portrait",
    "icon": "./assets/icon.png",
    "splash": {
      "image": "./assets/splash.png",
      "resizeMode": "contain",
      "backgroundColor": "#ffffff"
    },
    "updates": {
      "fallbackToCacheTimeout": 0
    },
    "assetBundlePatterns": [
      "**/*"
    ],
    "ios": {
      "supportsTablet": true
    },
    "android": {
      "adaptiveIcon": {
        "foregroundImage": "./assets/adaptive-icon.png",
        "backgroundColor": "#FFFFFF"
      }
    },
    "web": {
      "favicon": "./assets/favicon.png"
    }
  }
}
```

## 📁 Project Structure

```
Mobile-Movie-App/
├── 📁 assets/                 # Static assets (images, icons)
├── 📁 components/             # Reusable UI components
├── 📁 navigation/             # Navigation setup
├── 📁 screens/                # Application screens
├── 📁 services/               # API service functions
├── 📁 styles/                 # Styling files
├── 📄 App.tsx                 # Application entry point
├── 📄 app.json                # Expo configuration file
├── 📄 package.json            # Project dependencies
├── 📄 README.md               # Project documentation
└── 📄 .gitignore              # Git ignore rules
```

### Development Setup
```bash
# Fork and clone the repo
git clone https://github.com/yourusername/Mobile-Movie-App.git

# Install dependencies
npm install

# Create a new branch
git checkout -b feature/your-feature-name

# Make your changes and test
npm test

# Commit and push
git commit -m "Description of changes"
git push origin feature/your-feature-name
```

### Code Style
- Follow existing code conventions
- Run `npm run lint` before committing
- Add tests for new features
- Update documentation as needed

## Testing

Run tests using Jest:

```bash
npm test
```

## Deployment

### Expo

To deploy to Expo, run:

```bash
expo publish
```

Follow the prompts to publish your app.

### Standalone Builds

For standalone iOS and Android builds, refer to the Expo documentation: [https://docs.expo.dev/distribution/building-standalone-apps/](https://docs.expo.dev/distribution/building-standalone-apps/)

## FAQ

**Q: How do I add a new movie API?**

A: Modify the `services/api.ts` file to include your new API endpoint.

**Q: How do I customize the theme?**

A: Edit the styles in the `styles/` directory.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- 📚 **Libraries used**:
  - [React Navigation](https://reactnavigation.org/) - Navigation library
  - YT source = https://www.youtube.com/watch?v=f8Z9JyB2EIE

- 👥 **Programmed / Improve By:** Juliana Mancera
