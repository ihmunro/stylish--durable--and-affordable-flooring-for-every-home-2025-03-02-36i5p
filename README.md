# Calgary Premier Flooring Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Calgary Premier Flooring landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name:**
```html
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-blue-600 to-indigo-600 bg-clip-text text-transparent">
    Calgary Premier Flooring  <!-- Edit this text -->
</a>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors">Features</a>
    <!-- Edit menu item text here -->
</div>
```

### Hero Section
Update the main headline and subheading:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-gray-900 to-gray-700 bg-clip-text text-transparent">
    Stylish, Durable, and Affordable Flooring for Every Home  <!-- Edit headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Transform your space with premium flooring solutions...  <!-- Edit subheading -->
</p>
```

### Tailwind CSS Class Guide
- Text sizes: `text-sm`, `text-base`, `text-lg`, `text-xl`, `text-2xl`, etc.
- Colors: `text-gray-600`, `bg-blue-600`, etc.
- Spacing: `px-4` (padding left/right), `py-4` (padding top/bottom), `m-4` (margin)
- Responsive classes: `md:text-2xl` (applies at medium screens and up)

## Fixing Broken Links

### Current Link Inventory
1. Navigation Menu Links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

2. Call-to-Action Links:
```html
<a href="https://calgarypremierflooring.com" class="...">
    Get Started
</a>
```

### Updating Links
1. Internal Links (sections on same page):
   - Keep the `#` symbol
   - Match the `id` of the target section
   - Example: `<a href="#features">` links to `<section id="features">`

2. External Links:
```html
<!-- Replace with your actual URL -->
<a href="https://calgarypremierflooring.com" class="...">
    Get Started
</a>
```

## Linking Privacy and Terms Pages

### Footer Link Updates
Locate this section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors">Terms of Service</a></li>
    </ul>
</div>
```

Replace the `#` with proper links:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors">Terms of Service</a></li>
```

### Creating Policy Pages
1. Create new files:
   - `privacy.html`
   - `terms.html`

2. Use consistent styling:
```html
<!-- privacy.html or terms.html -->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Privacy Policy | Calgary Premier Flooring</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
</head>
<body class="font-['Inter'] antialiased bg-white text-gray-900">
    <!-- Copy header from index.html -->
    <!-- Add policy content here -->
    <!-- Copy footer from index.html -->
</body>
</html>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Verify that section `id` attributes match href values
   - Check for typos in both the link and section ID
   - Example: `<a href="#features">` must match `<section id="features">`

2. **Responsive Design Issues**
   - Check mobile view using browser dev tools
   - Ensure responsive classes are properly ordered (sm, md, lg)
   - Example: `class="text-base md:text-lg lg:text-xl"`

3. **Tailwind Classes Not Working**
   - Verify CDN link is working
   - Check for typos in class names
   - Use official Tailwind documentation to verify class names

4. **Images Not Loading**
   - Verify file paths are correct
   - Check image file names and extensions
   - Ensure images are in the correct directory

Remember to test all changes across different devices and browsers to ensure consistency.