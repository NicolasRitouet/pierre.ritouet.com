# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a memorial website for Pierre Ritouet (1948-2025), an architect. The site is a static HTML memorial with a single-page tribute format containing biography, testimonials, photo gallery, and acknowledgments.

**Key Context**: The main `index.html` currently contains a redirect to an external memorial site (libramemoria.com), but `test.html` contains the full memorial site implementation. This suggests the project may be in transition or testing phase.

## Architecture

### Core Structure
- **Static HTML Site**: Single-page application with no framework dependencies
- **Vanilla JavaScript**: All interactivity handled with plain JavaScript
- **CSS-in-HTML**: All styling embedded in `<style>` tags within the HTML
- **Asset Organization**: 
  - `images/` - 54+ personal photos organized chronologically
  - `temoignages/` - 57 testimonial images as PNG files
  - Root-level HTML files for different versions

### Key Components
- **Photo Gallery**: Interactive slideshow with modal viewer and navigation
- **Testimonials System**: Dual approach with image thumbnails and embedded text
- **Responsive Design**: Mobile-first approach with CSS Grid and Flexbox
- **Memorial Sections**: Biography, testimonials, photo gallery, acknowledgments

## Development Commands

### Development Server
```bash
npm run dev          # Python HTTP server on port 8000
npm run dev-alt      # Alternative PHP server on port 8000  
npm run start        # Alias for npm run dev
npm run preview      # Opens browser + starts server
```

### Build & Validation
```bash
npm run build        # Displays ready message (no actual build process)
npm run validate     # HTML validation using htmlhint
npm run help         # Shows available commands
```

### Deployment
```bash
npm run deploy-github    # Git add, commit, and push to main
npm run deploy-ftp       # Shows FTP deployment instructions
```

### Maintenance
```bash
npm run backup       # Creates timestamped tar.gz backup
npm run clean        # Removes backup files
```

## File Structure

```
├── index.html           # Main file (currently redirects to external site)
├── test.html           # Full memorial site implementation
├── package.json        # NPM scripts and dependencies
├── images/            # Personal photos (54+ files)
├── temoignages/       # Testimonial images (57 PNG files)
├── .htmlhintrc        # HTML validation configuration
└── robots.txt         # SEO directives
```

## Development Notes

### Current State
- The project appears to be in transition - `index.html` redirects externally while `test.html` contains the full memorial site
- No build process or bundling - direct HTML/CSS/JS development
- All code is self-contained within `test.html` (1300+ lines)

### Deployment Options
- GitHub Pages (current setup)
- Any static hosting service (Netlify, Vercel)
- Traditional web server (Apache/Nginx)

### Content Management
- Photos are referenced directly by filename
- Testimonials exist as both image files and embedded JavaScript text
- All memorial content is hardcoded in the HTML

### Technical Considerations
- No external dependencies beyond development tools
- HTMLHint configured for validation
- Mobile-responsive design implemented
- Accessibility features like alt text and semantic HTML

## Memorial Site Features

### Interactive Elements
- Photo slideshow with auto-advance
- Modal image viewer with keyboard navigation
- Expandable testimonial sections
- Smooth scrolling navigation

### Content Sections
1. **Hero Section**: Main photo, dates, and quote
2. **Biography**: Life story told by children
3. **Digital Guestbook**: Testimonial image previews
4. **Testimonials**: Detailed messages from family/friends
5. **Photo Gallery**: 54+ personal photos with captions
6. **Acknowledgments**: Thanks to caregivers and medical staff

This memorial site represents a personal family project with a focus on preserving memories and sharing the story of Pierre Ritouet's life and architectural career.