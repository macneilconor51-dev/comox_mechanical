# How to Make This Website Public

## Quick Steps to Enable GitHub Pages

1. **Go to Repository Settings**
   - Visit: https://github.com/macneilconor51-dev/comox_mechanical
   - Click "Settings" in the top navigation

2. **Navigate to Pages**
   - Find "Pages" in the left sidebar under "Code and automation"

3. **Configure GitHub Pages**
   - **Source**: Select your branch (e.g., `main` or `copilot/make-repository-public`)
   - **Folder**: Keep it as `/ (root)`
   - Click **Save**

4. **Wait for Deployment**
   - GitHub will build and deploy your site (takes 1-2 minutes)
   - Your site will be available at: `https://macneilconor51-dev.github.io/comox_mechanical/`

5. **Verify Your Website**
   - Click the link to view your live website
   - Test all pages and features

## What Was Changed

✅ Moved all website files from "Comox Mechanical Website" folder to the root directory  
✅ All HTML files are now in the root (required for GitHub Pages)  
✅ Images are in the `Images/` subdirectory with correct references  
✅ Created README.md with full documentation  
✅ Added .gitignore to prevent unwanted files  

## File Structure

```
/
├── index.html          (Homepage)
├── services.html       (Services page)
├── book.html          (Booking page)
├── contact-us.html    (Contact page)
├── Irish-mechanical.png (Logo)
├── logo.png           (Alternative logo)
├── Images/
│   ├── emergency-service.jpeg
│   ├── infloor-heat.jpeg
│   ├── logo-crop.png
│   ├── logo.png
│   ├── new-fixtures.jpeg
│   ├── new_construction.jpeg
│   ├── reno.jpeg
│   └── tankless-water-heater.jpeg
├── README.md
└── .gitignore
```

## Making the Repository Public (Optional)

If you also want to make the repository source code public:

1. Go to **Settings**
2. Scroll to the bottom "Danger Zone"
3. Click **Change visibility** → **Make public**
4. Type the repository name to confirm

**Note**: GitHub Pages works with both public and private repositories, so this step is optional.

## Troubleshooting

- **Site not loading?** Wait a few minutes and refresh
- **Images not showing?** Check the GitHub Actions tab for build status
- **404 errors?** Ensure the branch name in Pages settings is correct

## Need Help?

Contact: macneilconor51@gmail.com
