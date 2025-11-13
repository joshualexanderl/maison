# Maison - Black Pulsing Orb

A minimal, elegant single-page website featuring a pulsing black orb that serves as a clickable link.

## Description

This project displays a centered black pulsing orb on a white background with "maison" text at the bottom. The entire page pixelates in on load using the proven PixelatedImage algorithm (16 → 8 → 4 → 2 → 1 pixels). The orb features a smooth breathing animation that alternates between blurred and focused states. When clicked, it instantly redirects to https://joshualexander.com/music/releases. The minimalist aesthetic with retro pixelation effects creates a captivating visual experience.

## Features

- **Centered Design**: Orb perfectly centered on the page using flexbox
- **Full-Page Pixelation**: Entire page pixelates in on load using exact PixelatedImage algorithm
  - **Algorithm**: 16px → 8px → 4px → 2px → 1px (smooth progression)
  - **Timing**: 156ms base with 0.5x acceleration per step
  - **Canvas**: Fixed 128px width for optimal performance
  - **Total Duration**: ~442ms pixelation + 800ms fade = ~1.2s
  - Captures blurred orb and text together
  - Uses the proven algorithm from portfolio (lines 94-130)
- **Smooth Pulsing Animation**: After pixelating in, orb has 2-second breathing effect
  - Scale: 4x (large) → 1x (small)
  - Blur: 15px (soft) → 5px (sharp)
  - Uses `ease-in-out` timing for natural motion
- **Monospaced Typography**: 14px Courier New font with letter-spacing
- **Interactive**: 
  - Hover effect speeds up orb pulsing to 1 second
  - Click instantly redirects to music releases page
- **Exact Replication**: Uses identical parameters from PixelatedImage component
- **Responsive**: Works on all screen sizes
- **Clean Code**: Pure HTML/CSS/JavaScript - no dependencies

## Installation

No installation required! Simply open the `index.html` file in any modern web browser.

### Local Setup

1. Download or clone this repository
2. Open `index.html` in your web browser
3. Click the orb to navigate to the music releases page

### Web Hosting

Upload the `index.html` file to any web server or hosting platform:
- GitHub Pages
- Netlify
- Vercel
- Any static hosting service

## Usage

1. Open the page in a browser
2. Watch the entire page pixelate in from blocky to clear (16px → 1px) - total ~1.2s
3. After pixelating in, the orb starts its smooth pulsing animation
4. Click the orb to instantly redirect to https://joshualexander.com/music/releases

## Technical Details

### Orb Specifications
- **Base Size**: 20px × 20px circle
- **Color**: Pure black (#000000)
- **Animation**: Alternating scale (1x to 4x) and blur (5px to 15px)
- **Duration**: 2 seconds (normal), 1 second (hover)
- **Timing**: ease-in-out for smooth transitions

### Typography & Pixelation
- **Font**: Courier New (monospace)
- **Size**: 14px (reduced from 24px)
- **Letter Spacing**: 2px
- **Position**: 30px from bottom
- **Pixelation Algorithm**: Based on PixelatedImage component
  - **Fixed Canvas Size**: 128px width (optimal performance vs quality)
  - **Reference Canvas Pattern**: Text drawn once, then sampled
  - **Draw Method**: Draw-tiny-then-scale-up for pixel effect
  - **Image Smoothing**: Disabled across all browsers for crisp pixels
  - **Pixelate In**: 16 → 8 → 4 → 2 → 1 pixels (156ms base, 0.5x acceleration)
  - **Pixelate Out**: 1 → 2 → 4 → 8 → 16 pixels (78ms base, 2x deceleration)
  - **Total Duration**: ~292ms (pixelate in), ~1,248ms (pixelate out)

### Browser Compatibility
Works on all modern browsers:
- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Opera (latest)

## Version History

### v3.0.0 (November 13, 2025)
- **Implemented EXACT PixelatedImage algorithm** from portfolio site
- Full-page pixelation with blurred orb effect
- Exact parameters: 128px canvas, 156ms base, 0.5x acceleration
- Removed pixelate-out animation (instant redirect on click)
- Simplified interaction model
- All timing matches portfolio implementation line-by-line

### v2.2.0 (November 13, 2025)
- **Added orb pixelation on page load** - Orb now pixelates in using the same algorithm as text
- Implemented dual pixelation system (both orb and text pixelate in simultaneously)
- Orb canvas uses reference canvas pattern for efficient rendering
- Pulsing animation now only starts after pixelation completes
- Click handler moved to orb-container for better UX during pixelation
- Both elements use proven PixelatedImage algorithm with proper layering

### v2.1.0 (November 13, 2025)
- Added canvas-based pixelation animation for "maison" text
- **Pixelate In** on page load (16 → 8 → 4 → 2 → 1 pixels)
- **Pixelate Out** on click before redirect (1 → 2 → 4 → 8 → 16 pixels)
- Reduced text size from 24px to 14px
- Implemented exact algorithm from PixelatedImage component:
  - Fixed 128px canvas width for optimal performance
  - Reference canvas pattern (draw once, sample many times)
  - Draw-tiny-then-scale-up technique for pixel effect
  - Disabled image smoothing across all browsers
  - Proper timing: 156ms base with 0.5x acceleration (in), 78ms base with 2x deceleration (out)
- Click now waits for full pixelation before navigation
- Added state management and cleanup handlers

### v2.0.0 (November 13, 2025)
- **Complete rewrite** for glitch-free performance
- Implemented simplified pulsing animation (scale 1x-4x, blur 5px-15px)
- Added "maison" text at bottom in monospace font
- Removed complex multi-transform animations that caused glitching
- Based on proven animation pattern from floating-music-orb component
- Reduced base orb size from 300px to 20px for cleaner aesthetic
- Hover speeds up animation from 2s to 1s
- Pure CSS animations without conflicts

### v1.2.1 (November 13, 2025)
- Fixed animation glitching by combining pulse and float into single smooth animation
- Extended animation duration to 8 seconds for more fluid movement
- Synchronized all transform, filter, and shadow changes for seamless transitions

### v1.2.0 (November 13, 2025)
- Increased blur intensity to 25-30px for amorphous appearance
- Removed 3D sphere highlights and gradients
- Simplified to pure black blur without sphere definition
- Enhanced glow shadows for more ethereal effect

### v1.1.0 (November 13, 2025)
- Added pulsing animation (4-second cycle)
- Added floating/drifting animation (6-second cycle)
- Implemented blur effect (2-3px)
- Enhanced with layered black glow shadows
- Hover now accelerates pulsing animation
- Refined visual aesthetic for ethereal, dreamlike quality

### v1.0.0 (November 13, 2025)
- Initial release
- Black gradient orb with 3D effect
- Clickable link to Joshua Alexander's music releases
- Hover and click animations
- Fully responsive design

