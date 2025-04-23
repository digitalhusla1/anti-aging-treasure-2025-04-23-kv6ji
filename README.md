# Anti-Aging Landing Page Maintenance Guide

This guide will help you maintain and customize the Anti-Aging Treasure landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains your brand name and navigation menu. To update:

1. **Brand Name:**
```html
<!-- Find this line in the header section -->
<a href="/" class="text-2xl font-bold text-gray-800">Anti-Aging</a>
```
- Replace "Anti-Aging" with your brand name
- Adjust text size using `text-2xl` (can be `text-xl` for smaller or `text-3xl` for larger)

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition duration-300">Features</a>
    <!-- Add or modify menu items here -->
</div>
```
- Change text by modifying the content between `<a>` tags
- `space-x-8` controls spacing between items (increase/decrease number for more/less space)

### Hero Section
```html
<div class="max-w-4xl mx-auto text-center text-white">
    <h1 class="text-4xl md:text-6xl font-bold mb-6 leading-tight">Anti-Aging Treasure</h1>
    <p class="text-xl md:text-2xl mb-8">20 years younger, no fine lines</p>
</div>
```
- Update heading and subheading text
- `md:text-6xl` means text is larger on desktop (modify number for size adjustment)
- `mb-6` controls bottom margin (increase/decrease number for more/less space)

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white rounded-xl p-8 shadow-lg hover:shadow-xl transition duration-300 transform hover:scale-105">
    <div class="text-blue-600 mb-4">
        <i class="fas fa-star text-4xl"></i>
    </div>
    <h3 class="text-xl font-bold mb-4">Anti-Aging Serum</h3>
    <p class="text-gray-600">Advanced formula that penetrates deep into your skin</p>
</div>
```
- Change icon by replacing `fa-star` with any [Font Awesome](https://fontawesome.com/icons) icon class
- Update heading and description text
- `hover:scale-105` controls hover animation (increase/decrease number for more/less effect)

## Fixing Broken Links

### Navigation Links
Current links in navigation:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="airtm.me/sbiz100">Buy Now</a>
```

To update:
1. Internal links (starting with #) should match section IDs in your HTML
2. External links (like "Buy Now") need complete URLs:
```html
<!-- Change this -->
<a href="airtm.me/sbiz100">Buy Now</a>
<!-- To this -->
<a href="https://airtm.me/sbiz100">Buy Now</a>
```

### Footer Links
```html
<ul class="space-y-2">
    <li><a href="#" class="hover:text-blue-400 transition duration-300">About Us</a></li>
    <li><a href="#" class="hover:text-blue-400 transition duration-300">Shipping Policy</a></li>
    <li><a href="#" class="hover:text-blue-400 transition duration-300">Returns</a></li>
</ul>
```
Replace `#` with actual page URLs:
```html
<li><a href="/about.html" class="hover:text-blue-400 transition duration-300">About Us</a></li>
```

## Linking Privacy and Terms Pages

### Adding Privacy and Terms Links
Add these links to the footer's Quick Links section:
```html
<ul class="space-y-2">
    <!-- Existing links -->
    <li><a href="/privacy.html" class="hover:text-blue-400 transition duration-300">Privacy Policy</a></li>
    <li><a href="/terms.html" class="hover:text-blue-400 transition duration-300">Terms & Conditions</a></li>
</ul>
```

### Alternative Footer Layout
For better organization, create a new column:
```html
<div>
    <h4 class="text-xl font-bold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="/privacy.html" class="hover:text-blue-400 transition duration-300">Privacy Policy</a></li>
        <li><a href="/terms.html" class="hover:text-blue-400 transition duration-300">Terms & Conditions</a></li>
    </ul>
</div>
```

## Troubleshooting

### Common Issues

1. **Broken Responsive Design**
- Check that you haven't removed `md:` prefixes from classes
- Ensure the viewport meta tag is present in the head:
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

2. **Missing Icons**
- Verify Font Awesome CSS is loaded:
```html
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
```

3. **Links Not Working**
- Check for missing `https://` in external URLs
- Verify that internal page links match exact section IDs
- Ensure file paths are correct relative to your project structure

### Need Help?
- Double-check all changes against the original HTML
- Use browser developer tools (F12) to inspect elements
- Keep a backup of the original code before making changes
- Test all links and responsive layouts after modifications

Remember to maintain consistent styling throughout the page by copying existing Tailwind CSS classes when adding new elements.