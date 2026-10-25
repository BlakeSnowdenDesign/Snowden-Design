# About page: Wix setup

This page follows the design direction and the SEO/GEO spec (`docs/seo-geo-strategy.md`, PR #5). Wix shows embeds in an iframe, and search engines give iframe text little credit. So the H1, the intro and the question answers are **native Wix text**, and the embed holds the designed body of the page.

## Page structure, top to bottom

| # | Element | Type |
| --- | --- | --- |
| 1 | Site header | Native |
| 2 | Hero: eyebrow, H1, intro, button, plus the cube signature on the right | Native section + `shared/snowden-signature.html` embed |
| 3 | "Who is Blake Snowden?" answer block | Native |
| 4 | Story, services, principles, clients, motto, CTA | Embed `pages/about/snowden-about.html` |
| 5 | Site footer with name, Denver, 720-340-2611 and email | Native |

### 2. Native hero
- **Section:** full width, with an inner box at a 1,240 px content width and a 40 px corner radius. Background Midnight Ink `#0A1D26`, with an optional radial glow in Atlantic `#123440` at the top right. Padding: 120 px top, 72 px bottom, 64 px sides.
- **Eyebrow** (text, Satoshi Bold 12 px, uppercase, 0.14em letter spacing, Glacier Aqua `#7FE0D4`): `ABOUT THE STUDIO / DENVER, COLORADO`
- **H1** (set the text to Heading 1; Google Sans Flex 800, 64 to 96 px, white, line height 0.95, letter spacing -0.04em). Put the second line in Glacier Aqua:
  `Blake Snowden,` / `Denver web developer and 3D artist.`
- **Intro** (Paragraph, Satoshi 19 px, white at 80%): "I'm Blake Snowden, a Denver web developer and 3D artist. I build Wix websites, render products in 3D and run SEO and GEO growth plans, with strategy, design, media and code coming from the same desk."
- **Button:** "Book a free consultation", linking to the Contact page. Pill shape, Glacier Aqua fill, Midnight Ink text, at least 48 px tall.
- **Signature:** add Embed HTML, paste `shared/snowden-signature.html`, and place it on the right half of the hero at about 560 × 520 px, behind nothing. It has a transparent background. On phone, either set it to 100% width at 50% opacity behind the text, or hide it.

### 3. Native answer block (for GEO)
Snow `#FAFCFC` background, 96 px top padding, two columns.
- **H2:** "Who is Blake Snowden?"
- **Answer** (Paragraph, Satoshi 18 px, Slate): "Blake Snowden is a web developer and 3D artist in Denver, Colorado, and the founder of Snowden Design. He designs and builds Wix websites, creates graphics, video and 3D product renders, and pairs that with B2B and B2C business development strategy, so one person is accountable from the first plan to launch."
- **H2:** "What does Snowden Design do?"
- **Answer:** "Snowden Design is a Denver web design studio. It builds Wix websites and handles UX, SEO and GEO, graphics, digital art and 3D, video and drone footage, brand consulting, digital marketing, lead generation and project management for clients across Colorado and the US."

### 4. Embed
Embed HTML, full width, paste `snowden-about.html`. Height: **4,860 px** desktop, **5,270 px** tablet, **7,000 px** phone. Accessible name (Embed settings > "What's in the embed"): "About Blake Snowden: story, services, principles and client sites".

## SEO panel
- **URL slug:** `/about`
- **Title tag:** About Blake Snowden | Denver Web Developer & 3D Artist
- **Meta description:** Blake Snowden is a Denver web developer and 3D artist who builds Wix websites, renders products in 3D and runs SEO and GEO growth plans for small businesses.
- **Open Graph image:** 1200 × 630 branded card (new portrait once there is one).
- **Primary keyword:** Denver web developer and 3D artist. It appears in the H1, the first sentence, the portrait alt text and the title.

## Structured data (Advanced SEO > Structured data markup)
Paste both blocks. The business block can instead go site-wide once, via Settings > Custom Code.

```json
{
  "@context": "https://schema.org",
  "@type": "Person",
  "@id": "https://www.snowden-design.com/about#blake",
  "name": "Blake Snowden",
  "jobTitle": "Web Developer and 3D Artist",
  "worksFor": { "@id": "https://www.snowden-design.com/#business" },
  "url": "https://www.snowden-design.com/about",
  "homeLocation": { "@type": "City", "name": "Denver" },
  "knowsAbout": ["Wix Studio", "Web development", "3D rendering", "SEO", "GEO", "Video production", "Business development strategy"]
}
```

```json
{
  "@context": "https://schema.org",
  "@type": "AboutPage",
  "url": "https://www.snowden-design.com/about",
  "mainEntity": { "@id": "https://www.snowden-design.com/about#blake" },
  "about": { "@id": "https://www.snowden-design.com/#business" }
}
```

Add `"image"` once there is a headshot URL, and `"sameAs": ["<LinkedIn URL>"]` once it's confirmed.

## For Blake to confirm
- "Book a free consultation" comes from the SEO spec. Keep it only if the first call really is free.
- The portrait is the existing 533 px image, shown at 340 px. Send a high-resolution headshot and it can be shown larger.
