# Alphington Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Alphington Accounting Services landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Main Sections Overview
The landing page is divided into these key sections:
- Header (Navigation)
- Hero Section
- Services Section
- Benefits Section
- FAQ Section
- Call-to-Action Section
- Footer

### Updating Text Content

#### Header/Navigation
```html
<!-- Located at the top of the page -->
<a href="/" class="text-2xl font-bold text-gray-900">Alphington</a>
```
To change the company name, modify the text between `>` and `</a>`.

#### Hero Section
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6">
    We transform numbers into opportunities
</h1>
<p class="text-xl text-gray-600 mb-10">
    Professional accounting services tailored to drive your business growth
</p>
```
- Update the main heading by changing the text between the `<h1>` tags
- Modify the subheading by changing the text between the `<p>` tags

### Understanding Tailwind CSS Classes

#### Common Class Patterns
1. **Spacing Classes**
   - `px-6`: Adds padding left and right
   - `py-4`: Adds padding top and bottom
   - `mb-6`: Adds margin bottom
   
2. **Typography Classes**
   - `text-xl`: Sets font size
   - `font-bold`: Sets font weight
   - `text-gray-600`: Sets text color

3. **Responsive Classes**
   - `md:text-5xl`: Applies style at medium screen size
   - `lg:text-6xl`: Applies style at large screen size

#### Example: Modifying a Service Card
```html
<div class="bg-white p-8 rounded-2xl shadow-lg hover:shadow-xl transition-shadow duration-300">
```
To change the padding, replace `p-8` with:
- `p-4` (smaller padding)
- `p-12` (larger padding)

## Fixing Broken Links

### Current Link Structure
1. **Navigation Menu Links**
```html
<div class="hidden md:flex space-x-8">
    <a href="#services">Services</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

2. **Call-to-Action Links**
```html
<a href="https://theaccountants.com" class="inline-block px-8 py-4 bg-blue-600">
```

### Updating Links
1. Replace `https://theaccountants.com` with your actual website URL
2. Ensure internal links match section IDs:
   ```html
   <!-- Section ID -->
   <section id="services">
   
   <!-- Corresponding Navigation Link -->
   <a href="#services">
   ```

## Linking Privacy and Terms Pages

### Current Footer Structure
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Adding Privacy and Terms Links
1. Create your privacy.html and terms.html files
2. Update the footer links:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
- Check that section IDs match exactly with href attributes
- IDs are case-sensitive
```html
<!-- Correct -->
<section id="services">
<a href="#services">

<!-- Wrong -->
<section id="Services">
<a href="#services">
```

2. **Responsive Design Issues**
- Check media query classes (md:, lg:)
- Ensure you're not removing important responsive classes
```html
<!-- Keep both classes for proper responsive behavior -->
<div class="hidden md:flex">
```

3. **Style Inconsistencies**
- Maintain consistent color classes (e.g., `text-blue-600`)
- Keep consistent spacing patterns (px-6, py-4)
- Preserve hover and transition effects:
```html
class="hover:text-white transition-colors duration-300"
```

### Need Help?
- Double-check all changes against the original code
- Test the page at different screen sizes
- Validate all links before deploying
- Keep a backup of the original code

Remember to test all changes in a development environment before pushing to production.