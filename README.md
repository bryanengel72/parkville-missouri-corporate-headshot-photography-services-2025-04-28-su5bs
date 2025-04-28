# Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the 101Headshots landing page. Follow these steps carefully to make updates while preserving the page's functionality and design.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
```html
<header class="fixed w-full bg-white/95 backdrop-blur-sm shadow-sm z-50">
    <span class="text-2xl font-bold text-gray-900">101Headshots</span>
</header>
```
To update the company name:
1. Locate the `<span>` tag with class `text-2xl`
2. Replace "101Headshots" with your desired text
3. Maintain the existing classes to preserve styling

### Hero Section Text
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-extrabold text-gray-900">
    Parkville, Missouri Corporate Headshot Photography Services
</h1>
```
To modify the main headline:
1. Find the `<h1>` tag within the hero section
2. Update the text while keeping the responsive text classes:
   - `text-4xl`: Base size for mobile
   - `md:text-5xl`: Medium screens
   - `lg:text-6xl`: Large screens

### Understanding Tailwind Classes
Common classes used throughout:
- `mx-auto`: Centers content horizontally
- `px-4`: Adds horizontal padding
- `py-24`: Adds vertical padding
- `text-gray-900`: Sets text color
- `bg-white`: Sets background color
- `rounded-md`: Adds border radius

### Modifying Responsive Design
Example of responsive adjustment:
```html
<div class="grid grid-cols-1 md:grid-cols-3 gap-8">
```
This creates:
- Single column on mobile (`grid-cols-1`)
- Three columns on medium screens (`md:grid-cols-3`)
- 8 units of gap between items (`gap-8`)

## Fixing Broken Links

### Navigation Menu Links
Current navigation structure:
```html
<div class="hidden md:flex space-x-8">
    <a href="#services">Services</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update internal links:
1. Locate the `href` attribute
2. Ensure it matches the corresponding section's `id`
3. For external links, replace with full URL:
```html
<a href="https://www.yourwebsite.com">Link Text</a>
```

### Book Now Button
```html
<a href="https://www.101headshots.com" class="inline-flex items-center">
    Book Now
</a>
```
To update booking link:
1. Replace the URL in `href`
2. Test the link after updating
3. Maintain all existing classes for consistent styling

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the footer:
```html
<div class="border-t border-gray-800 mt-12 pt-8 text-center">
    <p class="text-gray-400">&copy; 2024 101Headshots. All rights reserved.</p>
    <!-- Add these lines below the copyright notice -->
    <div class="mt-4 space-x-4">
        <a href="/privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a>
        <a href="/terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a>
    </div>
</div>
```

### Creating Policy Pages
1. Create new files:
   - `privacy.html`
   - `terms.html`
2. Use consistent styling:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Privacy Policy - 101Headshots</title>
    <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="font-sans antialiased text-gray-900 bg-white">
    <!-- Copy header from index.html -->
    <!-- Add policy content here -->
    <!-- Copy footer from index.html -->
</body>
</html>
```

## Troubleshooting

Common Issues and Solutions:

1. **Broken Internal Links**
   - Verify that section `id` attributes match navigation `href` values
   - Check for typos in both the link and target section
   - Ensure sections have unique IDs

2. **Responsive Design Issues**
   - Test on multiple screen sizes
   - Verify Tailwind breakpoint classes are correct:
     - `md:` for medium screens
     - `lg:` for large screens
   - Check for missing responsive classes

3. **Style Inconsistencies**
   - Compare new elements with existing ones
   - Copy and modify existing class combinations
   - Maintain color scheme using provided Tailwind classes

Remember to:
- Test all changes in multiple browsers
- Validate links before publishing
- Back up files before making changes
- Maintain consistent spacing and indentation
- Test responsive design at various screen sizes

For additional help, refer to:
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [HTML Reference](https://developer.mozilla.org/en-US/docs/Web/HTML)