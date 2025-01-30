# Strongback Landing Page Maintenance Guide

This guide will help you maintain and customize the Strongback wheelchair landing page. It's designed for beginners with no prior coding experience.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name**: Locate this line in the header:
```html
<a href="#" class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">Strongback</a>
```
Simply replace "Strongback" with your desired text.

2. **Navigation Menu Items**: Find these lines:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-300 hover:text-white transition-colors">Features</a>
    <a href="#benefits" class="text-gray-300 hover:text-white transition-colors">Benefits</a>
    <a href="#contact" class="text-gray-300 hover:text-white transition-colors">Contact</a>
</div>
```
Replace the text between `<a>` tags to change menu items.

### Hero Section
The main headline and subheading are in the first section:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent">
    Strongback Comfort 24 Heavy Duty Wheelchair
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    Lightweight Yet Heavy Duty – Only 35.9 lbs, Supports 375 lbs
</p>
```

To modify:
- Change headline text between `<h1>` tags
- Update subheading between `<p>` tags
- Keep the classes intact to maintain styling

### Tailwind CSS Classes Explained
Common classes used throughout:
- `text-[size]`: Controls text size (xl, 2xl, 3xl, etc.)
- `mb-[number]`: Adds margin bottom (4, 8, 12, etc.)
- `py-[number]`: Adds padding top and bottom
- `bg-[color]`: Sets background color
- `md:`: Applies styles only on medium screens and up

## Managing Links

### Navigation Links
Current navigation links are:
1. Features (`#features`)
2. Benefits (`#benefits`)
3. Contact (`#contact`)

To update:
```html
<!-- Original -->
<a href="#features">Features</a>

<!-- Update to external link -->
<a href="https://yoursite.com/features">Features</a>

<!-- Update to internal page -->
<a href="features.html">Features</a>
```

### Call-to-Action Links
The "Buy Now" buttons currently point to:
```html
<a href="https://shrsl.com/4tt97" class="bg-gradient-to-r from-purple-600 to-pink-600...">
```

To update:
1. Locate all instances of `https://shrsl.com/4tt97`
2. Replace with your desired URL
3. Test each link after updating

## Adding Privacy and Terms Pages

### Current Footer Links
```html
<div>
    <h3 class="text-xl font-bold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors">Terms of Service</a></li>
    </ul>
</div>
```

To link privacy and terms pages:

1. Create new HTML files:
   - `privacy.html`
   - `terms.html`

2. Update the footer links:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors">Terms of Service</a></li>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Styles**
   - Check that Tailwind CSS is properly loaded
   - Verify class names are spelled correctly
   - Ensure responsive classes (md:, lg:) are in the correct order

2. **Links Not Working**
   - Verify file names match exactly (case-sensitive)
   - Check if files are in the correct directory
   - Test URLs in a new browser tab

3. **Animation Issues**
   - Confirm AOS script is loaded
   - Check data-aos attributes are properly set
   - Verify AOS initialization in the script section

Remember to:
- Always test changes in multiple browsers
- Back up files before making changes
- Maintain consistent styling across all pages
- Test responsive design at different screen sizes

Need help? Contact your web development team or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).