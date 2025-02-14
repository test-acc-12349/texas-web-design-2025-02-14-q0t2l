# Texas Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web Design landing page. It's written for beginners and provides step-by-step instructions for common updates.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your logo and navigation menu. To update:

1. Change the logo text:
```html
<!-- Find this line in the header section -->
<a href="/" class="text-2xl font-bold text-blue-600">TWD</a>
```
Simply replace "TWD" with your desired text.

### Hero Section
The main banner section includes your primary headline and subheading:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">Texas Web Design</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-8">Best Websites In Texas</p>
```

To modify:
1. Replace "Texas Web Design" with your main headline
2. Replace "Best Websites In Texas" with your subheading
3. The text sizes are responsive:
   - `text-4xl`: Default size
   - `md:text-5xl`: Medium screens
   - `lg:text-6xl`: Large screens

### Features and Benefits Sections
Each feature/benefit card follows this structure:

```html
<div class="bg-white p-8 rounded-xl shadow-lg hover:shadow-xl transition duration-300">
    <div class="w-16 h-16 bg-blue-100 rounded-lg flex items-center justify-center mb-6">
        <i class="fas fa-server text-2xl text-blue-600"></i>
    </div>
    <h3 class="text-xl font-bold mb-4">Free Hosting</h3>
    <p class="text-gray-600">Premium hosting included with every website package</p>
</div>
```

To update:
1. Change the icon by replacing the `fa-server` class with any [Font Awesome icon](https://fontawesome.com/icons)
2. Modify the heading text inside the `<h3>` tag
3. Update the description in the `<p>` tag

## Managing Links

### Navigation Menu Links
The navigation menu contains internal links to page sections:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Contact</a>
</div>
```

To update:
1. The `href="#section-name"` corresponds to section IDs in the HTML
2. Ensure any new sections you add have matching IDs
3. Keep the same class structure for consistent styling

### External Links
Update these placeholder links:

```html
<!-- Hero section -->
<a href="https://twd.com" class="px-8 py-4 bg-blue-600 text-white rounded-lg">Get Started</a>

<!-- Contact section -->
<a href="mailto:admin@twd.com" class="inline-block px-8 py-4 bg-white">Contact Us</a>

<!-- Footer email -->
<a href="mailto:admin@twd.com" class="hover:text-white transition-colors duration-300">admin@twd.com</a>
```

Replace all instances of:
- `https://twd.com` with your website URL
- `admin@twd.com` with your contact email

## Adding Privacy and Terms Pages

### 1. Create New Pages
Create two new files in your website directory:
- `privacy.html`
- `terms.html`

### 2. Update Footer Links
Locate this section in the footer:

```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

Replace the `#` placeholders:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues:

1. **Broken Internal Links**
   - Ensure section IDs match exactly with href attributes
   - IDs are case-sensitive
   - Example: `href="#FAQ"` won't link to `id="faq"`

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - These control how elements appear on different screen sizes
   - Example: `hidden md:flex` hides on mobile, shows on medium screens

3. **Icon Not Showing**
   - Verify Font Awesome is properly loaded
   - Check icon class names on [Font Awesome's website](https://fontawesome.com)
   - Ensure you're using the correct icon prefix (`fas`, `fab`, etc.)

### Need Help?
If you encounter issues:
1. Check the browser's developer tools (F12) for errors
2. Verify all files are in the correct directory
3. Ensure all links point to existing files or sections
4. Maintain the existing class structure when making changes

Remember to test all changes across different screen sizes using your browser's responsive design mode (F12 > Toggle device toolbar).