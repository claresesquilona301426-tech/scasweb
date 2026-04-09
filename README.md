# SCAS Admissions System

A production-ready, responsive web application for Sumulong College of Arts & Sciences (SCAS) that transforms their admissions process with modern UI/UX principles, micro-interactions, and data-driven design patterns.

## Features

### Core Functionality
- **Homepage**: Hero section with parallax effects, feature cards with counters, and interactive program showcase
- **Multi-Step Admissions Portal**: 4-step application wizard with real-time validation and file upload
- **AI Inquiry Chat**: Persistent chat widget with prebuilt responses and typing animations
- **Admin Dashboard**: Executive view with interactive charts, activity monitoring, and quick actions

### Technical Highlights
- **Responsive Design**: Mobile-first approach with breakpoints for all devices
- **Advanced Animations**: GSAP-powered scroll animations and micro-interactions
- **Accessibility**: WCAG 2.1 AA compliant with keyboard navigation and screen reader support
- **Performance**: Optimized for 60fps animations and fast loading
- **Modern Architecture**: Component-based CSS with design system and JavaScript modules

## Tech Stack

- **Frontend**: HTML5, CSS3 (Flex/Grid), Vanilla JavaScript (ES6+)
- **Animations**: GSAP 3.12.2 with ScrollTrigger
- **Charts**: Chart.js for admin dashboard analytics
- **Typography**: Google Fonts (Poppins)
- **Icons**: Inline SVG icons for scalability

## Project Structure

```
scas/
|_ css/
|  |_ design-system.css     # Design tokens and base styles
|  |_ components.css        # Component styles
|  |_ animations.css        # Animation definitions
|  |_ responsive.css        # Responsive breakpoints
|  |_ admissions.css        # Admissions portal styles
|  |_ admin.css             # Admin dashboard styles
|_ js/
|  |_ animations.js         # GSAP animation system
|  |_ navigation.js         # Responsive navigation
|  |_ program-filters.js    # Program filtering system
|  |_ chat-widget.js        # AI chat interface
|  |_ multi-step-form.js    # Admissions form wizard
|  |_ file-upload.js        # File upload with drag & drop
|  |_ number-counters.js    # Animated number counters
|  |_ admin-charts.js       # Dashboard charts
|_ index.html              # Homepage
|_ admissions.html         # Admissions portal
|_ admin.html              # Admin dashboard
|_ assets/                 # Images and assets
|_ README.md               # This file
```

## Design System

### Color Palette
- **Primary**: #1E3A8A (Navy - Trust)
- **Secondary**: #F59E0B (Gold - Prestige)
- **Success**: #10B981
- **Error**: #EF4444
- **Warning**: #F59E0B
- **Neutral**: F8FAFC, E2E8F0, 64748B

### Typography Scale
- **H1**: 3.75rem (60px) - Bold
- **H2**: 3rem (48px) - Bold
- **H3**: 2.25rem (36px)
- **H4**: 1.875rem (30px)
- **Body**: 1rem (16px)
- **Small**: 0.875rem (14px)

### Spacing System (8pt Grid)
- xs: 0.5rem | s: 1rem | m: 1.5rem | l: 2rem | xl: 3rem | xxl: 4rem

## Responsive Breakpoints

- **Mobile**: 320px - 768px
- **Tablet**: 768px - 1024px
- **Desktop**: 1024px - 1440px
- **Large**: 1440px+

## Getting Started

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge)
- Local web server (XAMPP, WAMP, MAMP, or Live Server)

### Installation

1. Clone or download the project files
2. Place in your web server directory (e.g., `htdocs/scas`)
3. Start your local web server
4. Navigate to `http://localhost/scas`

### File Structure Setup

Create the following directory structure:

```
scas/
|_ css/
|_ js/
|_ assets/
|   |_ logo.svg
|   |_ hero-bg.jpg
|   |_ program-*.jpg
|   |_ pattern.svg
```

## Pages Overview

