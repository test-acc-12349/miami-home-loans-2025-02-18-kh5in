# Miami Home Loans Landing Page - Maintenance Guide

This guide will help you maintain and customize the Miami Home Loans landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step instructions for common updates.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text (MHL)**
```html
<!-- Find this line in the header section -->
<a href="/" class="text-2xl font-bold text-blue-600">MHL</a>
```
Simply replace "MHL" with your desired text.

2. **Navigation Menu Items**
```html
<a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Services</a>
```
- Replace "Services" with your new menu item name
- The `text-gray-600` class controls the text color
- `hover:text-blue-600` changes color on hover

### Hero Section
To update the main headline and subtext:

```html
<h1 class="text-4xl sm:text-5xl lg:text-6xl font-bold text-gray-900 tracking-tight mb-6">
    Best Mortgage Broker In Miami
</h1>
<p class="text-xl sm:text-2xl text-gray-600 mb-10">
    Expert mortgage solutions tailored to your needs
</p>
```
- Replace the text between the tags
- Text size classes explained:
  - `text-4xl`: Base size
  - `sm:text-5xl`: Size on small screens
  - `lg:text-6xl`: Size on large screens

### Feature Cards
Each feature card follows this structure:
```html
<div class="group bg-white rounded-2xl shadow-lg p-8 hover:shadow-xl transition-all duration-300">
    <!-- Icon container -->
    <h3 class="text-xl font-semibold mb-4">First Home Buyer</h3>
    <p class="text-gray-600">Expert guidance and support...</p>
</div>
```
To modify:
1. Update the title in the `<h3>` tag
2. Change description in the `<p>` tag
3. Keep the existing classes for consistent styling

## Fixing Broken Links

### Current Link Structure
The page contains several types of links:

1. **Navigation Menu Links**
```html
<a href="#features">Services</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="https://mhl.com">Get Started</a>
```
To update:
- Internal section links start with #
- External links need full URLs
- Replace "https://mhl.com" with your actual domain

2. **Call-to-Action Links**
```html
<a href="https://mhl.com" class="inline-flex items-center...">
    Start Your Application
</a>
```
Update all instances of "https://mhl.com" with your actual application URL.

## Linking Privacy and Terms Pages

### Footer Link Updates
Locate the legal section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold mb-6">Legal</h4>
    <ul class="space-y-3">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link privacy and terms pages:
1. Replace the `#` with proper paths:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

2. Create matching HTML files:
- Create `privacy.html` in the same directory
- Create `terms.html` in the same directory
- Use the same styling classes for consistency

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
- Ensure section IDs match href attributes
- Section IDs should not include spaces
- Example: `href="#features"` links to `id="features"`

2. **Responsive Design Issues**
- Don't remove responsive classes (sm:, md:, lg:)
- Keep the existing structure of grid classes
- Test on multiple screen sizes

3. **Style Inconsistencies**
- Maintain color classes (text-blue-600, bg-blue-600)
- Keep transition classes for hover effects
- Preserve padding and margin classes

### Need Help?
If you encounter issues:
1. Check the Tailwind CSS documentation
2. Verify all closing tags match opening tags
3. Ensure proper class spelling
4. Test links in multiple browsers

Remember to always backup your files before making changes!