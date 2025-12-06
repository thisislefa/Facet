# Facet - Interactive Client Stories Component

A sleek, modern testimonial showcase featuring a split-layout design with smooth transitions between client stories. This component combines clean typography with interactive navigation to create an engaging client testimonial experience.

## Live Preview

[View Live Demo](https://thisislefa.github.io/Facet/) | [GitHub Repository](https://github.com/thisislefa/Facet)

## Overview

Facet is a responsive client testimonial component that showcases stories through a two-panel layout. The left panel displays client profiles with professional images, while the right panel presents testimonials, company logos, and detailed descriptions. Built with vanilla JavaScript for smooth transitions and optimal performance.

## Features

- **Split-Layout Design**: Clean separation between client profile and testimonial content
- **Animated Transitions**: Smooth fade animations between stories
- **Interactive Navigation**: Previous/Next buttons with visual feedback
- **Responsive Grid**: Adapts from 2-column desktop to single-column mobile
- **Customizable Content**: Easily update client stories, images, and company logos
- **Accessibility Ready**: Semantic HTML and ARIA labels
- **Performance Optimized**: No external dependencies, minimal JavaScript

## Installation

### Direct Usage
```html
<!-- Add to your project -->
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter+Tight:wght@300;400;500;600;700&display=swap" rel="stylesheet">
<link rel="stylesheet" href="path/to/facet.css">

<section class="cs-wrapper">
  <!-- Copy HTML structure from index.html -->
</section>

<script src="path/to/facet.js"></script>
```

### Local Setup
```bash
# Clone the repository
git clone https://github.com/thisislefa/Facet.git
cd Facet

# Open in browser
open index.html
# or serve locally
python3 -m http.server 8080
```

## Project Structure

```
Facet/
├── index.html          # Main HTML structure
├── style.css          # All styling and responsive design
├── script.js          # Interactive functionality
└── README.md          # Documentation
```

## Customization

### CSS Variables
The component uses the Inter Tight font family and a neutral color palette. Customize by modifying these core styles:

```css
:root {
  --font-family: 'Inter Tight', sans-serif;
  --color-primary: #000000;
  --color-secondary: #666666;
  --color-accent: #b0b0b0;
  --color-background: #ffffff;
  --color-surface: #f1f1f1;
  --transition-speed: 0.3s;
}
```

### Adding More Stories
Extend the `stories` array in `script.js`:

```javascript
const stories = [
  {
    name: "Client Name",
    role: "Position, Company",
    image: "https://path-to-image.jpg",
    quote: "Client testimonial quote",
    description: "Detailed description of the project and results",
    logoHTML: `<!-- SVG or HTML for company logo -->`
  },
  // Add more stories here
];
```

### Content Structure
Each story object contains:
- `name`: Client's full name
- `role`: Position and company
- `image`: URL to client portrait
- `quote`: Main testimonial quote
- `description`: Detailed case study description
- `logoHTML`: HTML/logo markup for company branding

## Responsive Design

### Breakpoints
- **Desktop (900px+)**: 2-column grid layout
- **Tablet (600-900px)**: Single column with adjusted typography
- **Mobile (<600px)**: Optimized for touch, stacked elements

### Typography Scale
- **Title**: 64px (Desktop) → 48px (Mobile)
- **Quote**: 38px → 28px
- **Description**: 17px
- **Profile Name**: 24px
- **Profile Role**: 15px

## JavaScript API

### Core Functions
```javascript
// Manual content update
updateContent(index); // Switch to specific story index

// Navigation controls
elements.prevBtn.addEventListener('click', previousStory);
elements.nextBtn.addEventListener('click', nextStory);

// Current state
currentIndex; // Currently displayed story index
stories.length; // Total number of stories
```

### Event Listeners
The component includes click handlers for navigation buttons with smooth transitions. The `fade-out` CSS class controls opacity transitions during content switching.

## Browser Support

- Chrome 60+
- Firefox 55+
- Safari 12+
- Edge 79+
- iOS Safari 12+
- Android Chrome 67+

## Performance Considerations

1. **Image Optimization**: Use compressed, properly sized images
2. **Lazy Loading**: Consider adding `loading="lazy"` to images
3. **Font Loading**: Preconnect to Google Fonts for faster loading
4. **JavaScript Optimization**: Minimal bundle size with no dependencies

## Accessibility

- Semantic HTML structure
- ARIA labels for navigation buttons
- Keyboard navigation support
- Sufficient color contrast ratios
- Focus indicators for interactive elements

## Troubleshooting

### Common Issues

1. **Images not loading**: Check image URLs and CORS settings
2. **Transitions not working**: Ensure CSS transition properties are supported
3. **Layout breaks on mobile**: Verify viewport meta tag is present
4. **JavaScript errors**: Check console for conflicts or syntax errors

### Debug Mode
Add this to your JavaScript console to inspect component state:

```javascript
console.log('Current Index:', currentIndex);
console.log('Total Stories:', stories.length);
console.log('Active Story:', stories[currentIndex]);
```

## License

MIT License - Free for personal and commercial use.

## Author

**Lefa Mofokeng**  
GitHub: [@thisislefa](https://github.com/thisislefa)

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Open a Pull Request

---

Facet provides an elegant solution for showcasing client testimonials with a focus on clean design and smooth user experience. The component is production-ready and easily customizable for various use cases.
