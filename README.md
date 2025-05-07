# Viral Deals Landing Page - Maintenance Guide

This guide will help you maintain and customize the Viral Deals landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions to make common updates.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the site logo and navigation menu. To modify:

```html
<!-- Logo Text (Line 20) -->
<div class="text-2xl font-bold bg-gradient-to-r from-purple-600 to-pink-600 bg-clip-text text-transparent">
    Viral Deals  <!-- Edit this text to change the logo -->
</div>

<!-- Navigation Items (Lines 25-28) -->
<div class="hidden lg:flex space-x-8">
    <a href="#deals">Deals</a>  <!-- Edit these text labels -->
    <a href="#voordelen">Voordelen</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

### Hero Section
The main headline and call-to-action section:

```html
<!-- Main Headline (Lines 38-43) -->
<h1 class="text-4xl md:text-5xl lg:text-6xl font-extrabold text-gray-900 mb-6 leading-tight">
    Dagelijkse Viral Deals<br>
    <span class="bg-gradient-to-r from-purple-600 to-pink-600 bg-clip-text text-transparent">
        Amazon Nederland
    </span>
</h1>

<!-- Subheadline (Lines 44-46) -->
<p class="text-xl md:text-2xl text-gray-600 mb-12 max-w-3xl mx-auto">
    #tiktokmademebuyit - Mis geen enkele trending deal!
</p>
```

### Tailwind CSS Tips for Beginners
- Font sizes use classes like `text-xl`, `text-2xl`, etc.
- Colors use format `text-{color}-{shade}` (e.g., `text-purple-600`)
- Spacing uses `m-` for margin and `p-` for padding
- Responsive classes start with screen sizes: `md:` or `lg:`

Example of modifying a button's appearance:
```html
<!-- Original Button -->
<a href="#" class="inline-flex items-center px-8 py-4 text-lg font-semibold text-white bg-gradient-to-r from-purple-600 to-pink-600 rounded-full">

<!-- To make button larger -->
<a href="#" class="inline-flex items-center px-10 py-5 text-xl font-bold text-white bg-gradient-to-r from-purple-600 to-pink-600 rounded-full">
```

## Managing Links

### Navigation Menu Links
Current internal links in the navigation:
```html
<div class="hidden lg:flex space-x-8">
    <a href="#deals">Deals</a>
    <a href="#voordelen">Voordelen</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update these links:
1. Identify the section ID you want to link to
2. Add `#` followed by the section ID
3. Ensure the target section has a matching `id` attribute

### WhatsApp Channel Link
The current WhatsApp link appears twice in the code:
```html
<!-- Update this URL in both locations -->
href="https://whatsapp.com/channel/0029VbBWx8c6RGJLIuXz3G1J"
```

### Social Media Links
Located in the footer:
```html
<div class="flex space-x-4">
    <a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">
        <i class="fab fa-tiktok text-2xl"></i>
    </a>
    <!-- Replace # with your social media URLs -->
</div>
```

## Adding Privacy and Terms Pages

### Footer Link Setup
Current placeholder links in footer:
```html
<ul class="space-y-2 text-gray-400">
    <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

To link to new pages:
1. Create `privacy.html` and `terms.html` in your root directory
2. Update the links:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure section IDs match exactly (case-sensitive)
   - Check for extra spaces in IDs
   - Verify the `#` symbol is present in the href

2. **Responsive Design Issues**
   - Check responsive classes (`md:`, `lg:`)
   - Test on different screen sizes
   - Verify the viewport meta tag is present:
   ```html
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   ```

3. **Font Awesome Icons Not Showing**
   - Verify the Font Awesome CDN link is present:
   ```html
   <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
   ```
   - Check icon class names match exactly

### Need Help?
If you encounter issues:
1. Check the browser's developer tools (F12) for errors
2. Verify all files are in the correct directory
3. Ensure all links use the correct relative paths
4. Double-check Tailwind CSS classes for typos

Remember to always test changes across different devices and browsers before pushing to production.