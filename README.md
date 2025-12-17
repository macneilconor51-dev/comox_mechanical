# Irish Mechanical - Comox Valley Plumbing Services

A professional website for Irish Mechanical, providing plumbing services in the Comox Valley, BC area.

## Website Features

- **Responsive Design**: Works seamlessly on desktop, tablet, and mobile devices
- **Service Pages**: Detailed information about plumbing services offered
- **Online Booking**: Integrated Google Calendar for scheduling estimates
- **Contact Form**: Formspree integration for customer inquiries
- **24/7 Availability**: Emergency service information prominently displayed

## Pages

- `index.html` - Homepage with hero section and company overview
- `services.html` - Detailed service offerings with images
- `book.html` - Free estimate booking with Google Calendar integration
- `contact-us.html` - Contact form and company information

## Making This Website Public with GitHub Pages

To make this website publicly accessible via GitHub Pages:

### Step 1: Enable GitHub Pages

1. Go to your repository on GitHub: https://github.com/macneilconor51-dev/comox_mechanical
2. Click on **Settings** (top right)
3. Scroll down to the **Pages** section in the left sidebar
4. Under "Source", select the branch you want to deploy (usually `main` or `master`)
5. Keep the folder as `/ (root)` since the HTML files are in the root directory
6. Click **Save**

### Step 2: Access Your Website

After enabling GitHub Pages, your website will be available at:

```
https://macneilconor51-dev.github.io/comox_mechanical/
```

It may take a few minutes for the site to become available after enabling GitHub Pages.

### Step 3: Custom Domain (Optional)

If you want to use a custom domain:

1. In the GitHub Pages settings, enter your custom domain in the "Custom domain" field
2. Configure your DNS provider to point to GitHub Pages:
   - For apex domain (example.com): Set A records to GitHub's IPs
   - For subdomain (www.example.com): Set CNAME record to `macneilconor51-dev.github.io`
3. Enable "Enforce HTTPS" for secure connections

## Repository Visibility

To make the repository itself public:

1. Go to **Settings** in your GitHub repository
2. Scroll to the bottom to the "Danger Zone" section
3. Click **Change visibility**
4. Select **Make public**
5. Confirm the action

**Note**: Making the repository public allows anyone to view the source code. GitHub Pages works with both public and private repositories.

## Local Development

To view the website locally:

1. Clone the repository
2. Open `index.html` in your web browser
3. Or use a local web server:
   ```bash
   # Python 3
   python -m http.server 8000
   
   # Then visit http://localhost:8000
   ```

## Contact Information

- **Phone**: (778) 992-6324
- **Email**: macneilconor51@gmail.com
- **Service Area**: Comox Valley, BC (Courtenay, Comox, Cumberland)

## Technologies Used

- HTML5
- CSS3 (with CSS Grid and Flexbox)
- Google Fonts (Poppins)
- Google Calendar (for booking)
- Formspree (for contact form)

## License

© 2025 Irish Mechanical | Licensed & Insured
