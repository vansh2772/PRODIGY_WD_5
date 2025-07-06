# Deployment Guide

This guide will help you deploy your Weather App to various platforms.

## Netlify Deployment (Recommended)

### Method 1: Drag & Drop (Quick)

1. **Build your project locally:**
   ```bash
   npm run build
   ```

2. **Deploy to Netlify:**
   - Go to [netlify.com](https://netlify.com)
   - Sign up/Login with your GitHub account
   - Drag and drop the `dist` folder to the Netlify dashboard
   - Your site will be live instantly!

3. **Set up environment variables:**
   - Go to Site settings → Environment variables
   - Add: `VITE_WEATHER_API_KEY` = your Meteoblue API key

### Method 2: Git Integration (Recommended for updates)

1. **Push your code to GitHub:**
   ```bash
   git add .
   git commit -m "Initial commit"
   git push origin main
   ```

2. **Connect to Netlify:**
   - Go to [netlify.com](https://netlify.com)
   - Click "New site from Git"
   - Choose GitHub and select your repository
   - Set build command: `npm run build`
   - Set publish directory: `dist`
   - Click "Deploy site"

3. **Configure environment variables:**
   - Go to Site settings → Environment variables
   - Add: `VITE_WEATHER_API_KEY` = your Meteoblue API key
   - Redeploy the site

### Method 3: Netlify CLI

1. **Install Netlify CLI:**
   ```bash
   npm install -g netlify-cli
   ```

2. **Login to Netlify:**
   ```bash
   netlify login
   ```

3. **Deploy:**
   ```bash
   npm run build
   netlify deploy --prod --dir=dist
   ```

## Vercel Deployment

1. **Install Vercel CLI:**
   ```bash
   npm install -g vercel
   ```

2. **Deploy:**
   ```bash
   vercel
   ```

3. **Set environment variables:**
   - Go to your Vercel dashboard
   - Navigate to Settings → Environment Variables
   - Add: `VITE_WEATHER_API_KEY` = your Meteoblue API key

## GitHub Pages Deployment

1. **Add GitHub Pages dependency:**
   ```bash
   npm install --save-dev gh-pages
   ```

2. **Update package.json:**
   ```json
   {
     "scripts": {
       "predeploy": "npm run build",
       "deploy": "gh-pages -d dist"
     }
   }
   ```

3. **Deploy:**
   ```bash
   npm run deploy
   ```

## Firebase Hosting

1. **Install Firebase CLI:**
   ```bash
   npm install -g firebase-tools
   ```

2. **Login to Firebase:**
   ```bash
   firebase login
   ```

3. **Initialize Firebase:**
   ```bash
   firebase init hosting
   ```

4. **Build and deploy:**
   ```bash
   npm run build
   firebase deploy
   ```

## Environment Variables Setup

### Required Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `VITE_WEATHER_API_KEY` | Meteoblue API key | `QFxesIZP3NnK6jCb` |

### How to Get API Key

1. Go to [Meteoblue Weather API](https://www.meteoblue.com/en/weather-api)
2. Sign up for a free account
3. Generate an API key
4. Add it to your deployment platform's environment variables

## Troubleshooting

### Common Issues

1. **Build fails:**
   - Ensure Node.js version 18+ is installed
   - Run `npm install` to install dependencies
   - Check for TypeScript errors: `npm run lint`

2. **API calls fail:**
   - Verify your API key is correct
   - Check environment variables are set
   - Ensure the API key has proper permissions

3. **Page shows 404 on refresh:**
   - This is normal for SPA routing
   - Netlify/Vercel should handle this automatically
   - For other platforms, configure redirects to `index.html`

4. **Environment variables not working:**
   - Ensure variable names start with `VITE_`
   - Redeploy after adding environment variables
   - Check platform-specific documentation

### Performance Optimization

1. **Enable compression:**
   - Most platforms enable gzip automatically
   - Check your platform's documentation

2. **Cache optimization:**
   - Static assets are cached automatically
   - Consider adding cache headers for API responses

3. **CDN:**
   - Netlify and Vercel provide global CDN
   - Consider using a CDN for better performance

## Monitoring

1. **Analytics:**
   - Netlify Analytics (paid)
   - Google Analytics
   - Vercel Analytics

2. **Error tracking:**
   - Sentry
   - LogRocket
   - Browser console monitoring

## Security

1. **API Key Security:**
   - Never commit API keys to Git
   - Use environment variables
   - Rotate keys regularly

2. **HTTPS:**
   - All major platforms provide HTTPS
   - Ensure your domain uses HTTPS

3. **CORS:**
   - Configure CORS if needed
   - Most weather APIs support CORS

## Support

If you encounter issues:

1. Check the platform's documentation
2. Review the troubleshooting section
3. Check browser console for errors
4. Verify environment variables are set correctly
5. Test locally with `npm run preview` 