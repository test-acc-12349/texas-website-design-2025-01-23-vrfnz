# Texas Website Design - Landing Page Maintenance Guide

This guide will help you maintain and customize the Texas Website Design landing page. Whether you're new to web development or just getting started, follow these instructions to make updates safely and effectively.

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
<!-- Find this line in the header -->
<div class="text-2xl font-bold text-blue-600">TWD</div>
```
- Replace "TWD" with your desired text
- Adjust size using `text-2xl` (options: text-sm, text-lg, text-3xl, etc.)
- Change color using `text-blue-600` (options: text-red-600, text-green-600, etc.)

### Hero Section
Located at the top of the page with main headline:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight">
    Texas Website Design
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">Best Websites In Texas</p>
```
- Update text between tags
- Responsive text sizes use format: `base-size:md:larger-size`
- Spacing uses `mb-` (margin-bottom) classes (mb-2 = small, mb-12 = large)

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white p-8 rounded-xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="text-blue-600 mb-4"><i class="fas fa-pencil-ruler text-3xl"></i></div>
    <h3 class="text-xl font-bold mb-4">Custom Design</h3>
    <p class="text-gray-600">Unique, tailored websites...</p>
</div>
```
To modify:
1. Change icon: Update `fa-pencil-ruler` with any [Font Awesome](https://fontawesome.com/icons) icon
2. Update heading: Replace text in `<h3>` tag
3. Update description: Modify text in `<p>` tag

## Fixing Broken Links

### Navigation Menu Links
Current navigation links:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```
To update:
1. Internal links (same page):
   - Use `#section-id` format
   - Ensure section IDs match exactly
2. External links:
   - Replace `#` with full URL
   - Example: `href="https://example.com/page"`

### Footer Links
Current footer structure:
```html
<ul class="space-y-2">
    <li><a href="#" class="hover:text-white transition-colors duration-300">Web Design</a></li>
    <li><a href="#" class="hover:text-white transition-colors duration-300">Development</a></li>
    <li><a href="#" class="hover:text-white transition-colors duration-300">SEO</a></li>
</ul>
```
To update:
1. Replace `#` with proper URLs
2. Maintain the `hover:text-white transition-colors duration-300` classes for consistent styling

## Linking Privacy and Terms Pages

### Adding Privacy Policy Link
Locate this section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```
Update links:
1. Replace `#` with `/privacy.html` for privacy policy
2. Replace `#` with `/terms.html` for terms of service
3. Example:
```html
<li><a href="/privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
```

## Troubleshooting

### Common Issues:

1. **Broken Internal Links:**
   - Ensure section IDs match navigation links exactly
   - Check for typos in href attributes
   - IDs are case-sensitive

2. **Responsive Design Issues:**
   - Maintain responsive classes (md:, lg:) when updating
   - Test on multiple screen sizes
   - Don't remove container classes

3. **Icon Not Showing:**
   - Verify Font Awesome CDN link in header
   - Check icon class names against Font Awesome documentation
   - Ensure proper icon prefix (fas, far, fab)

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Verify changes in multiple browsers
- Use browser developer tools (F12) to inspect elements

Remember to always backup your files before making changes, and test thoroughly on different devices and browsers after updates.