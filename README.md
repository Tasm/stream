# Streaming Tracker PWA

A mobile-optimized Progressive Web App for tracking TV shows and movies across all streaming services.

## Features
- ✅ Track shows across Netflix, Amazon, Peacock, YouTube, Hulu, Disney+, HBO Max, and more
- ✅ Remember Season & Episode progress
- ✅ Track watch status (Watching, Finished, Paused)
- ✅ Works offline with IndexedDB storage
- ✅ Mobile-first responsive design
- ✅ Converts to Android app with PWABuilder

## Files Included
- `streaming-tracker.html` - Main app file
- `manifest.json` - Web app manifest
- `service-worker.js` - Offline functionality

## Setup Instructions for PWABuilder

### 1. Create Your GitHub Repository
1. Create a new repository on GitHub
2. Upload these files to your repository

### 2. Create Icons Folder
You need to create app icons in the following sizes. You can use a free tool like:
- **Favicon.io** (https://favicon.io/)
- **RealFaviconGenerator** (https://realfavicongenerator.net/)
- **PWABuilder Image Generator** (https://www.pwabuilder.com/imageGenerator)

Create a folder called `icons` and add these files:
```
icons/
  ├── icon-72x72.png
  ├── icon-96x96.png
  ├── icon-128x128.png
  ├── icon-144x144.png
  ├── icon-152x152.png
  ├── icon-192x192.png
  ├── icon-384x384.png
  ├── icon-512x512.png
  ├── icon-maskable-192x192.png
  └── icon-maskable-512x512.png
```

**Icon Design Tip:** Use a TV/streaming themed icon with the purple gradient colors (#667eea to #764ba2)

### 3. Enable GitHub Pages
1. Go to your repository Settings
2. Navigate to "Pages" in the left sidebar
3. Under "Source", select your main branch
4. Click Save
5. Your app will be live at: `https://yourusername.github.io/yourrepo/streaming-tracker.html`

### 4. Use PWABuilder
1. Go to https://www.pwabuilder.com/
2. Enter your GitHub Pages URL
3. Click "Start"
4. PWABuilder will analyze your PWA
5. Click "Package for Stores"
6. Select "Android" 
7. Download your Android package
8. Upload to Google Play Store

## File Structure
```
your-repo/
  ├── streaming-tracker.html
  ├── manifest.json
  ├── service-worker.js
  ├── icons/
  │   ├── icon-72x72.png
  │   ├── icon-96x96.png
  │   └── ... (other icon sizes)
  └── README.md
```

## How It Works

### IndexedDB Storage
All your show data is stored locally on your device using IndexedDB:
- **Database Name:** StreamingTrackerDB
- **Store Name:** shows
- **Auto-incrementing ID** for each entry
- **Persists even when app is closed**

### Data Structure
Each show entry contains:
- Service (streaming platform)
- Title (show/movie name)
- Season & Episode numbers
- Date last watched
- Status (Watching/Finished/Paused)

### Offline Functionality
The service worker caches the app files, so it works offline. Your show data is always stored locally in IndexedDB.

## Customization Options

### Change Color Scheme
Edit these values in the CSS (in streaming-tracker.html):
```css
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
```

And in manifest.json:
```json
"background_color": "#667eea",
"theme_color": "#667eea"
```

### Add More Streaming Services
In streaming-tracker.html, find the service select dropdown and add more options:
```html
<option value="YourService">Your Service Name</option>
```

### Modify Status Options
Change the status dropdown options in the HTML form section.

## Testing Locally
1. Open `streaming-tracker.html` in a web browser
2. Add some test shows
3. Close and reopen - your data will persist
4. Works in Chrome, Firefox, Safari, Edge

## Support
For PWABuilder issues: https://github.com/pwa-builder/PWABuilder
For IndexedDB reference: https://developer.mozilla.org/en-US/docs/Web/API/IndexedDB_API

## License
Free to use and modify for personal or commercial projects.
