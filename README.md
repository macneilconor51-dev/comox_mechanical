# Comox Mechanical Website

This is the official website for Comox Mechanical, a plumbing services company serving the Comox Valley, BC area.

## Development Instructions

### Viewing Changes in Your Browser

When working on this website in Visual Studio or any text editor, you may experience browser caching issues where your changes don't appear immediately. Here are several solutions:

#### Solution 1: Hard Refresh (Recommended)
Force your browser to reload the page and bypass the cache:
- **Windows/Linux**: Press `Ctrl + F5` or `Ctrl + Shift + R`
- **Mac**: Press `Cmd + Shift + R`

#### Solution 2: Clear Browser Cache
1. Open browser Developer Tools (`F12`)
2. Right-click on the refresh button
3. Select "Empty Cache and Hard Reload"

#### Solution 3: Use Browser Developer Tools
1. Open Developer Tools (`F12`)
2. Go to the Network tab
3. Check "Disable cache" checkbox
4. Keep Developer Tools open while developing

#### Solution 4: Use Private/Incognito Mode
Open your HTML files in a private/incognito window to avoid caching issues during development.

### Cache Control Headers

All HTML files include cache control meta tags to prevent aggressive caching:
```html
<meta http-equiv="Cache-Control" content="no-cache, no-store, must-revalidate" />
<meta http-equiv="Pragma" content="no-cache" />
<meta http-equiv="Expires" content="0" />
```

These headers tell browsers not to cache the pages, which is helpful during development. **Note:** For production deployment, you may want to adjust these settings to allow caching for better performance.

## File Structure

```
Comox Mechanical Website/
├── index.html              # Home page
├── services.html           # Services overview
├── book.html              # Booking page
├── contact-us.html        # Contact page
├── service-*.html         # Individual service pages
├── Images/                # Image assets
│   ├── logo-crop.png
│   └── ...
├── Comox-Mechanical.png   # Logo
└── ...
```

## Local Development

1. Open any HTML file in Visual Studio, VS Code, or your preferred editor
2. Make your changes
3. Save the file
4. Refresh your browser with `Ctrl + F5` (Windows/Linux) or `Cmd + Shift + R` (Mac)
5. If changes still don't appear, clear your browser cache completely

## Using Live Server (Recommended)

For the best development experience, use a live server extension:

### VS Code
1. Install the "Live Server" extension by Ritwick Dey
2. Right-click on any HTML file
3. Select "Open with Live Server"
4. The page will automatically reload when you save changes

### Visual Studio
1. Use IIS Express or the built-in web server
2. The server will serve your files and handle updates better than opening files directly

## Deployment

This is a static HTML website that can be deployed to:
- GitHub Pages
- Netlify
- Vercel
- Any static hosting service
- Traditional web hosting via FTP

Simply upload all files to your web server, maintaining the directory structure.

## Browser Support

This website supports all modern browsers:
- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Mobile browsers

## Contact

For questions or issues, contact: macneilconor51@gmail.com
