# Likhari (لکھاری – Stationers)
### *Aesthetic E-Commerce Web Platform with Technical SEO & CI/CD Pipeline*

[![GitHub Pages](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-success?style=for-the-badge&logo=github)](https://mahrukh-adeel.github.io/Likhari-DM/)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Schema.org](https://img.shields.io/badge/Schema.org-JSON--LD%20SEO-008080?style=for-the-badge&logo=schema-dot-org)](https://schema.org/)
[![CI/CD](https://img.shields.io/badge/CI%2FCD-GitHub%20Actions-blue?style=for-the-badge&logo=githubactions&logoColor=white)](https://github.com/Mahrukh-Adeel/Likhari-DM/actions)

---

## Executive Summary

**Likhari (لکھاری – Stationers)** is an e-commerce storefront designed for stationery enthusiasts, artists, and students seeking curated, aesthetic, and affordable writing supplies. 

Engineered as a high-performance, lightweight web application, the project highlights a balance between **clean frontend UI design**, **digital marketing optimization**, and **modern web performance standards**. Beyond core e-commerce interfaces, the platform features production-grade **Technical SEO** (Schema.org JSON-LD structured data, XML sitemaps, canonical tagging, next-gen image compression) and automated zero-downtime deployment via **GitHub Actions**.

> **Live Production Site:** [https://mahrukh-adeel.github.io/Likhari-DM/](https://mahrukh-adeel.github.io/Likhari-DM/)

---

## Key Highlights & Employer Focus

| Focus Area | Engineering Implementation & Business Impact |
| :--- | :--- |
| **Zero-Framework Performance** | Built with semantic HTML5, modular CSS3, and vanilla JavaScript—delivering ultra-fast page load speeds, zero bundle overhead, and low latency. |
| **Technical SEO & Search Visibility** | Integrated JSON-LD structured data (`WholesaleStore`, `Product` schemas), Google-compliant XML sitemaps (`sitemap.xml`), and HTML sitemaps to optimize search engine crawling, indexation, and rich snippets. |
| **Next-Gen Asset Optimization** | Implemented modern **AVIF** and **WebP** image formats alongside browser-level image preloading, reducing network payload and optimizing First Contentful Paint (FCP). |
| **E-Commerce UX Flow** | Complete multi-page user journeys: interactive hero carousels, categorized product showcase grids, shopping cart order summaries with discount coupon validation, and an exhaustive FAQ / customer support center. |
| **CI/CD Automation** | Integrated continuous deployment pipeline with GitHub Actions (`static.yml`) for automated artifact generation and zero-config static hosting on GitHub Pages. |

---

## Core Feature Breakdown

### 1. Dynamic Landing Experience (`index.html`)
- **Interactive Hero Carousel:** Automated timer-based image transition with synchronized manual navigation controls (`prev` / `next`) and DOM-level preloading for smooth transitions.
- **Top Promotional Bar:** High-visibility announcement banner highlighting shipping thresholds ("Free shipping on orders above Rs. 2000").
- **Product Category Showcases:** Horizontal scroll-snapped product carousels across key departments:
  - *New Arrivals* (Novelty paper cutters, space clips, translucent organizers)
  - *Journals & Notebooks* (A5 spiral notebooks, loose-leaf refills)
  - *Highlighters & Markers* (Fluorescent pens, double-head acrylic markers)
  - *Antique & Traditional Stationery* (Calligraphy reed pens / Qalam, Dawat ink pots, parchment papers)
  - *Aesthetic Sticker Packs* (Panda PVC sheets, decorative floral boxes)
- **Email Newsletter CTA:** Lead generation subscription form integrated into the footer.

### 2. Department Catalogues (`Journals.html`, `Highlighters.html`, `NewArrivals.html`)
- Clean responsive card layouts with uniform image containers, SKU pricing in PKR, and one-click "Add to Cart" interactions.
- Modular navigation with quick category switching and breadcrumbs.

### 3. Shopping Cart & Checkout Mockup (`Cart.html`)
- Master-detail cart interface displaying itemized orders with dynamic quantity incrementors/decrementors (`+`/`-`) and item removal actions.
- Coupon and promo-code application interface.
- Real-time order summary calculation (Subtotal, Discount deduction, Final Total, and Checkout CTA).

### 4. Customer Trust & Knowledge Base (`FAQ.html`, `AboutUs.html`)
- Detailed step-by-step order placement guide, supported payment methods (Visa, Mastercard, PayPal, Bank Transfer), return policy breakdown, and brand story.

---

## Technical SEO & Digital Marketing Architecture

To demonstrate digital marketing strategy and search discoverability, the repository incorporates industry-standard SEO patterns:

### Structured Data (JSON-LD)
Rich snippet markup enables Google Search to understand store identity and individual product offerings directly on the Search Engine Results Page (SERP):

```html
<!-- Local / Wholesale Store Entity Schema -->
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "WholesaleStore",
  "name": "Likhari",
  "image": "https://cdn3.iconfinder.com/data/icons/feather-5/24/pen-tool-256.png",
  "url": "https://mahrukh-adeel.github.io/Likhari-DM/",
  "address": {
    "@type": "PostalAddress",
    "addressLocality": "Islamabad",
    "postalCode": "44000",
    "addressCountry": "PK"
  },
  "sameAs": "https://www.facebook.com/profile.php?id=61559555609354" 
}
</script>

<!-- Product Schema for Rich SERP Snippets -->
<script type="application/ld+json">
{
  "@context": "https://schema.org/", 
  "@type": "Product", 
  "name": "Kuromi Spiral A5 Notebook",
  "image": "https://mahrukh-adeel.github.io/Likhari-DM/product-image7.webp",
  "offers": {
    "@type": "Offer",
    "priceCurrency": "PKR",
    "price": "950"
  }
}
</script>
```

### Crawlability & Canonicalization
- **Canonical URLs:** `<link rel="canonical" href="https://mahrukh-adeel.github.io/Likhari-DM/">` prevents duplicate content penalties across protocol/subpath variants.
- **XML Sitemap:** Standards-compliant `sitemap.xml` with defined page priorities (`1.0` for home, `0.8` for catalogues) and timestamps.
- **HTML Sitemap:** Accessible `sitemap.html` providing user and crawler fallback navigation.
- **Optimized Metadata:** Focused title tags (`لکھاری – Stationers`), localized meta descriptions, keywords, and mobile theme-color customization (`#d3e7ff`).

---

## Repository Structure

```text
Likhari-DM/
├── .github/
│   └── workflows/
│       └── static.yml           # GitHub Actions workflow for automatic Pages deployment
├── AboutUs.html                 # Brand story, mission, core values, and team info
├── Cart.html                    # Shopping cart interface, coupon input, and order summary
├── Categories.html              # Category directory route
├── FAQ.html                     # Customer support knowledge base & ordering FAQ
├── Highlighters.html            # Highlighters & markers department catalogue
├── Journals.html                # Aesthetic notebooks and loose-leaf journal catalogue
├── Login.html                   # User authentication portal
├── NewArrivals.html             # New inventory and trending products showcase
├── PrivacyPolicy.html           # Store privacy and customer data policy
├── Stickers.html                # Sticker sheets and novelty stationery catalogue
├── Vintage.html                 # Traditional and calligraphy supplies catalogue
├── Wishlist.html                # Saved products wishlist page
├── popular.html                 # Most popular and bestseller listing
├── index.html                   # Primary storefront landing page with hero carousel & products
├── sitemap.html                 # User-facing HTML sitemap
├── sitemap.xml                  # Search-engine XML sitemap for Google Search Console
├── style.css                    # Central stylesheet (flexbox layouts, responsive design, themes)
├── script.js                    # Global JavaScript module
├── logo.jpg                     # Brand identity logo
├── wallpaper.jpg                # High-resolution aesthetic hero asset
└── product-image*.{avif,webp,jpg} # Optimized multi-format product imagery
```

---

## Technology Stack

- **Markup & Semantics:** HTML5, Schema.org Microdata/JSON-LD
- **Styles & Layout:** CSS3 (Custom Flexbox Grid, Media Queries, Keyframe Animations)
- **Typography & Icons:** [Google Fonts (Truculenta)](https://fonts.google.com/specimen/Truculenta), [FontAwesome 6.5.1](https://fontawesome.com/)
- **Scripting & DOM:** Vanilla ES6+ JavaScript
- **DevOps & Hosting:** GitHub Actions, GitHub Pages CDN
- **Asset Formats:** AVIF, WebP, JPG

---

## Local Development Setup

To explore or run this project locally, no heavy package managers or compilers are required:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Mahrukh-Adeel/Likhari-DM.git
   cd Likhari-DM
   ```

2. **Serve locally:**
   You can open `index.html` directly in your browser, or launch a local development server:
   
   *Using Python 3:*
   ```bash
   python3 -m http.server 8000
   ```
   *Using VS Code:*
   Right-click `index.html` and select **"Open with Live Server"**.

3. **Visit the app:**
   Open [http://localhost:8000](http://localhost:8000) in your web browser.

---

## Engineering Roadmap & Scalability Next Steps

- [ ] **Persistent State Management:** Implement `localStorage` / `IndexedDB` caching for shopping cart items and wishlist synchronization across browser sessions.
- [ ] **Full-Text Client-Side Search:** Implement a fast, fuzzy client-side search engine (e.g., Fuse.js or mini-search) for instant product filtering.
- [ ] **Headless E-Commerce Integration:** Connect checkout actions to Stripe Checkout or Shopify Storefront API for live credit card and digital wallet transactions.
- [ ] **PWA Support:** Add a Web App Manifest (`manifest.json`) and service worker for offline catalogue browsing and app installation.

---

## Authors & Academic Credits

Developed as part of the **Digital Marketing & Web Development** curriculum in the **Department of Computer Science (BSCS - 4th Semester)** at **National University of Modern Languages (NUML), Islamabad**.

- **Sara Khan** – Frontend Development, Component Styling, Cart & Catalogues ([@SaraKhan-24](https://github.com/SaraKhan-24))
- **Mahrukh Adeel** – Technical SEO, Schema Markup, Sitemap Architecture & Deployment ([@Mahrukh-Adeel](https://github.com/Mahrukh-Adeel))

---

## License

This project is open-source and available under the [MIT License](https://opensource.org/licenses/MIT).
