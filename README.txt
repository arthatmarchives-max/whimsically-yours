WHIMSICALLY YOURS — VERCEL PWA PACKAGE

Files:
- index.html: your original app, with PWA metadata and service-worker registration added
- manifest.json: install/home-screen metadata
- sw.js: basic same-origin offline caching
- icons/: app icons

DEPLOY:
1. Go to https://vercel.com/ and sign in.
2. Create a new project. The easiest reliable method is to create a GitHub repository and upload these files, then import that repository in Vercel.
3. Keep index.html, manifest.json, and sw.js at the project root. Keep the icons folder as-is.
4. For a plain static site, no build command is needed. If Vercel asks for a framework, choose Other; leave the build command blank and use the project root as the root directory.
5. Deploy. Vercel will give you a https://your-project-name.vercel.app address.

TEST:
- Open the deployed HTTPS URL once while online.
- Wait a moment, then reload.
- Test by turning off the network and reopening/reloading the app.
- On Android Chrome, use the browser menu and choose Install app or Add to Home screen.
- On iPhone, open in Safari, tap Share, then Add to Home Screen.

NOTES:
- Offline caching is for the app shell and same-origin files. Google Fonts are external, so typography may fall back to system fonts offline.
- The first visit must be online so the service worker can install and cache the app.
- The wheel, quotes, and mystery actions are embedded in the HTML, so those features work offline after the app shell is cached.
