# Landing Page Maintenance Guide

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains your logo and navigation menu. To update:

```html
<!-- Logo Text -->
<a href="/" class="text-2xl font-bold text-blue-600">Hoogwerker<span class="text-gray-700">Huur</span></a>
```
- To change the logo text, modify "Hoogwerker" and "Huur"
- The `text-blue-600` class controls the blue color
- The `text-gray-700` class controls the gray color

### Hero Section
Located at the top of the page with the main headline:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">
    🔥 Hoogwerker Huren Amersfoort Met Korting
</h1>
```
- Update the emoji by changing or removing "🔥"
- Modify headline text while keeping the classes intact
- The responsive text sizes are:
  - Mobile: `text-4xl`
  - Tablet: `md:text-5xl`
  - Desktop: `lg:text-6xl`

### Features Section
Each feature card follows this structure:

```html
<div class="bg-white p-8 rounded-2xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="text-3xl mb-4">💰</div>
    <h3 class="text-xl font-bold mb-4">Tot 30% Korting</h3>
    <p class="text-gray-600">Profiteer nu van onze tijdelijke actie</p>
</div>
```
- Change emojis in the `text-3xl` div
- Update headings in the `h3` tags
- Modify description text in the `p` tags
- Keep the styling classes to maintain design consistency

## Fixing Broken Links

### Navigation Menu Links
Current navigation links are:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Voordelen</a>
    <a href="#pricing">Prijzen</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update:
1. Identify the section ID you want to link to
2. Update the `href` attribute with `#section-id`
3. Example: `<a href="#new-section">New Section</a>`

### External Links
Main call-to-action buttons currently point to:
```html
<a href="https://hoogwerkerhurenamersfoort.nl">
```

To update:
1. Replace the URL with your desired destination
2. Ensure the URL includes `https://` or `http://`
3. Test the link after updating

## Linking Privacy and Terms Pages

### Footer Links Section
Current placeholder links:

```html
<ul class="space-y-2">
    <li><a href="#" class="hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="hover:text-blue-400 transition-colors duration-300">Algemene Voorwaarden</a></li>
</ul>
```

To add proper links:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-blue-400 transition-colors duration-300">Algemene Voorwaarden</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match exactly with href attributes
   - Section IDs are case-sensitive
   - Example: `href="#FAQ"` won't link to `id="faq"`

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - These control how elements appear on different screen sizes
   - Example: `hidden md:flex` hides on mobile, shows on tablet/desktop

3. **Style Inconsistencies**
   - Keep the same color classes (e.g., `text-blue-600`)
   - Maintain spacing classes (e.g., `mb-4`, `py-20`)
   - Use existing button styles for new buttons:
```html
class="bg-blue-600 text-white px-6 py-2 rounded-full hover:bg-blue-700 transform hover:scale-105 transition-all duration-300"
```

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs) for class references
- Verify all changes in multiple browsers
- Test on both mobile and desktop views
- Keep a backup of the original HTML before making changes

Remember to test all changes thoroughly before pushing to production!