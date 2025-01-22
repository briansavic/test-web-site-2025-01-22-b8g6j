# Landing Page Maintenance Guide

This guide will help you maintain and customize the Test Web Site landing page. Follow these instructions carefully to make updates while preserving the design and functionality.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text:**
```html
<!-- Find this line in the header -->
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-purple-600 to-blue-500 bg-clip-text text-transparent">Test Web Site</a>
```
Replace "Test Web Site" with your company name while keeping the classes intact.

2. **Navigation Links:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Benefits</a>
    <a href="#contact" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Contact</a>
</div>
```
Update link text while maintaining the classes for consistent styling.

### Hero Section
Located at the top of the main content:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-purple-600 to-blue-500 bg-clip-text text-transparent">
    Test Web Site
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12 leading-relaxed">
    Transform your digital presence with innovative solutions designed for modern businesses.
</p>
```
- Replace heading and paragraph text
- Keep responsive classes (`text-4xl md:text-5xl lg:text-6xl`) to maintain proper sizing across devices

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white rounded-2xl p-8 shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="w-12 h-12 bg-purple-100 rounded-full flex items-center justify-center mb-6">
        <!-- Icon SVG here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Test Feature 1</h3>
    <p class="text-gray-600">Innovative solutions designed to enhance your digital presence.</p>
</div>
```
- Update feature titles and descriptions
- Maintain card structure and classes for consistent layout
- Icons can be replaced by modifying the SVG code

## Fixing Broken Links

### Current Link Inventory
1. Navigation Menu Links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#contact">Contact</a>
```

2. Call-to-Action Links:
```html
<a href="https://test.com" class="...">Get Started</a>
```

### Updating Links
1. Replace placeholder URLs:
- Change `https://test.com` to your actual website URL
- Verify internal links (#features, #benefits, #contact) match section IDs
- Example:
```html
<!-- Before -->
<a href="https://test.com">Get Started</a>
<!-- After -->
<a href="https://yourwebsite.com/signup">Get Started</a>
```

2. Update Email Links:
```html
<!-- Find in contact section -->
<p class="text-xl text-gray-600 mb-12">Contact us at test@test.com</p>
```
Replace with your actual contact email.

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links in the Quick Links section:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Quick Links</h4>
    <ul class="space-y-2">
        <!-- Existing links -->
        <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

## Troubleshooting

### Common Issues

1. **Broken Gradients**
If gradient text disappears:
```html
<!-- Ensure these classes are present -->
bg-gradient-to-r from-purple-600 to-blue-500 bg-clip-text text-transparent
```

2. **Mobile Menu Issues**
Check that the mobile menu button has these classes:
```html
<button class="md:hidden text-gray-600 hover:text-gray-900">
```

3. **Responsive Layout Problems**
Verify grid classes are correct:
```html
grid grid-cols-1 md:grid-cols-3 gap-8
```

### Need Help?
- Double-check all class names match exactly
- Verify Tailwind CSS CDN link is working
- Ensure all sections have correct ID attributes
- Test on multiple devices and browsers

Remember to always backup your code before making changes, and test thoroughly after each modification.