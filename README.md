# Landing Page Maintenance Guide

This guide will help you maintain and customize your TexasWeb landing page. Follow these detailed instructions to make common updates while preserving the design and functionality.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains your logo and navigation menu. To update:

1. **Logo Text:**
```html
<!-- Find this line in the header section -->
<a href="#" class="text-2xl font-bold text-primary">TexasWeb</a>
```
- Replace "TexasWeb" with your business name
- Adjust text size by changing `text-2xl` to `text-xl` (smaller) or `text-3xl` (larger)

2. **Navigation Menu Items:**
```html
<nav class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-primary transition duration-300 font-medium">Features</a>
    <!-- Additional menu items -->
</nav>
```
- Update link text between `>` and `</a>`
- Maintain the class structure to preserve hover effects

### Hero Section
Located at the top of the page:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight tracking-tight mb-6">Custom Websites For Your Business</h1>
<p class="text-xl text-gray-600 mb-8 max-w-2xl mx-auto">Professional web solutions designed to help Texas businesses stand out and grow online.</p>
```

To modify:
- Update heading text between `<h1>` tags
- Change subheading text between `<p>` tags
- Adjust text size using Tailwind classes:
  - `text-4xl` for smaller screens
  - `md:text-5xl` for medium screens
  - `lg:text-6xl` for large screens

### Features Section
Each feature card follows this structure:

```html
<div class="bg-white p-8 rounded-xl shadow-md hover:shadow-lg transition duration-300 transform hover:-translate-y-1">
    <div class="w-14 h-14 bg-blue-100 rounded-full flex items-center justify-center mb-6">
        <i class="fas fa-mobile-alt text-primary text-2xl"></i>
    </div>
    <h3 class="text-xl font-bold text-gray-900 mb-3">Responsive Design</h3>
    <p class="text-gray-600">Looks perfect on any device...</p>
</div>
```

To update:
1. Change icon: Replace `fa-mobile-alt` with any [Font Awesome](https://fontawesome.com/icons) icon class
2. Update heading: Modify text between `<h3>` tags
3. Update description: Change text between `<p>` tags

## Fixing Broken Links

### Navigation Menu Links
Current internal links in the navigation:

```html
<nav class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</nav>
```

To update:
1. For internal sections: Use `#section-name`
2. For external pages: Replace `#` with full URL
   ```html
   <a href="https://your-domain.com/page">Page Name</a>
   ```

### Call-to-Action Links
Located in hero and CTA sections:

```html
<a href="https://sigmaseo.io" class="inline-flex items-center justify-center px-8 py-3...">
```

Replace `https://sigmaseo.io` with your desired URL.

### Footer Links
Social media links need updating:

```html
<div class="flex space-x-4">
    <a href="#" class="text-gray-400 hover:text-white transition duration-300">
        <i class="fab fa-facebook-f"></i>
    </a>
    <!-- Additional social links -->
</div>
```

Replace `#` with your social media profile URLs.

## Linking Privacy and Terms Pages

### Adding Privacy and Terms Links
Locate the footer section:

```html
<div class="flex space-x-6">
    <a href="#" class="text-gray-400 hover:text-white text-sm transition duration-300">Privacy Policy</a>
    <a href="#" class="text-gray-400 hover:text-white text-sm transition duration-300">Terms of Service</a>
</div>
```

Update with proper links:
```html
<a href="/privacy.html" class="text-gray-400 hover:text-white text-sm transition duration-300">Privacy Policy</a>
<a href="/terms.html" class="text-gray-400 hover:text-white text-sm transition duration-300">Terms of Service</a>
```

## Troubleshooting

### Common Issues

1. **Broken Responsive Design**
   - Don't remove `md:` or `lg:` prefixes from classes
   - Maintain the existing responsive class structure
   ```html
   text-4xl md:text-5xl lg:text-6xl
   ```

2. **Missing Icons**
   - Ensure Font Awesome CSS is loaded
   - Check icon class names on [Font Awesome](https://fontawesome.com/icons)
   - Maintain the `fas`, `fab`, or `far` prefix

3. **Broken Links**
   - Internal links must match section IDs exactly
   - External links need `https://` prefix
   - Check for typos in URLs

### Need Help?
If you encounter issues:
1. Compare your changes with the original code
2. Verify all opening tags have matching closing tags
3. Check browser console for errors (Right-click > Inspect > Console)
4. Ensure all files are in the correct directory

Remember to test all changes across different devices and browsers to ensure consistency.