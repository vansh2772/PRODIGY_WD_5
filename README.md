# Weather App

A beautiful, responsive weather application built with React, TypeScript, and Tailwind CSS. Get real-time weather information for any location worldwide.

## Features

- 🌍 **Global Weather Data** - Get weather information for any city worldwide
- 📍 **Location Services** - Automatic location detection or manual search
- 🎨 **Dynamic Backgrounds** - Background changes based on weather conditions
- 📱 **Responsive Design** - Works perfectly on desktop, tablet, and mobile
- 🔄 **Real-time Updates** - Refresh weather data with a single click
- 🌡️ **Detailed Information** - Temperature, humidity, wind, pressure, visibility, and UV index
- 📅 **5-Day Forecast** - Extended weather forecast
- ⚡ **Fast & Lightweight** - Optimized for performance

## Technologies Used

- **React 18** with TypeScript
- **Tailwind CSS** for styling
- **Vite** for build tooling
- **Lucide React** for icons
- **WeatherAPI.com** for weather data

## Getting Started

### Prerequisites

- Node.js (version 16 or higher)
- npm or yarn

### Installation

1. Clone the repository:
```bash
git clone <your-repo-url>
cd weather-app
```

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm run dev
```

4. Open your browser and navigate to `http://localhost:5173`

## API Configuration

This app uses WeatherAPI.com for weather data. The API key is already configured, but if you need to use your own:

1. Get a free API key from [WeatherAPI.com](https://www.weatherapi.com/)
2. Replace the `API_KEY` in `src/services/weatherService.ts`

## Building for Production

To create a production build:

```bash
npm run build
```

The built files will be in the `dist` directory, ready for deployment.

## Deployment

This app can be deployed to any static hosting service:

- **Netlify**: Drag and drop the `dist` folder
- **Vercel**: Connect your GitHub repository
- **GitHub Pages**: Use GitHub Actions for automatic deployment
- **Firebase Hosting**: Use Firebase CLI

## Project Structure

```
src/
├── components/          # Reusable UI components
├── hooks/              # Custom React hooks
├── services/           # API services
├── types/              # TypeScript type definitions
├── utils/              # Utility functions
└── App.tsx             # Main application component
```

## Features in Detail

### Weather Information
- Current temperature and "feels like" temperature
- Weather conditions with icons
- Humidity, wind speed and direction
- Atmospheric pressure
- Visibility distance
- UV index

### Location Services
- Automatic geolocation detection
- Manual city search with autocomplete
- Support for coordinates and city names

### Responsive Design
- Mobile-first approach
- Optimized for all screen sizes
- Touch-friendly interface

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Weather data provided by [WeatherAPI.com](https://www.weatherapi.com/)
- Icons by [Lucide](https://lucide.dev/)
- Built with [Vite](https://vitejs.dev/) and [React](https://reactjs.org/)