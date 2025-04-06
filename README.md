# AI Revolution Landing Page - Maintenance Guide

This guide will help you maintain and customize the AI Revolution landing page. It's written for beginners with no prior coding experience.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the site logo and navigation menu. To modify:

1. Update the logo text:
```html
<!-- Find this line in the header -->
<div class="text-2xl font-bold text-blue-600">AI Revolution</div>
```
Simply replace "AI Revolution" with your desired text.

### Hero Section
Located at the top of the page with the main headline:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight">
    AI is Taking Over. Blockchain is making waves.
</h1>
```

To modify:
1. Change the headline text between the `<h1>` tags
2. Adjust text size using these Tailwind classes:
   - `text-4xl`: Base size
   - `md:text-5xl`: Medium screens
   - `lg:text-6xl`: Large screens

### Feature Cards
Each feature card follows this structure:
```html
<div class="bg-white rounded-xl shadow-lg p-8 hover:shadow-xl transition-shadow duration-300">
    <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mb-6">
        <i class="fas fa-robot text-2xl text-blue-600"></i>
    </div>
    <h3 class="text-xl font-semibold mb-4">24/7 AI Assistant</h3>
    <p class="text-gray-600">Access your personal AI assistant...</p>
</div>
```

To modify:
1. Change icon: Replace `fa-robot` with any [Font Awesome icon](https://fontawesome.com/icons)
2. Update heading: Modify text within `<h3>` tags
3. Update description: Modify text within `<p>` tags

### Common Tailwind Classes Explained
- `bg-white`: White background
- `text-gray-600`: Gray text color
- `rounded-xl`: Rounded corners
- `shadow-lg`: Box shadow
- `hover:scale-105`: Grows slightly on hover
- `transition-all`: Smooth transitions
- `duration-300`: Transition timing

## Managing Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="hover:text-blue-600 transition-colors duration-300">Features</a>
    <a href="#benefits" class="hover:text-blue-600 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="hover:text-blue-600 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="hover:text-blue-600 transition-colors duration-300">Contact</a>
</div>
```

To update:
1. Locate the `href` attribute
2. For internal links (same page):
   - Use `#section-id` format
   - Ensure the target section has matching ID
3. For external links:
   - Replace with full URL: `href="https://example.com"`

### Call-to-Action Buttons
There are two main CTA buttons:
```html
<!-- Top button -->
<a href="https://go.e1ulife.com/ai-takeover?affid=Silwane1" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-lg">
    Start Earning Now
</a>

<!-- Bottom button -->
<a href="https://go.e1ulife.com/ai-takeover?affid=Silwane1" class="inline-block bg-white text-blue-600 px-8 py-4 rounded-lg">
    Get Started Now
</a>
```

To update:
1. Replace the `href` value with your affiliate or destination link
2. Update button text between the `<a>` tags

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your website folder:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Locate these lines in the footer:
```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

Replace the `#` with:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match exactly with link hrefs
   - Example: `href="#features"` needs `id="features"` on target section

2. **Responsive Design Issues**
   - Check mobile view using browser dev tools
   - Verify all `md:` and `lg:` prefixed classes are present

3. **Icons Not Showing**
   - Confirm Font Awesome CSS is properly loaded
   - Check icon class names against Font Awesome documentation

4. **Styling Problems**
   - Verify Tailwind CSS CDN link is working
   - Check for typos in class names
   - Use browser inspector to debug styles

For additional help or advanced customization, please refer to:
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [Font Awesome Icons](https://fontawesome.com/icons)