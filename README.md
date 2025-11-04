# Clickkar Raju - Business Website

A modern, responsive business website for Clickkar Raju - Professional Photography & Video Editing Services.

## Features

- **Responsive Design**: Works perfectly on desktop, tablet, and mobile devices
- **Modern UI/UX**: Beautiful gradient hero section with smooth animations
- **Portfolio Gallery**: Filterable portfolio section to showcase your work
- **Interactive Lightbox**: Click on portfolio items to view images in full-screen
- **Smooth Scrolling**: Seamless navigation between sections
- **Contact Form**: Easy-to-use contact form with email integration
- **Mobile-Friendly Navigation**: Hamburger menu for mobile devices

## Sections

1. **Hero Section**: Eye-catching introduction with business branding and call-to-action buttons
2. **Services**: Comprehensive service offerings (Product Photography, Image Editing, Video Editing, Brand Photography)
3. **About**: Business overview with statistics and achievements
4. **Portfolio**: Filterable gallery to display work samples and client projects
5. **Experience**: Timeline view of professional experience and credentials
6. **Contact**: Enhanced contact form with service selection and business information

## How to Use

### 1. Adding Your Work Samples

To add your own work samples to the portfolio section:

1. Open `index.html`
2. Find the section with class `portfolio-grid`
3. Replace the placeholder images with your own:

```html
<div class="portfolio-item" data-category="photography">
    <div class="portfolio-image">
        <img src="path/to/your/image.jpg" alt="Description">
        <div class="portfolio-overlay">
            <h4>Your Project Title</h4>
            <p>Project description</p>
            <button class="view-btn" onclick="openLightbox(this)">View</button>
        </div>
    </div>
</div>
```

4. Update the `data-category` attribute to match the filter:
   - `photography` - for photography work
   - `editing` - for image editing work
   - `video` - for video editing work

### 2. Customizing Colors

Edit the CSS variables in `style.css`:

```css
:root {
    --primary-color: #2c3e50;
    --secondary-color: #3498db;
    --accent-color: #e74c3c;
    /* ... other colors */
}
```

### 3. Updating Contact Information

Update the contact section in `index.html` with your current details.

### 4. Adding Social Media Links

In the footer section, update the social media links:

```html
<a href="your-instagram-url" aria-label="Instagram"><i class="fab fa-instagram"></i></a>
<a href="your-linkedin-url" aria-label="LinkedIn"><i class="fab fa-linkedin"></i></a>
<a href="your-behance-url" aria-label="Behance"><i class="fab fa-behance"></i></a>
```

## Deployment

### Option 1: GitHub Pages
1. Create a GitHub repository
2. Upload all files
3. Go to Settings > Pages
4. Select the main branch and save

### Option 2: Netlify
1. Drag and drop your project folder to Netlify
2. Your site will be live instantly

### Option 3: Vercel
1. Install Vercel CLI: `npm i -g vercel`
2. Run `vercel` in your project directory
3. Follow the prompts

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## Files Structure

```
portfolio/
├── index.html      # Main HTML file
├── style.css       # Stylesheet
├── script.js       # JavaScript functionality
└── README.md       # This file
```

## Notes

- The portfolio images currently use placeholder images from Unsplash. Replace them with your actual work samples.
- The contact form uses a mailto link by default. For production, consider integrating with a service like Formspree or EmailJS.
- All images should be optimized for web (use tools like TinyPNG or ImageOptim).

## License

This portfolio template is free to use and modify for personal and commercial projects.

---

**Created for Clickkar Raju - Professional Photography & Video Editing Services**

