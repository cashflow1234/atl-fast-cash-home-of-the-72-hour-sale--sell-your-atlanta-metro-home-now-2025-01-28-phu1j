# ATL Fast Cash Landing Page - Maintenance Guide

This guide will help you maintain and customize the ATL Fast Cash landing page. Whether you're new to HTML and CSS or just getting started, follow these instructions to make updates safely and effectively.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company logo and navigation menu. To update:

```html
<!-- Logo Text -->
<div class="text-2xl font-bold text-blue-600">ATL Fast Cash</div>
```
- To change the logo text, simply replace "ATL Fast Cash"
- To modify logo size, adjust `text-2xl` to `text-xl` (smaller) or `text-3xl` (larger)

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-8">
    ATL Fast Cash Home of The 72 Hour Sale
</h1>
```
- Update the headline by changing the text between the `<h1>` tags
- The classes `text-4xl`, `md:text-5xl`, and `lg:text-6xl` control text size at different screen sizes

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white p-8 rounded-2xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <h3 class="text-xl font-semibold mb-4">Fast Closing</h3>
    <p class="text-gray-600">Close on your timeline - as quick as 72 hours</p>
</div>
```
To modify:
1. Change the heading text between `<h3>` tags
2. Update description text between `<p>` tags
3. Maintain the existing classes for consistent styling

## Managing Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Contact</a>
</div>
```

To update links:
1. Locate the `href` attribute
2. For internal links (same page sections), use `#section-name`
3. For external links, use the full URL: `https://example.com`

### Call-to-Action Links
The main form link appears multiple times:
```html
<a href="https://form.jotform.com/250276622130043" class="inline-block bg-blue-600 text-white...">
```
- Update all instances of this form link when changing the form URL
- Search for "jotform" to find all occurrences

## Adding Privacy and Terms Pages

### Step 1: Add Footer Links
Add these lines to the footer's Quick Links section:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

### Step 2: Create New Pages
1. Create `privacy.html` and `terms.html` in the same directory as `index.html`
2. Copy the header and footer from `index.html` to maintain consistent styling
3. Add your policy content between the header and footer

## Troubleshooting

Common Issues:
1. **Broken Layout**: If the layout breaks, check that you haven't removed any essential Tailwind CSS classes
2. **Missing Styles**: Ensure the Tailwind CDN link remains in the `<head>` section:
```html
<script src="https://cdn.tailwindcss.com"></script>
```
3. **Non-Working Links**: Verify that:
   - Internal links match section IDs exactly
   - External links include `https://`
   - File paths are correct for privacy/terms pages

### Need Help?
- Double-check your changes against the original code
- Use browser developer tools (F12) to inspect elements
- Maintain all existing classes when adding new elements
- Test all changes on both desktop and mobile views

Remember to always backup the original files before making changes, and test thoroughly after each modification.