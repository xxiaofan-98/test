# Photography Portfolio Website

A modern, responsive photography portfolio website built with Express.js, Pug templates, and vanilla JavaScript. This website showcases a professional photographer's work with a clean, elegant design that puts the focus on the photography.

## 🌟 Features

### Design & User Experience
- **Modern, Clean Design**: Minimalist layout that highlights photography work
- **Fully Responsive**: Optimized for desktop, tablet, and mobile devices
- **Smooth Animations**: CSS transitions and JavaScript-powered scroll animations
- **Interactive Portfolio**: Filterable gallery with category-based sorting
- **Image Lightbox**: Click-to-expand functionality for detailed photo viewing
- **Professional Typography**: Beautiful font combinations (Inter + Playfair Display)

### Pages & Functionality
- **Homepage**: Hero section, featured work, about preview, testimonials, and call-to-action
- **Portfolio**: Filterable gallery showcasing different photography categories
- **About**: Detailed photographer biography, skills, experience, and philosophy
- **Contact**: Contact form, business information, FAQ, and social links
- **Error Pages**: Custom 404 and error pages matching the site design

### Technical Features
- **Express.js Backend**: Robust Node.js server with proper routing
- **Pug Templates**: Clean, maintainable template engine
- **Mobile Navigation**: Hamburger menu for mobile devices
- **Form Handling**: Contact form with validation
- **SEO Optimized**: Proper meta tags, semantic HTML, and structured content
- **Performance Optimized**: Lazy loading, optimized images, and efficient CSS

## 🚀 Quick Start

### Prerequisites
- Node.js (v14 or higher)
- npm or yarn

### Installation

1. **Clone or download the project**
   ```bash
   git clone <repository-url>
   cd photography-portfolio
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start the development server**
   ```bash
   npm start
   ```

4. **Open in browser**
   ```
   http://localhost:3000
   ```

## 📁 Project Structure

```
photography-portfolio/
├── public/                 # Static assets
│   ├── images/            # Photography images
│   │   └── portfolio/     # Portfolio category images
│   ├── stylesheets/       # CSS files
│   │   └── style.css      # Main stylesheet
│   └── javascripts/       # Client-side JavaScript
│       └── script.js      # Main JavaScript file
├── routes/                # Express routes
│   └── index.js          # Main routing logic
├── views/                 # Pug templates
│   ├── layout.pug        # Base layout template
│   ├── index.pug         # Homepage
│   ├── portfolio.pug     # Portfolio page
│   ├── about.pug         # About page
│   ├── contact.pug       # Contact page
│   └── error.pug         # Error page
├── app.js                # Express application setup
├── package.json          # Dependencies and scripts
└── README.md            # This file
```

## 🎨 Customization Guide

### 1. Personal Information
Update the following files with your personal information:

**views/layout.pug** - Update photographer name:
```pug
a.nav-logo(href="/") Your Name
```

**All template files** - Replace "Alex Thompson" with your name

### 2. Contact Information
**views/contact.pug** - Update contact details:
```pug
p email@yourname.com
p +1 (555) 123-4567
p Your City, State
```

**views/layout.pug** - Update footer contact info

### 3. Images
Replace placeholder images in `public/images/` with your actual photography:

- `hero-photo.jpg` - Main hero image (800x600px recommended)
- `portrait-1.jpg`, `wedding-1.jpg`, `landscape-1.jpg` - Featured work images
- `photographer.jpg` - Your professional photo
- `about-photographer.jpg` - About page image
- `client-1.jpg`, `client-2.jpg`, `client-3.jpg` - Client testimonial photos

**Portfolio images** in `public/images/portfolio/`:
- Organize by category (portraits, weddings, landscapes, events)
- Recommended size: 400x350px minimum
- Use high-quality, web-optimized images

### 4. Content Customization

**Homepage (views/index.pug)**:
- Update hero title and subtitle
- Modify about section content
- Replace testimonials with real client feedback
- Update statistics in the stats section

**About Page (views/about.pug)**:
- Write your personal photography journey
- Update experience and skills sections
- Modify the timeline with your actual milestones
- Customize photography philosophy

**Portfolio Page (views/portfolio.pug)**:
- Add/remove portfolio categories
- Update project descriptions
- Ensure `data-category` attributes match filter buttons

### 5. Styling Customization

**Color Scheme** (public/stylesheets/style.css):
```css
/* Primary gradient colors */
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);

/* Update these hex values to match your brand */
--primary-color: #667eea;
--secondary-color: #764ba2;
```

**Typography**:
- Headings: Playfair Display (serif)
- Body text: Inter (sans-serif)
- Update font imports in layout.pug if needed

### 6. Social Media Links
Update social media URLs in:
- `views/layout.pug` (footer)
- `views/contact.pug` (contact section)

```pug
a(href="https://instagram.com/yourusername" aria-label="Instagram")
```

## 🔧 Advanced Customization

### Adding New Portfolio Categories

1. **Update filter buttons** in `views/portfolio.pug`:
```pug
button.filter-btn(data-filter="newcategory") New Category
```

2. **Add portfolio items** with matching data-category:
```pug
.portfolio-item(data-category="newcategory")
```

3. **CSS styling** is automatic - no changes needed

### Contact Form Integration

The contact form currently logs submissions to console. To integrate with a real backend:

1. **Update the POST route** in `routes/index.js`
2. **Add email service** (SendGrid, Mailgun, etc.)
3. **Add database storage** if needed

Example with SendGrid:
```javascript
router.post('/contact', async (req, res) => {
  try {
    await sendEmail(req.body);
    res.redirect('/contact?success=true');
  } catch (error) {
    res.redirect('/contact?error=true');
  }
});
```

### SEO Optimization

1. **Update meta descriptions** in each template
2. **Add structured data** for better search engine understanding
3. **Optimize image alt tags** with descriptive text
4. **Add sitemap.xml** and robots.txt

## 📱 Mobile Optimization

The website is fully responsive with:
- Mobile-first CSS approach
- Touch-friendly navigation
- Optimized image sizes
- Readable typography on all devices

## 🌐 Deployment

### Deployment Options

1. **Heroku**:
   ```bash
   heroku create your-portfolio-name
   git push heroku main
   ```

2. **Netlify**: Deploy from GitHub repository

3. **DigitalOcean**: Use App Platform for easy deployment

4. **Traditional hosting**: Upload files to web server

### Environment Configuration

Create `.env` file for production settings:
```
NODE_ENV=production
PORT=3000
EMAIL_SERVICE_API_KEY=your_key_here
```

## 🔍 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- iOS Safari (latest)
- Chrome Mobile (latest)

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📞 Support

If you need help customizing this template or have questions, please create an issue in the repository.

---

**Built with ❤️ for photographers who want to showcase their work beautifully online.**