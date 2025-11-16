# Icon Generation Guide

I've included `icon-template.svg` - a simple TV icon with your app's purple gradient colors.

## Easy Option: Use Online Tools

### Option 1: PWABuilder Image Generator (RECOMMENDED)
1. Go to: https://www.pwabuilder.com/imageGenerator
2. Upload the `icon-template.svg` file
3. Click "Download" - it generates ALL sizes you need automatically
4. Extract the zip file
5. Copy all PNG files to an `icons` folder in your repository

### Option 2: Favicon.io
1. Go to: https://favicon.io/favicon-converter/
2. Upload the `icon-template.svg` file
3. Download the generated files
4. Rename them to match the names in manifest.json

### Option 3: RealFaviconGenerator
1. Go to: https://realfavicongenerator.net/
2. Upload the `icon-template.svg` file
3. Generate icons for all platforms
4. Download and use the PNG files

## Manual Option: Use Image Editing Software

If you have Photoshop, GIMP, or Inkscape:

1. Open `icon-template.svg`
2. Export/Save As PNG at these sizes:
   - 72x72
   - 96x96
   - 128x128
   - 144x144
   - 152x152
   - 192x192
   - 384x384
   - 512x512

3. For maskable icons (safe area for Android):
   - Create 192x192 with 20% padding on all sides
   - Create 512x512 with 20% padding on all sides

## Customize the Icon

You can edit `icon-template.svg` in:
- **Inkscape** (free): https://inkscape.org/
- **Figma** (free online): https://www.figma.com/
- **Any text editor** - it's just XML!

Ideas for customization:
- Change the gradient colors
- Add your initials
- Change the TV design
- Add streaming service logos

## Quick Test

After generating icons:
1. Create an `icons` folder in your repository
2. Put all PNG files in that folder
3. Make sure file names match those in `manifest.json`
4. Open your app in Chrome
5. Check DevTools > Application > Manifest to verify icons load

## Maskable Icons Explained

Maskable icons have extra padding so Android can safely apply different shapes (circle, square, squircle) without cutting off important content.

The "safe zone" is the center 80% of the icon. Keep your TV logo in that area for maskable versions.
