# Classy Weather

Small practice project built to learn React class components and consuming a public weather API (Open-Meteo). The app searches for a location, fetches geocoding results and a daily weather forecast, and renders a simple 5-day forecast.

This repository was created as a class exercise — minimal, intentionally simple, and aimed at showing how to work with React class components, state, and effects via async calls.

## Features

- Search for a location (geocoding via Open-Meteo)
- Display location name and country flag
- Show daily weather icons and min/max temperatures

## Tech

- React (Create React App)
- JavaScript (ES6+)
- CSS

## Run locally

Requires Node.js (14+ recommended) and npm.

Open a PowerShell terminal in the project root and run:

```powershell
npm install
npm start
```

The app runs at http://localhost:3000 by default.

## Build

Create a production build with:

```powershell
npm run build
```

The optimized output will be in the `build/` folder (this is what you deploy to static hosts such as Vercel).

## Push to GitHub (PowerShell)

If this repo isn't already a git repo, initialize it and push to GitHub:

```powershell
git init
git add .
git commit -m "initial: classy-weather practice app"
# replace <your-repo-url> with the HTTPS or SSH URL from GitHub
git remote add origin <your-repo-url>
git branch -M main
git push -u origin main
```

If the repository already exists and you only need to push a new branch:

```powershell
git checkout -b feature/your-branch
git add .
git commit -m "feature: your message"
git push -u origin feature/your-branch
```

## Deploy to Vercel

Two common ways to deploy:

1) Using the Vercel GitHub integration (recommended)

- Push your repository to GitHub.
- Go to https://vercel.com, sign in, and import your GitHub repository.
- Vercel will detect Create React App and use `npm run build`. Ensure the build command is `npm run build` and the output directory is `build` (these are the defaults).

2) Using the Vercel CLI

Install and deploy via CLI:

```powershell
npm i -g vercel
vercel login
cd "d:\projects\jonas projects\09-classy-weather"
vercel --prod
```

Vercel will run the build and deploy the `build/` output.

### Notes

- No special environment variables are required for the provided Open-Meteo usage.
- If you want platform-consistent emoji rendering for flags, the project includes a `.flag` CSS class that forces an emoji-capable font; Vercel deployment will serve the same CSS.

## vercel.json (optional)

This repo includes a `vercel.json` to explicitly tell Vercel to use the static-build with the `build` directory and route all requests to `index.html` (useful for single-page apps):

```json
{
  "builds": [
    { "src": "package.json", "use": "@vercel/static-build", "config": { "distDir": "build" } }
  ],
  "routes": [
    { "src": "/(.*)", "dest": "/index.html" }
  ]
}
```

## License

This is a small practice repo — use it however you like.
# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can't go back!**

If you aren't satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you're on your own.

You don't have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn't feel obligated to use this feature. However we understand that this tool wouldn't be useful if you couldn't customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

### Analyzing the Bundle Size

This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `npm run build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)
