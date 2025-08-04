# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a GitHub Pages portfolio website for Alexey Primechaev, showcasing iOS apps and personal information. The site is hosted at `alexeyprimechaev.github.io` and uses a static HTML/CSS/JavaScript structure without any build tools or frameworks.

## Architecture

- **Main Portfolio Page**: `index.html` - Interactive grid of app cards with hover effects and video previews
- **App Detail Pages**: Each app has its own subdirectory (`samokat/`, `2006CAM/`, `bigbucks/`, `shoot/`, `juu/`) containing:
  - `index.html` - App detail page with video and image showcase
  - `Image1.png` through `ImageN.png` - App screenshots
  - `icon.png` and `icon_small.png` - App icons
  - `appstore.svg` - App Store badge
  - `video.mp4` - App preview video
- **Static Assets**: `cv.pdf`, `CNAME` file for custom domain

## Key Features

### Main Portfolio (`index.html`)
- Interactive app cards with random rotation effects
- Video preview on hover with image cycling
- Long-press functionality for 2x video speed
- Responsive design for mobile and desktop
- Random visual variations (rotations) applied via JavaScript

### App Detail Pages
- Full-screen video showcase
- Image gallery with responsive layout
- Desktop: split-screen with fixed text overlay on left, scrollable images on right
- Mobile: vertical layout with video at top, info in middle, images below
- Random rotation effects for visual interest

## Development Guidelines

### File Structure
- Keep the flat structure for app directories
- Use consistent naming: `ImageN.png` (where N is sequential number)
- Video files should be named `video.mp4`
- Icons should be `icon.png` (large) and `icon_small.png` (small)

### Styling Conventions
- Black background (`#000`) throughout
- System fonts: `-apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif`
- White text with occasional opacity variations
- Responsive breakpoint at 768px
- Random rotation effects using CSS custom properties (`--rotation-var`)

### JavaScript Patterns
- Random rotation generation: `Math.random() * range - offset`
- Video controls: autoplay on hover, pause on leave
- Touch/mouse event handling for mobile compatibility
- Use `dataset` attributes for storing state (current image, max images, etc.)

## Deployment

This is a GitHub Pages site that deploys automatically from the `master` branch. No build process required - all files are served statically.

## Common Tasks

### Adding a New App
1. Create new directory with app name
2. Add required files: `index.html`, images, icons, video, `appstore.svg`
3. Update main `index.html` to include new app card
4. Follow existing HTML structure and CSS patterns

### Updating App Content
- Replace images in app directory (maintain naming convention)
- Update video file
- Modify app-specific `index.html` for text changes
- Update image count in `data-max-images` attribute if needed