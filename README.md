# Landing Page Maintenance Guide

This guide will help you maintain and customize the WebAgency landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Modifying Text Content

#### Hero Section
The main headline and subheading are located in the hero section. To update:

```html
<!-- Original -->
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8">
    Best Web Agency In Sydney
</h1>

<!-- How to modify -->
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8">
    Your New Headline Here
</h1>
```

#### Features Section
Each feature card contains a title and description:

```html
<h3 class="text-xl font-semibold mb-4">Easy to Use</h3>
<p class="text-gray-400">Intuitive interfaces and user-friendly designs...</p>
```

### Understanding Tailwind Classes

Key classes used in this landing page:

- Layout Classes:
  - `container`: Centers content
  - `mx-auto`: Horizontal auto margins
  - `px-6`: Horizontal padding
  - `py-24`: Vertical padding

- Responsive Classes:
  - `md:text-4xl`: Applies at medium screens
  - `lg:text-6xl`: Applies at large screens

To modify responsive behavior:

```html
<!-- Original -->
<div class="text-xl md:text-2xl">

<!-- Make text larger on all screens -->
<div class="text-2xl md:text-3xl">
```

## Fixing Broken Links

### Navigation Menu Links
Current navigation links are:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update:
1. Locate the `href` attribute
2. Replace with new link:
   ```html
   <!-- Internal link (same page) -->
   <a href="#section-name">Section</a>
   
   <!-- External link -->
   <a href="https://your-site.com/page">Page</a>
   ```

### Call-to-Action Links
Update the "Get Started" links:

```html
<!-- Find this link in the header -->
<a href="https://fixrr.online" class="hidden md:inline-flex items-center...">

<!-- Replace with your URL -->
<a href="https://your-website.com" class="hidden md:inline-flex items-center...">
```

## Linking Privacy and Terms Pages

### Adding Policy Links
In the footer section, locate:

```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

Update the links:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

### Maintaining Consistent Styling
When adding new links, always include these classes:
- `hover:text-white`: Changes text color on hover
- `transition-colors`: Smooth color transition
- `duration-300`: Transition timing

## Troubleshooting

Common issues and solutions:

1. **Broken Layout**
   - Check if you've removed any `container` classes
   - Verify `px-6` padding classes are present
   - Ensure responsive classes (`md:`, `lg:`) are intact

2. **Links Not Working**
   - For internal links (#section), verify section IDs exist
   - For external links, include `https://` prefix
   - Check for typos in URLs

3. **Animations Not Working**
   - Verify AOS script is loaded
   - Check `data-aos` attributes are present
   - Ensure no conflicting JavaScript

Remember:
- Always test changes in multiple browsers
- Check mobile responsiveness
- Back up files before making changes
- Use browser developer tools to inspect elements

Need more help? Contact your web development team or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).