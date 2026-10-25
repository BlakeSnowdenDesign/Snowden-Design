# Contact page: Wix setup

This page follows the design direction and the SEO/GEO spec (`docs/seo-geo-strategy.md`, PR #5). The H1, the intro, the contact details and the form are **native Wix elements**. The embed holds only the "what happens next" steps and the hand-off panel.

## Page structure, top to bottom

| # | Element | Type |
| --- | --- | --- |
| 1 | Site header | Native |
| 2 | Hero: eyebrow, H1, intro, call and email buttons, plus the cube signature | Native section + `shared/snowden-signature.html` embed |
| 3 | What happens next + "Tell me what you're building" panel | Embed `pages/contact/snowden-contact.html` |
| 4 | Contact form | Native Wix Form |
| 5 | "How do I start a project?" answer block | Native |
| 6 | Site footer with name, Denver, 720-340-2611 and email | Native |

### 2. Native hero
Use the same section style as the About hero: Midnight Ink, 40 px radius, 1,240 px content width.
- **Eyebrow:** `TAKING NEW PROJECTS / DENVER, COLORADO`
- **H1** (Heading 1, Google Sans Flex 800, white; second line in Glacier Aqua): `Contact a Denver` / `web designer.`
- **Intro:** "Tell me about your brand, your audience and your timing. Snowden Design builds Wix websites, 3D product renders and SEO and GEO growth plans from Denver, Colorado."
- **Buttons:** "Call 720-340-2611" (link `tel:+17203402611`, Glacier Aqua pill) and "Email blake@snowden-design.com" (link `mailto:blake@snowden-design.com`, outline pill).
- **Signature embed:** on the right, about 560 × 480 px, transparent. Hide it on phone.

### 3. Embed
Embed HTML, full width, paste `snowden-contact.html`. Height: **1,050 px** desktop, **1,190 px** tablet, **1,710 px** phone. Accessible name: "How a Snowden Design project starts".

### 4. Native Wix Form (Add > Contact & Forms)
Place it directly under the embed, in a Snow `#FAFCFC` section, 1,240 px wide.

| Field | Type | Required |
| --- | --- | --- |
| Name | Short text | Yes |
| Email | Email | Yes |
| Phone | Phone | No |
| Project type | Dropdown: Web design and development; Branding, graphics and 3D; Video; SEO and GEO; Marketing and lead generation; Something else | Yes |
| Tell me about the project | Long text, placeholder "A few lines is plenty" | Yes |

- **Submit button:** "Start the conversation". Midnight Ink pill with white Satoshi Bold text, hover fill Studio Teal `#16B3A6`, at least 48 px tall.
- **Success message:** "Thanks. I'll be in touch."
- **Fields:** Mist `#EEF3F4` fill, 1.5 px border `rgba(10,29,38,.12)`, 20 px radius, Satoshi 16 px, focus border Studio Teal. Labels: Satoshi Bold 12 px, uppercase, 0.14em letter spacing, Slate.
- **Notifications:** send submissions to blake@snowden-design.com. In GA4, mark the form submit and `tel:` clicks as key events.

### 5. Native answer block (for GEO)
- **H2:** "How do I start a project with Snowden Design?"
- **Answer:** "Send the form above, call 720-340-2611 or email blake@snowden-design.com. Blake Snowden replies personally with a few questions, then sets up a discovery call about your business, content and goals. You leave with a plan covering scope, timing and the next step to launch."

## SEO panel
- **URL slug:** rename `/contact-1` to `/contact` and add a 301 redirect from `/contact-1` (SEO > URL Redirect Manager).
- **Title tag:** Contact Snowden Design | Denver Web Designer | 720-340-2611
- **Meta description:** Book a free website consultation with Snowden Design in Denver. Call 720-340-2611 or email blake@snowden-design.com for a quote on design, 3D or SEO.
- **Primary keyword:** contact a Denver web designer. It appears in the H1 and the title.

## Structured data (Advanced SEO > Structured data markup)
```json
{
  "@context": "https://schema.org",
  "@type": "ProfessionalService",
  "@id": "https://www.snowden-design.com/#business",
  "name": "Snowden Design",
  "url": "https://www.snowden-design.com/",
  "description": "Denver web design studio building Wix websites, photorealistic 3D product renders and SEO/GEO growth plans.",
  "telephone": "+1-720-340-2611",
  "email": "blake@snowden-design.com",
  "founder": { "@id": "https://www.snowden-design.com/about#blake" },
  "address": { "@type": "PostalAddress", "addressLocality": "Denver", "addressRegion": "CO", "addressCountry": "US" },
  "areaServed": [{ "@type": "City", "name": "Denver" }, { "@type": "State", "name": "Colorado" }, { "@type": "Country", "name": "United States" }]
}
```
```json
{
  "@context": "https://schema.org",
  "@type": "ContactPage",
  "url": "https://www.snowden-design.com/contact",
  "about": { "@id": "https://www.snowden-design.com/#business" }
}
```
If the business block is added site-wide via Custom Code, paste only the ContactPage block here.

## For Blake to confirm
- The meta description says "free website consultation", from the SEO spec. Keep it only if the first call really is free.
