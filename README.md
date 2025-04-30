# Landing Page Maintenance Guide

This guide will help you maintain and customize the landing page by providing detailed instructions for common updates and modifications.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains your logo and navigation menu. To update:

1. **Logo Text**
```html
<!-- Find this section -->
<div class="text-2xl font-bold bg-gradient-to-r from-blue-600 to-purple-600 bg-clip-text text-transparent">
    Logo
</div>
```
- Replace "Logo" with your company name
- The gradient effect is created by `bg-gradient-to-r from-blue-600 to-purple-600`
- To change colors, replace `blue-600` and `purple-600` with other Tailwind colors

2. **Navigation Links**
```html
<div class="hidden md:flex space-x-8">
    <a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
    <a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Benefits</a>
    <a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Contact</a>
</div>
```
- Update link text between `<a>` tags
- `hidden md:flex` means the menu is hidden on mobile and visible on medium screens
- `space-x-8` controls spacing between links

### Hero Section
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-extrabold text-gray-900 mb-8 leading-tight tracking-tight">
    Lorem ipsum dolor
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12 leading-relaxed">
    Lorem ipsum dolor
</p>
```
- Replace "Lorem ipsum dolor" with your headline and subheadline
- Text sizes use responsive classes:
  - `text-4xl`: Default size
  - `md:text-5xl`: Medium screens
  - `lg:text-6xl`: Large screens

### Features Section
```html
<div class="p-8 bg-white rounded-2xl shadow-lg hover:shadow-xl transform hover:scale-105 transition-all duration-300">
    <h3 class="text-xl font-semibold mb-4 text-gray-900">Lorem ipsum dolor</h3>
    <p class="text-gray-600 leading-relaxed">Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
</div>
```
- Copy this card structure to add more features
- Update heading and paragraph text
- Key classes:
  - `rounded-2xl`: Rounded corners
  - `shadow-lg`: Box shadow
  - `hover:scale-105`: Hover animation

## Fixing Broken Links

### Current Link Inventory
1. Navigation Menu Links:
```html
<a href="#">Features</a>
<a href="#">Benefits</a>
<a href="#">Contact</a>
```

To update links:
1. Replace `#` with proper URLs:
   ```html
   <!-- For same-page sections -->
   <a href="#features">Features</a>
   
   <!-- For external pages -->
   <a href="https://example.com/features">Features</a>
   ```

2. Add IDs to corresponding sections:
   ```html
   <section id="features" class="py-24 bg-white">
   ```

### Call-to-Action Buttons
```html
<!-- Update these href attributes -->
<a href="#" class="inline-flex items-center px-8 py-4...">Get Started</a>
<a href="#" class="inline-flex items-center px-8 py-4...">Contact Us</a>
```

## Linking Privacy and Terms Pages

### Adding Footer Links
1. Locate the footer section:
```html
<div class="grid grid-cols-1 md:grid-cols-4 gap-12">
    <div>
        <h4 class="text-white text-lg font-semibold mb-6">Company</h4>
        <ul class="space-y-4">
```

2. Add privacy and terms links:
```html
<ul class="space-y-4">
    <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

## Troubleshooting

### Common Issues

1. **Broken Responsive Design**
- Check that you haven't removed responsive classes (starting with `md:` or `lg:`)
- Maintain the container class: `container mx-auto px-6`

2. **Missing Hover Effects**
- Ensure hover classes (starting with `hover:`) remain intact
- Example: `hover:text-gray-900 hover:scale-105`

3. **Gradient Colors Not Showing**
- Verify the complete gradient chain is present:
  ```html
  bg-gradient-to-r from-[color] to-[color]
  ```

### Need Help?
- Check Tailwind CSS documentation for color options
- Use browser inspector to identify specific classes
- Test responsiveness using browser dev tools
- Maintain all transition classes for smooth animations

Remember to:
- Back up your code before making changes
- Test on multiple devices and browsers
- Keep the responsive design intact
- Maintain consistent styling across sections