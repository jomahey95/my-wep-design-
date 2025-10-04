# Design Your Future Vision

A bilingual (Arabic/English), responsive, single-page website with a separate gallery page, featuring a polished light/dark theme, RTL/LTR support, and modern UI.

## Features
- **Bilingual UI (AR/EN)** with language toggle (🌐) and persistence via `localStorage`.
- **Light/Dark theme** with animated toggle (☀️/🌙), system preference detection, and persistence.
- **Sticky, glassy navbar** with dropdowns and hover effects.
- **Responsive design** with mobile-friendly hamburger menu on the home page.
- **Hero section** with CTAs.
- **Back-to-top button** for better UX.
- **Gallery page** (`gallery.html`) with a responsive grid, lazy-loading images, and the ability to open images in new tabs (plus an "Open all" utility).

## Project Structure
```
my project/
├─ index.html          # Home page with theme + language system
├─ gallery.html        # Gallery page integrated with same theme/translation logic
├─ images/             # Place your images here
└─ README.md
```

## Getting Started
1. Open `index.html` directly in your browser (double-click) or serve via a local server.
2. Use the **🌐** button to toggle languages (Arabic/English). The app updates layout direction automatically (RTL/LTR) and remembers your choice.
3. Use the **☀️/🌙** toggle to switch theme. It respects system settings by default and remembers your choice via `localStorage`.
4. Click **المعرض (Gallery)** in the navbar to open the gallery page in a new tab.

## Adding Images to the Gallery
Copy your images to the `images/` folder so they can load from `gallery.html`.

PowerShell example to create the folder and copy your provided files:
```powershell
$dest = 'C:\Users\victus\OneDrive\Desktop\my project\images'
New-Item -ItemType Directory -Path $dest -Force | Out-Null
$srcs = @(
 'C:\Users\victus\OneDrive\Desktop\my first project\images-interior 5.jpg',
 'C:\Users\victus\OneDrive\Desktop\my first project\images-interior 6.jpg',
 'C:\Users\victus\OneDrive\Desktop\my first project\images-interior 10.jpg',
 'C:\Users\victus\OneDrive\Desktop\my first project\images-interior 11.jpg',
 'C:\Users\victus\OneDrive\Desktop\my first project\images-interior0.jpg',
 'C:\Users\victus\OneDrive\Desktop\my first project\images-interior2.jpg',
 'C:\Users\victus\OneDrive\Desktop\my first project\images-interior3.jpg',
 'C:\Users\victus\OneDrive\Desktop\my first project\images-interior7.jpg',
 'C:\Users\victus\OneDrive\Desktop\my first project\images-interior8.jpg',
 'C:\Users\victus\OneDrive\Desktop\my first project\images-interior 4.jpg'
)
Copy-Item -LiteralPath $srcs -Destination $dest -Force
```
If your file names or locations differ, update the paths in `gallery.html` accordingly.

## Customization
- **Branding/colors**: Adjust CSS variables in `index.html` and `gallery.html` under `:root` and `body.dark`.
- **Texts/translations**: Update the translation objects in scripts (`applyTranslations` functions) in both files.
- **Email link**: In `index.html`, set your email address in the mail icon link: `href="mailto:you@example.com"`.
- **Navbar items**: Update links/texts inside the `.navbar` sections.

## Recommended Improvements (optional)
- **Lightbox viewer** on gallery images (modal with next/prev and keyboard navigation).
- **SEO**: Add meta description, Open Graph tags, and a favicon.
- **Performance**: Preconnect to Google Fonts, compress images, and add `loading="lazy"` (already enabled for gallery images).
- **Accessibility**: Add `aria-expanded` to menu toggles and refine focus states.

## License
This project is free to use for personal and educational purposes. Add your preferred license if needed.
