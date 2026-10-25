# About page: Wix setup

## Page structure (Wix Studio)
1. Native site header (menu stays native).
2. **Embed HTML**, full width: paste `snowden-about.html`. Height: **5,650 px** desktop, **5,880 px** tablet, **7,620 px** phone.
3. Native site footer.

## SEO settings (Page settings > SEO basics)
- **URL slug:** `/about`
- **Title tag:** About Blake Snowden | Snowden Design, Denver Web Designer
- **Meta description:** Blake Snowden is the designer and developer behind Snowden Design in Denver, Colorado: web design and development, video, branding and B2B and B2C business development strategy.
- **Open Graph:** same title and description; image = a Snowden Design project screenshot or a new portrait.
- **Indexing:** allow. Canonical: self.

The page H1 ("Where art meets technology.") and intro sit inside the embed, which search engines treat as a separate document. Until the hero moves to native Wix text, keep the title and description above accurate. That way, the page still reads clearly in search.

## Structured data (Page settings > Advanced SEO > Structured data markup)
Includes only facts that are visible on the page.

```json
{
  "@context": "https://schema.org",
  "@type": "AboutPage",
  "url": "https://www.snowden-design.com/about",
  "mainEntity": {
    "@type": "Person",
    "name": "Blake Snowden",
    "jobTitle": "Designer and developer",
    "worksFor": {
      "@type": "ProfessionalService",
      "name": "Snowden Design",
      "url": "https://www.snowden-design.com",
      "email": "blake@snowden-design.com",
      "telephone": "+1-720-340-2611",
      "areaServed": "Denver, Colorado",
      "address": { "@type": "PostalAddress", "addressLocality": "Denver", "addressRegion": "CO", "addressCountry": "US" }
    },
    "knowsAbout": ["Web design", "Web development", "User experience", "SEO", "Graphics", "Digital art", "3D", "Video production", "Drone footage", "Brand consulting", "Digital marketing", "Lead generation", "Business development strategy"]
  }
}
```

## For Blake to confirm
- The facts line "Builds on: Wix Studio, plus custom code" is new copy.
- The portrait is the existing 533 px image, shown at 340 px. Send a high-resolution portrait to replace it, and it can be shown larger.
