# Weather App

A beautiful weather application with real-time data built with React, TypeScript, and Tailwind CSS.

## Features

- Real-time weather data for any location worldwide
- Beautiful, responsive UI with Tailwind CSS
- TypeScript for type safety
- Location search functionality
- Current weather and 7-day forecast
- Modern React hooks and functional components

## Getting Started

### Prerequisites

- Node.js (version 18 or higher)
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

3. Set up environment variables:
```bash
cp env.example .env
```

4. Add your Meteoblue API key to the `.env` file:
```
VITE_WEATHER_API_KEY=your_api_key_here
```

Get your API key from: [Meteoblue Weather API](https://www.meteoblue.com/en/weather-api)

### Development

Run the development server:
```bash
npm run dev
```

The app will be available at `http://localhost:5173`

### Building for Production

Build the project:
```bash
npm run build
```

Preview the production build:
```bash
npm run preview
```

## Deployment

### Netlify (Recommended)

1. Push your code to GitHub
2. Connect your repository to Netlify
3. Set the build command: `npm run build`
4. Set the publish directory: `dist`
5. Add environment variables in Netlify dashboard:
   - `VITE_WEATHER_API_KEY`: Your Meteoblue API key

### Vercel

1. Install Vercel CLI: `npm i -g vercel`
2. Run: `vercel`
3. Add environment variables in Vercel dashboard

### Manual Deployment

1. Build the project: `npm run build`
2. Upload the `dist` folder to your web server
3. Ensure your server is configured to serve the `index.html` file for all routes

## Environment Variables

| Variable | Description | Required |
|----------|-------------|----------|
| `VITE_WEATHER_API_KEY` | Meteoblue API key | Yes |
| `VITE_WEATHER_BASE_URL` | API base URL (optional) | No |

## Technologies Used

- **React 18** - UI framework
- **TypeScript** - Type safety
- **Vite** - Build tool and dev server
- **Tailwind CSS** - Styling
- **Lucide React** - Icons
- **Meteoblue API** - Weather data

## Project Structure

```
src/
├── components/     # React components
├── hooks/         # Custom React hooks
├── services/      # API services
├── types/         # TypeScript type definitions
├── utils/         # Utility functions
└── main.tsx       # App entry point
```

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

MIT License - see LICENSE file for details