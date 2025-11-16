# Quick Setup Checklist

Follow these steps to get your Streaming Tracker app live and converted to Android!

## ✅ Step 1: Get Your Files Ready
- [x] streaming-tracker.html
- [x] manifest.json  
- [x] service-worker.js
- [x] README.md
- [ ] Create icons folder with PNG files (see ICON-GUIDE.md)

## ✅ Step 2: Create GitHub Repository
1. Go to https://github.com/new
2. Name it something like: `streaming-tracker`
3. Make it Public (required for GitHub Pages)
4. Click "Create repository"

## ✅ Step 3: Upload Files to GitHub
**Option A - Via Website:**
1. Click "uploading an existing file"
2. Drag and drop all your files
3. Commit changes

**Option B - Via Git Command Line:**
```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/yourusername/streaming-tracker.git
git push -u origin main
```

## ✅ Step 4: Enable GitHub Pages
1. Go to your repo Settings
2. Click "Pages" in left sidebar
3. Under "Source" select: main branch
4. Click Save
5. Wait 1-2 minutes
6. Your URL will be: `https://yourusername.github.io/streaming-tracker/streaming-tracker.html`

## ✅ Step 5: Generate Icons (IMPORTANT!)
1. Go to: https://www.pwabuilder.com/imageGenerator
2. Upload `icon-template.svg`
3. Download the generated icons
4. Upload to GitHub in an `icons` folder

Your file structure should look like:
```
streaming-tracker/
  ├── streaming-tracker.html
  ├── manifest.json
  ├── service-worker.js
  ├── README.md
  └── icons/
      ├── icon-72x72.png
      ├── icon-96x96.png
      ├── icon-128x128.png
      └── ... (all other sizes)
```

## ✅ Step 6: Test Your PWA
1. Open your GitHub Pages URL in Chrome on mobile
2. You should see your streaming tracker
3. Open Chrome menu > "Add to Home Screen"
4. Test that it works offline

## ✅ Step 7: Convert to Android App with PWABuilder
1. Go to: https://www.pwabuilder.com/
2. Enter your GitHub Pages URL
3. Click "Start"
4. Wait for analysis
5. Click "Package For Stores"
6. Select "Android"
7. Fill in app details:
   - Package ID: com.yourname.streamingtracker
   - App Name: My Streaming Tracker
   - Version: 1.0.0
8. Download your Android package

## ✅ Step 8: Publish to Google Play Store (Optional)
1. Create Google Play Developer account ($25 one-time fee)
2. Go to Google Play Console
3. Create new app
4. Upload the package from PWABuilder
5. Fill in store listing info
6. Submit for review

## 🎯 Quick Test Before PWABuilder

Test these on your GitHub Pages URL:
- [ ] Page loads correctly
- [ ] Can add a show
- [ ] Data persists after refresh
- [ ] Icons appear in browser tab
- [ ] Works on mobile device
- [ ] "Add to Home Screen" appears on mobile

## 🚨 Common Issues

**Icons not showing?**
- Check that icons folder path is correct
- Make sure all icon files exist
- Clear browser cache

**PWA not installable?**
- Must be served over HTTPS (GitHub Pages does this automatically)
- manifest.json must be linked in HTML
- Icons must be present

**Data not persisting?**
- Check browser console for IndexedDB errors
- Make sure you're not in incognito/private mode

**PWABuilder errors?**
- Make sure all icon sizes are present
- Check that manifest.json is valid JSON
- Verify your GitHub Pages URL is accessible

## 📱 File Size Note

The entire app is just one HTML file (~15KB) + manifest + service worker. Very lightweight!
All data is stored locally in IndexedDB, so users don't need internet after first install.

## Need Help?

- PWABuilder docs: https://docs.pwabuilder.com/
- GitHub Pages: https://docs.github.com/en/pages
- IndexedDB: https://developer.mozilla.org/en-US/docs/Web/API/IndexedDB_API

Good luck with your streaming tracker app! 🎬📺
