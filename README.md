# Best Sellers Product Section

A responsive, Shopify-style product showcase section featuring a "Best Sellers" grid with interactive hover effects and mobile-friendly toggle functionality.

## Features

- **Responsive Design**
  - Mobile (< 640px): 2-column grid layout with "Show More" toggle
  - Desktop (≥ 640px): Horizontal scrolling row layout
  - Custom styled scrollbar for desktop

- **Product Cards**
  - Image hover effects (secondary image fades in on hover)
  - Product badges ("BEST SELLER" and "SALE 15%")
  - Star ratings and review counts
  - Product titles and pricing

- **Interactive Elements**
  - Mobile "Show More/Show Less" button (shows first 4 cards by default)
  - Smooth transitions and hover states
  - Responsive resize handling

- **Accessibility**
  - Semantic HTML structure
  - ARIA attributes for interactive elements
  - Proper alt text for images

## Getting Started

### Prerequisites

No build tools or dependencies required! This project uses:
- Tailwind CSS via CDN
- Vanilla JavaScript
- Plain HTML

### Installation

1. Clone or download this repository
2. Open `index.html` in a web browser
3. That's it! No build step needed.

### Usage

Simply open `index.html` in any modern web browser. The page will automatically:
- Display products in a 2-column grid on mobile devices
- Display products in a horizontal scrollable row on desktop
- Show the first 4 products on mobile with a "Show More" button to reveal the rest

## Project Structure

```
Shopify-design-assignment/
├── index.html          # Main HTML file with all styles and scripts
└── README.md          # This file
```

## Technical Details

### Layout Strategy

- **Mobile**: CSS Grid with 2 columns, first 4 cards visible by default
- **Desktop**: Flexbox with horizontal overflow scrolling
- Breakpoint: 640px (Tailwind's `sm:` breakpoint)

### Technologies Used

- **HTML5**: Semantic markup
- **Tailwind CSS**: Utility-first CSS framework (via CDN)
- **Vanilla JavaScript**: No frameworks, pure JS for interactivity

### Browser Support

Works in all modern browsers that support:
- CSS Grid
- Flexbox
- CSS Custom Properties
- ES6 JavaScript

## Customization

### Adding More Products

To add more product cards, simply duplicate the card structure:

```html
<article class="product-card sm:w-[280px] sm:flex-shrink-0">
  <div class="relative group rounded-xl overflow-hidden">
    <!-- Badge (optional) -->
    <span class="absolute top-3 left-3 bg-white text-xs font-semibold px-2 py-1 rounded-xl">
      BEST SELLER
    </span>
    <!-- Main image -->
    <img src="..." alt="Product Name" class="..." />
    <!-- Hover image -->
    <img src="..." alt="" class="..." />
  </div>
  <h3 class="mt-3 text-sm font-medium">Product Name</h3>
  <p class="text-xs text-gray-500">★★★★☆ · 1,234 Reviews</p>
  <p class="mt-1 text-sm font-semibold">$104.95</p>
</article>
```

### Styling

The project uses Tailwind CSS utility classes. To customize:
- Modify Tailwind classes directly in the HTML
- Add custom CSS in the `<style>` tag in the `<head>`
- Replace Tailwind CDN with a custom build if needed

### JavaScript Behavior

The mobile toggle functionality:
- Shows first 4 cards by default on mobile
- Toggles visibility of remaining cards
- Automatically adjusts on window resize
- Updates button text and ARIA attributes

## Shopify Integration

This code is designed to be Shopify/Liquid template-friendly:
- Explicit HTML repetition (no loops required)
- Semantic structure that works with Shopify's product object
- Easy to convert to Liquid template syntax

## Notes

- Images are loaded from Unsplash (placeholder images)
- Product data is hardcoded for demonstration purposes
- In a production Shopify theme, you would replace static data with Liquid variables
- The "Shop All Best Sellers" link currently points to `#` - update with your actual collection URL

## License

This project is provided as-is for demonstration purposes.

