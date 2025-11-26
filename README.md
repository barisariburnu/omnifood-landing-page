# Omnifood Landing Page

A modern, responsive landing page for Omnifood - a premium food delivery service. This project showcases a beautifully designed single-page website featuring smooth animations, mobile-responsive design, and an engaging user experience.

![Omnifood Landing Page](resources/img/hero-min.jpg)

## 🚀 Features

- **Responsive Design**: Fully responsive layout that works seamlessly on desktop, tablet, and mobile devices
- **Smooth Animations**: jQuery-powered scroll animations using Waypoints and Animate.css
- **Sticky Navigation**: Smart sticky navigation bar that appears on scroll
- **Modern UI/UX**: Clean, professional design with engaging visual elements
- **Grid System**: Custom grid layout for consistent spacing and alignment
- **Icon Fonts**: Ionicons integration for scalable vector icons
- **Cross-browser Compatible**: Works on all modern browsers

## 📋 Table of Contents

- [Demo](#demo)
- [Technologies Used](#technologies-used)
- [Getting Started](#getting-started)
- [Project Structure](#project-structure)
- [Customization](#customization)
- [Browser Support](#browser-support)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgments](#acknowledgments)

## 🎯 Demo

Visit the live demo: [Omnifood Landing Page](https://barisariburnu.github.io/omnifood-landing-page/)

## 🛠️ Technologies Used

### Core Technologies
- **HTML5**: Semantic markup with modern HTML5 elements
- **CSS3**: Custom styles with advanced CSS3 features (flexbox, gradients, transitions)
- **JavaScript**: jQuery for smooth interactions and animations

### Libraries & Frameworks
- **jQuery 1.11.2**: DOM manipulation and event handling
- **Ionicons**: Beautiful icon font
- **Animate.css**: CSS animation library
- **Waypoints**: Scroll-triggered animations
- **Normalize.css**: CSS reset for consistent cross-browser rendering
- **Grid.css**: Custom grid system for responsive layouts

### Fonts
- **Raleway**: Google Fonts (weights: 100, 300, 400)

## 🏁 Getting Started

### Prerequisites

No special prerequisites needed! This is a static HTML website.

### Installation

1. Clone the repository:
```bash
git clone https://github.com/barisariburnu/omnifood-landing-page.git
```

2. Navigate to the project directory:
```bash
cd omnifood-landing-page
```

3. Open `index.html` in your browser:
```bash
# On Windows
start index.html

# On macOS
open index.html

# On Linux
xdg-open index.html
```

Alternatively, you can use a local server:

**Using Python:**
```bash
# Python 3
python -m http.server 8000

# Python 2
python -m SimpleHTTPServer 8000
```

**Using Node.js (http-server):**
```bash
npx http-server
```

Then visit `http://localhost:8000` in your browser.

## 📁 Project Structure

```
omnifood-landing-page/
│
├── index.html                 # Main HTML file
├── README.md                  # Project documentation
├── LICENSE                    # GNU GPL v3.0 license
│
├── resources/                 # Project assets
│   ├── css/
│   │   ├── style.css         # Main stylesheet
│   │   └── queries.css       # Media queries for responsive design
│   │
│   ├── js/
│   │   └── script.js         # Custom JavaScript
│   │
│   ├── img/                  # Images and photos
│   │   ├── hero-min.jpg      # Hero background
│   │   ├── logo.png          # Logo files
│   │   ├── logo-white.png
│   │   └── ...               # Meal photos and city images
│   │
│   └── favicons/             # Favicon files
│       ├── favicon.ico
│       ├── apple-touch-icon.png
│       └── ...
│
└── vendors/                   # Third-party libraries
    ├── css/
    │   ├── normalize.css     # CSS reset
    │   ├── grid.css          # Grid system
    │   ├── ionicons.min.css  # Icon font
    │   └── animate.css       # Animation library
    │
    ├── fonts/                # Ionicons font files
    │
    └── js/
        └── jquery.waypoints.min.js  # Waypoints library
```

## 🎨 Customization

### Colors

The main brand color is orange (`#e67e22`). To change it:

1. Open `resources/css/style.css`
2. Find and replace all instances of `#e67e22` with your desired color
3. Also update the darker shade `#cf6d17` (used for hover effects)

### Content

1. **Hero Section**: Edit the hero text in `index.html` (lines 43-46)
2. **Features**: Modify the features section (lines 49-87)
3. **Cities**: Update city information (lines 164-234)
4. **Pricing Plans**: Customize pricing plans (lines 262-328)

### Images

Replace images in the `resources/img/` directory with your own:
- Hero background: `hero-min.jpg`
- Logo files: `logo.png`, `logo-white.png`
- Meal photos: `1.jpg` through `8.jpg`
- City photos: `lisbon-3.jpg`, `san-francisco.jpg`, `berlin.jpg`, `london.jpg`

### Typography

To change the font:

1. Choose a font from [Google Fonts](https://fonts.google.com/)
2. Update the link in `index.html` (line 15)
3. Update the `font-family` in `resources/css/style.css` (line 23)

## 🌐 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Opera (latest)
- Internet Explorer 9+ (with polyfills)

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

See [CONTRIBUTING.md](CONTRIBUTING.md) for detailed guidelines.

Quick start:
1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the GNU General Public License v3.0 - see the [LICENSE](LICENSE) file for details.

## 👏 Acknowledgments

- Original design and concept from a Udemy course on web development
- [Ionicons](https://ionicons.com/) for the beautiful icon set
- [Animate.css](https://animate.style/) for CSS animations
- [Unsplash](https://unsplash.com/) for food photography
- All contributors who helped improve this project

## 📧 Contact

Barış Arıburnu - [@barisariburnu](https://github.com/barisariburnu)

Project Link: [https://github.com/barisariburnu/omnifood-landing-page](https://github.com/barisariburnu/omnifood-landing-page)

---

⭐ If you found this project helpful, please give it a star!
