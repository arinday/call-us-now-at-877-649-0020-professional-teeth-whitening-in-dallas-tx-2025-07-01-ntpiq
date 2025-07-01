# BrightSmile Landing Page - Maintenance Guide

This guide will help you maintain and customize the BrightSmile dental landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains your logo and navigation menu. To update:

1. **Logo Text:**
```html
<!-- Find this line in the header -->
<a href="/" class="text-2xl font-bold text-blue-600">BrightSmile</a>
```
- Replace "BrightSmile" with your business name
- Adjust size using `text-2xl` (options: text-lg, text-xl, text-3xl)
- Change color using `text-blue-600` (options: text-red-600, text-green-600)

2. **Navigation Links:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#services" class="text-gray-600 hover:text-blue-600">Services</a>
    <!-- Add or modify links here -->
</div>
```
- Update text between `<a>` tags
- Keep the `hidden md:flex` class to maintain mobile responsiveness

### Hero Section
Located at the top of the page:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight">
    Professional Teeth Whitening in Dallas, TX
</h1>
```
- Update heading text while maintaining the multi-size responsive classes
- Don't remove `leading-tight` as it controls line spacing

### Features Section
Each feature card follows this structure:
```html
<div class="p-8 bg-white rounded-xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="w-12 h-12 bg-blue-100 rounded-full">
        <!-- Icon here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">15-Min Response</h3>
    <p class="text-gray-600">Quick response time...</p>
</div>
```
- Keep the `p-8` padding and `rounded-xl` classes for consistent spacing
- Maintain hover effects with `hover:shadow-xl`

## Fixing Broken Links

### Navigation Menu Links
Current links in the navigation:
```html
<a href="#services">Services</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="tel:8776490020">(877) 649-0020</a>
```

To update:
1. Replace phone number:
   ```html
   <a href="tel:YOUR-NUMBER">YOUR-NUMBER</a>
   ```
2. For internal section links, ensure the href matches section IDs:
   ```html
   <a href="#section-id">Link Text</a>
   <!-- Corresponding section should have: -->
   <section id="section-id">
   ```

### Call-to-Action Links
Located in hero and CTA sections:
```html
<a href="tel:8776490020" class="inline-flex items-center justify-center px-8 py-4">
    Call Now
</a>
```
- Update both the `href` and button text
- Maintain the `inline-flex` and padding classes for proper button styling

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the footer:

```html
<!-- Find the Links section in footer -->
<div>
    <h3 class="text-xl font-bold mb-4">Links</h3>
    <ul class="space-y-2">
        <!-- Add these new lines -->
        <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Creating Policy Pages
1. Create new files:
   - `privacy.html`
   - `terms.html`

2. Use this basic template for each:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Privacy Policy - BrightSmile</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
</head>
<body class="font-inter">
    <!-- Copy header from index.html -->
    
    <main class="pt-32 px-4 container mx-auto">
        <h1 class="text-3xl font-bold mb-8">Privacy Policy</h1>
        <!-- Add your policy content here -->
    </main>

    <!-- Copy footer from index.html -->
</body>
</html>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Responsive Design:**
   - Check that you haven't removed important responsive classes like `md:` or `lg:`
   - Maintain the container class: `container mx-auto px-4`

2. **Misaligned Elements:**
   - Verify flex classes are intact: `flex items-center justify-center`
   - Check spacing utilities: `space-x-8`, `gap-4`

3. **Missing Styles:**
   - Confirm Tailwind CDN is loading
   - Check for typos in class names
   - Maintain the font import for 'Inter'

For additional help, refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs) or contact your web development team.