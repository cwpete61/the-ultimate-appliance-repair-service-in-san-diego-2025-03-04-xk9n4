# SD Appliance Repair Landing Page - Maintenance Guide

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains your company name and navigation menu. To update:

1. **Company Name:**
```html
<!-- Find this line in the header section -->
<a href="#" class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">
    SD Appliance Repair  <!-- Replace this text -->
</a>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <!-- Each menu item can be updated here -->
    <a href="#services" class="text-gray-300 hover:text-white transition-colors duration-300">Services</a>
</div>
```

### Hero Section
The main banner section contains your primary headline and call-to-action:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent">
    The Ultimate Appliance Repair Service in San Diego  <!-- Update headline here -->
</h1>

<p class="text-xl md:text-2xl text-gray-300 mb-12">
    Professional, reliable, and affordable appliance repair services at your doorstep  <!-- Update subheading -->
</p>
```

#### Understanding Tailwind Classes
- `text-4xl`: Base text size
- `md:text-5xl`: Text size on medium screens
- `lg:text-6xl`: Text size on large screens
- `mb-8`: Margin bottom spacing
- `text-gray-300`: Text color

### Features Section
Each feature card follows this structure:
```html
<div class="bg-gray-900 rounded-2xl p-8 transform hover:scale-105 transition-all duration-300 shadow-xl hover:shadow-2xl border border-gray-700">
    <!-- Icon container -->
    <div class="w-16 h-16 bg-gradient-to-br from-purple-500 to-pink-500 rounded-full flex items-center justify-center mb-6">
        <!-- SVG icon here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Same Day Service</h3>  <!-- Feature title -->
    <p class="text-gray-400">Quick response times and efficient service</p>  <!-- Feature description -->
</div>
```

## Fixing Broken Links

### Current Link Inventory
1. Navigation Menu Links:
```html
<a href="#services">Services</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

2. Call-to-Action Links:
```html
<!-- Hero Section CTA -->
<a href="https://google.com" class="inline-block px-8 py-4...">
    Schedule Service Now  <!-- Replace google.com with your booking URL -->
</a>

<!-- Contact Section Email -->
<a href="mailto:You@email.com" class="inline-block px-8 py-4...">
    Contact Us Now  <!-- Update email address -->
</a>
```

### Updating Links
1. Replace placeholder URLs:
```html
<!-- From -->
<a href="https://google.com">Schedule Service Now</a>

<!-- To -->
<a href="https://your-booking-system.com">Schedule Service Now</a>
```

2. Update email addresses:
```html
<!-- From -->
<a href="mailto:You@email.com">Contact Us Now</a>

<!-- To -->
<a href="mailto:your.actual@email.com">Contact Us Now</a>
```

## Linking Privacy and Terms Pages

### Footer Links Section
Locate the Legal section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Adding Policy Links
1. Create your policy pages (privacy.html and terms.html)
2. Update the href attributes:
```html
<!-- From -->
<a href="#">Privacy Policy</a>

<!-- To -->
<a href="privacy.html">Privacy Policy</a>

<!-- And -->
<a href="terms.html">Terms of Service</a>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links:**
- Ensure all section IDs match their corresponding links
- Example: `<section id="services">` matches `<a href="#services">`

2. **Responsive Design Issues:**
- Check Tailwind breakpoint classes (md:, lg:)
- Example: `class="text-4xl md:text-5xl lg:text-6xl"`

3. **Gradient Text Not Showing:**
- Ensure all three classes are present:
  ```html
  bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent
  ```

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Test responsiveness using browser developer tools

Remember to always test your changes across different screen sizes and browsers after making updates.