### Homepage (`index.html`)
- **Hero Section**: Full viewport with parallax background and CTA buttons
- **Feature Cards**: 4-column grid with animated counters and hover effects
- **Program Showcase**: Filterable grid with smooth transitions
- **AI Chat Widget**: Persistent floating chat interface

### Admissions Portal (`admissions.html`)
- **Multi-Step Form**: 4-step wizard with progress indicator
- **Real-time Validation**: Instant feedback with visual indicators
- **File Upload**: Drag & drop support with progress tracking
- **Success Modal**: Confirmation with reference number

### Admin Dashboard (`admin.html`)
- **Executive Stats**: Key metrics with trend indicators
- **Interactive Charts**: Applications by month and program popularity
- **Activity Feed**: Recent admissions and inquiry activities
- **Quick Actions**: Common admin tasks

## JavaScript Modules

### Animation System (`animations.js`)
- GSAP-powered scroll animations
- Intersection Observer for performance
- Micro-interactions and hover effects
- Parallax scrolling effects

### Navigation System (`navigation.js`)
- Responsive mobile menu
- Smooth scrolling
- Active state management
- Keyboard navigation

### Chat Widget (`chat-widget.js`)
- AI-powered responses
- Typing indicators
- Message history
- Quick reply buttons

### Multi-Step Form (`multi-step-form.js`)
- Form validation
- Step transitions
- Progress tracking
- Data persistence

## Performance Optimizations

- **Lazy Loading**: Images and components load as needed
- **GPU Acceleration**: Hardware-accelerated animations
- **Optimized Animations**: 60fps target with reduced motion support
- **Efficient CSS**: Minimal reflows and repaints
- **Compressed Assets**: Production-ready minification

## Accessibility Features

- **Keyboard Navigation**: Full keyboard accessibility
- **Screen Reader Support**: ARIA labels and live regions
- **High Contrast Mode**: Enhanced visibility support
- **Reduced Motion**: Respects user preferences
- **Focus Management**: Logical focus flow
- **Touch Targets**: Minimum 44px touch targets

## Browser Support

- **Chrome**: 90+
- **Firefox**: 88+
- **Safari**: 14+
- **Edge**: 90+

## Customization

### Adding New Programs
```javascript
// In program-filters.js
this.programOptions.college.push({
  value: 'new-program',
  text: 'New Program Name'
});
```

### Updating Colors
```css
/* In design-system.css */
:root {
  --color-primary: #YOUR_COLOR;
  --color-secondary: #YOUR_COLOR;
}
```

### Adding New Chart Types
```javascript
// In admin-charts.js
window.adminChartsSystem.addChart('#newChart', 'line', data, options);
```

## API Integration

The system is designed to easily integrate with backend APIs:

```javascript
// Example API integration
const submitApplication = async (formData) => {
  try {
    const response = await fetch('/api/applications', {
      method: 'POST',
      headers: { 'Content-Type': 'application/json' },
      body: JSON.stringify(formData)
    });
    return await response.json();
  } catch (error) {
    console.error('Submission failed:', error);
  }
};
```

## Deployment

### Production Checklist
- [ ] Minify CSS and JavaScript files
- [ ] Optimize images (WebP format recommended)
- [ ] Enable gzip compression
- [ ] Set up SSL certificate
- [ ] Configure CDN for static assets
- [ ] Test with Lighthouse (target: 95+)

### Environment Variables
```javascript
const config = {
  apiUrl: process.env.API_URL || '/api',
  environment: process.env.NODE_ENV || 'development'
};
```

## Contributing

1. Follow the existing code style
2. Test on multiple devices and browsers
3. Ensure accessibility compliance
4. Document new features
5. Update README as needed

## License

This project is proprietary to Sumulong College of Arts & Sciences.

## Support

For technical support or questions:
- Email: webmaster@scas.edu.ph
- Phone: (02) 1234-5678

---

**SCAS Admissions System** - Transforming education through technology
