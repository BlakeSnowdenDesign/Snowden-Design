# Snowden Design: SEO & GEO keyword strategy and page spec

Oct 25, 2026 · BLAKE · Living version: [Claude Doc](https://claude.ai/artifact/RHkYkpbJjWaaEhqbFMa7qd)

Every page built for the new Wix site follows this spec. Page threads (Claude and Replit) should read the "What Wix embeds can and can't control" section before building.

## Summary

Snowden Design should rank and get cited as **the Denver web designer who builds the site, renders the product in 3D, and runs the growth plan afterward**. That combination is rare locally, so it is the positioning every page reinforces.

Three primary targets carry the site:

1. **Web design Denver** (and "Denver web designer", "Colorado web design") for the Home page.
2. **3D product rendering / 3D modeling services** for the Work page, proven by the MONGRAIN projects.
3. **Website care plans + SEO/GEO, ads and social management** for a Services/Packages page, which is where recurring revenue comes from.

How to use this doc: the keyword map says what each cluster targets, the page assignments say which page owns which keyword (one primary per page, no two pages competing), and the spec and schema sections are the checklist every page build follows before BLAKE publishes in Wix.

Keyword priorities below are tiers based on intent and local competition, not measured search volumes. Validate them in Google Search Console and Keyword Planner 4 to 6 weeks after launch and re-rank.

## Keyword map

Eight clusters cover the skill set. Tier 1 = commercial intent and winnable locally, target first; Tier 2 = supporting pages and sections; Tier 3 = long-tail for FAQs, blog posts and GEO answers.

| Cluster | Primary keyword | Secondary and long-tail | Intent | Tier |
| --- | --- | --- | --- | --- |
| Local web design | web design Denver | Denver web designer; Colorado web design; small business website design Denver; custom website design Colorado; web developer Denver CO | Hire | 1 |
| Wix specialist | Wix web designer | Wix Studio designer Denver; Wix expert Colorado; Wix website redesign; Wix SEO setup; migrate website to Wix | Hire | 1 |
| 3D modeling and rendering | 3D product rendering services | 3D modeling services Denver; photorealistic product rendering; jewelry 3D rendering; CAD to render; 3D product visualization for ecommerce; 360 product spin | Hire | 1 |
| SEO | SEO services Denver | local SEO Colorado; Google Business Profile optimization; technical SEO audit; on-page SEO for small business; Wix SEO services | Hire | 1 |
| GEO / AI search | generative engine optimization | GEO services; AI search optimization; how to rank in ChatGPT answers; get cited by Google AI Overviews; answer engine optimization (AEO) | Learn, then hire | 2 |
| Analytics and reporting | Google Analytics 4 setup | GA4 dashboard for small business; Looker Studio website report; monthly website performance report; conversion tracking setup | Hire / learn | 2 |
| Hosting and care plans | website maintenance plans | website care plan Denver; managed website hosting Colorado; monthly website support; website updates and security monitoring | Hire (recurring) | 1 |
| Ads and social | Google Ads management Denver | PPC management small business; Meta ads management; social media management Denver; AI-assisted social media content; local service ads | Hire (recurring) | 2 |

**Brand and entity terms** (must appear consistently on every page and profile): Snowden Design, Blake Snowden, Denver, Colorado, web design, 3D rendering. Same business name, phone (720-340-2611, the Denver Google Voice line; retire 970.685.8733 from listings) and email (blake@snowden-design.com) everywhere, so search engines and AI models treat them as one entity.

**Question keywords for FAQs and GEO** (Tier 3):

- How much does a website cost in Denver?
- Is Wix good for SEO in 2026?
- What is GEO and how is it different from SEO?
- How do I get my business mentioned by ChatGPT or Google AI Overviews?
- What is included in a website maintenance plan?
- How much does 3D product rendering cost?
- Is 3D rendering cheaper than a product photoshoot?
- What should a monthly website analytics report include?
- Do I need Google Ads if I have good SEO?

**Avoid**: generic national head terms ("web design", "SEO") as a page's primary, and stuffing city names into every heading. Use one city mention in the title, one in the H1 or first paragraph, and the rest naturally.

## Page-to-keyword assignments

Each page owns one primary keyword and no other page uses that keyword as its primary. Supporting pages link to the owner with the keyword (or a close variant) as anchor text.

| Page | Slug | Primary keyword | Secondary keywords | Schema types |
| --- | --- | --- | --- | --- |
| Home | / | web design Denver | Denver web designer; Wix web designer; 3D product rendering; website care plans | ProfessionalService (LocalBusiness), WebSite, Organization |
| Work | /work | 3D product rendering services | web design portfolio Denver; jewelry 3D rendering (MONGRAIN); Wix website examples | CollectionPage, CreativeWork per project, ImageObject |
| Services | /services | Wix web designer Denver | custom website design Colorado; SEO services Denver; generative engine optimization; Google Analytics 4 setup | Service (one per offer), FAQPage |
| Growth packages | /packages | website maintenance plans | managed website hosting Colorado; Google Ads management Denver; social media management Denver; monthly website report | Service + OfferCatalog, FAQPage |
| SEO & GEO | /seo-geo | SEO services Denver | generative engine optimization; AI search optimization; local SEO Colorado; Google Business Profile optimization | Service, FAQPage |
| Analytics sample | /analytics-dashboard | GA4 dashboard for small business | Looker Studio website report; monthly website performance report | WebPage, Dataset (optional) |
| About | /about | Denver web developer and 3D artist | Blake Snowden; web design and 3D rendering Colorado | AboutPage, Person |
| Contact | /contact | contact a Denver web designer | free website consultation Denver; website quote Colorado | ContactPage, ProfessionalService |

Slug notes: Wix keeps old slugs like /contact-1 unless renamed. Rename to the slugs above and add 301 redirects from /projects and /contact-1 in Wix's URL Redirect Manager so existing rankings carry over.

If SEO & GEO and Services end up as one page, keep "SEO services Denver" on that merged page and drop the separate row; don't let both pages target it.

## GEO: getting cited in AI answers

AI answer engines (Google AI Overviews and AI Mode, ChatGPT search, Perplexity, Claude, Copilot) quote pages that state a clear, checkable answer, from an entity they can identify. The rules below make each page quotable.

1. **Answer first.** Under each H2, open with a 40 to 60 word direct answer, then the detail. Example: "A website care plan from Snowden Design costs $X per month and covers hosting, security updates, backups, a monthly GA4 report and one hour of edits."
2. **Use question headings.** Phrase H2/H3s the way people ask (the Tier 3 list above) and mark those blocks up with FAQPage schema.
3. **Be specific and quotable.** Numbers, prices or price ranges, timelines, deliverable lists, named tools (Wix Studio, GA4, Looker Studio, Blender/KeyShot or whatever BLAKE actually uses). Vague claims ("we deliver results") never get cited.
4. **Build one consistent entity.** Same name, Denver address or service area, phone 720-340-2611 and email on the site, Google Business Profile, LinkedIn, Behance/ArtStation, Clutch, Yelp and the Wix Marketplace profile. Link them all from Organization schema via `sameAs`.
5. **Show proof.** Named projects (MONGRAIN), before/after metrics, client quotes with names and companies. Add a Review/testimonial section only with real reviews.
6. **Visible dates and authorship.** "Updated October 2026" on service and pricing pages; Blake Snowden named as author with a Person schema on About.
7. **Let AI crawlers in.** In Wix SEO settings, edit robots.txt to allow Googlebot, Bingbot, OAI-SearchBot, GPTBot, ChatGPT-User, PerplexityBot, ClaudeBot and Google-Extended. Submit the sitemap in Google Search Console and Bing Webmaster Tools (Bing feeds ChatGPT and Copilot).
8. **Put the answer text where crawlers can read it.** See the Wix section: copy inside an HTML embed iframe is weak or invisible to crawlers, so answer paragraphs and FAQs belong in native Wix text.
9. **Earn mentions off-site.** Denver business directories, Colorado design associations, guest posts, and answering questions on Reddit and Quora under the brand name. AI models weight third-party mentions heavily.

How to measure: monthly, ask ChatGPT, Perplexity and Google AI Mode the top 10 Tier 1 and Tier 3 queries and log whether Snowden Design is named or linked. Pair that with GA4 referral traffic from chatgpt.com, perplexity.ai and copilot.microsoft.com. This log is also a strong item for the monthly client report in the growth packages.

## Per-page SEO spec

Every page ships with the title, description and social tags below, set in that page's Wix SEO panel, and follows the on-page rules after the table.

### Titles and meta descriptions (ready to paste)

Titles stay under 60 characters with the primary keyword first; descriptions run 140 to 160 characters and end with an action.

| Page | Title tag | Meta description |
| --- | --- | --- |
| Home | Web Design Denver \| Wix, 3D Rendering & SEO \| Snowden Design | Denver web designer building fast Wix sites, photorealistic 3D product renders and SEO/GEO growth plans. Book a free consultation with Snowden Design. |
| Work | 3D Product Rendering & Web Design Portfolio \| Snowden Design | See 3D product renders and Wix websites by Snowden Design, including photorealistic jewelry rendering for MONGRAIN. Based in Denver, serving clients nationwide. |
| Services | Wix Web Designer Denver \| Design, SEO & 3D \| Snowden Design | Custom Wix website design, SEO and GEO, GA4 analytics and 3D product rendering from a Denver web designer. Clear pricing, fast turnaround, local support. |
| Growth packages | Website Maintenance Plans & Growth Packages \| Snowden Design | Monthly website care plans: hosting, updates, security, GA4 reports, SEO/GEO, Google Ads and social media management from Snowden Design in Denver, CO. |
| SEO & GEO | SEO & GEO Services Denver \| Rank in Google and AI Answers | Local SEO and generative engine optimization in Denver. Get found on Google, in AI Overviews and in ChatGPT answers with structured data and content that ranks. |
| Analytics sample | Sample GA4 Dashboard for Small Business \| Snowden Design | See the Google Analytics 4 dashboard every Snowden Design client gets: traffic, leads, search rankings and AI referrals, reported monthly in plain English. |
| About | About Blake Snowden \| Denver Web Developer & 3D Artist | Blake Snowden is a Denver web developer and 3D artist who builds Wix websites, renders products in 3D and runs SEO and GEO growth plans for small businesses. |
| Contact | Contact Snowden Design \| Denver Web Designer \| 720-340-2611 | Book a free website consultation with Snowden Design in Denver. Call 720-340-2611 or email blake@snowden-design.com for a quote on design, 3D or SEO. |

### Social tags (Open Graph and X/Twitter)

- `og:title` and `og:description`: reuse the title and description above (Wix fills these from the SEO panel unless overridden under Social Share).
- `og:image`: a 1200 x 630 px JPG or PNG under 1 MB per page; use a MONGRAIN render on Work and a branded card elsewhere. Text kept inside the centre 1000 x 500 px so crops don't cut it.
- `og:type` = website (Home) or article (blog posts); `og:locale` = en_US; `og:site_name` = Snowden Design.
- `twitter:card` = summary_large_image. Add `twitter:site` only if BLAKE has an X account.

### On-page rules

1. **One H1 per page** containing the primary keyword, e.g. Home: "Denver web design, 3D rendering and growth plans". Wix page titles in the menu do not count as an H1.
2. **H2s for each section, H3s inside them**, never skipping levels. At least two H2s phrased as questions (GEO rule 2).
3. **Primary keyword in the first 100 words**, once in an H2, and in the image alt text of the lead image. Two or three natural uses per page is enough.
4. **Alt text** describes the image and its context in under 125 characters: "Photorealistic 3D render of a diamond engagement ring for MONGRAIN". Decorative images get empty alt. File names match: `mongrain-engagement-ring-3d-render.webp`, not `IMG_2041.png`.
5. **Images**: WebP or AVIF, at most 200 KB for photos and renders on page (offer full-size renders via click-through), explicit width and height to avoid layout shift, lazy-loading below the fold.
6. **Internal links**: every page links to Services and Contact; Work project cards link to the matching service; the Packages page links to the Analytics sample. Anchor text uses keywords ("3D product rendering services"), never "click here".
7. **Canonical** = the clean `https://www.snowden-design.com/<slug>` URL (Wix sets it; check it isn't pointing at the wixsite.com address).
8. **NAP block** (name, Denver service area, 720-340-2611, email) in the site footer, identical on every page.
9. **Calls to action**: one primary CTA per screen ("Book a free consultation"), and a tel: link on mobile.
10. **Performance and accessibility**: target LCP under 2.5 s, CLS under 0.1, INP under 200 ms on mobile in PageSpeed Insights; colour contrast at least 4.5:1; every form field labelled.

## JSON-LD schema templates

Paste these into each page's Wix SEO panel (Advanced SEO, Structured data markup), never inside an HTML embed, where crawlers won't credit them. Replace anything in angle brackets, and delete fields you can't fill truthfully. Validate each page in Google's [Rich Results Test](https://search.google.com/test/rich-results) and the [Schema Markup Validator](https://validator.schema.org/).

### 1. Business entity (Home and Contact; site-wide if added once in Custom Code)

Snowden Design is a service-area business, so the address carries city and region only, with no street line, matching how the Google Business Profile should be set up.

```json
{
  "@context": "https://schema.org",
  "@type": "ProfessionalService",
  "@id": "https://www.snowden-design.com/#business",
  "name": "Snowden Design",
  "url": "https://www.snowden-design.com/",
  "logo": "https://www.snowden-design.com/<logo-path>.png",
  "image": "https://www.snowden-design.com/<og-image>.jpg",
  "description": "Denver web design studio building Wix websites, photorealistic 3D product renders and SEO/GEO growth plans.",
  "telephone": "+1-720-340-2611",
  "email": "blake@snowden-design.com",
  "founder": { "@id": "https://www.snowden-design.com/about#blake" },
  "address": {
    "@type": "PostalAddress",
    "addressLocality": "Denver",
    "addressRegion": "CO",
    "addressCountry": "US"
  },
  "areaServed": [
    { "@type": "City", "name": "Denver" },
    { "@type": "State", "name": "Colorado" },
    { "@type": "Country", "name": "United States" }
  ],
  "knowsAbout": ["Web design", "Wix Studio", "3D modeling", "3D product rendering", "Search engine optimization", "Generative engine optimization", "Google Analytics 4", "Google Ads", "Social media marketing"],
  "priceRange": "$$",
  "sameAs": [
    "<Google Business Profile URL>",
    "<LinkedIn URL>",
    "<Instagram URL>",
    "<Behance or ArtStation URL>"
  ]
}
```

### 2. WebSite (Home only)

```json
{
  "@context": "https://schema.org",
  "@type": "WebSite",
  "@id": "https://www.snowden-design.com/#website",
  "name": "Snowden Design",
  "url": "https://www.snowden-design.com/",
  "publisher": { "@id": "https://www.snowden-design.com/#business" },
  "inLanguage": "en-US"
}
```

### 3. Service with packages (Services, Growth packages, SEO & GEO)

One Service block per offer. On the packages page, list each tier as an Offer; show the same prices in visible text or leave `price` out.

```json
{
  "@context": "https://schema.org",
  "@type": "Service",
  "name": "Website care and growth plans",
  "serviceType": "Website maintenance and digital marketing",
  "provider": { "@id": "https://www.snowden-design.com/#business" },
  "areaServed": { "@type": "State", "name": "Colorado" },
  "url": "https://www.snowden-design.com/packages",
  "hasOfferCatalog": {
    "@type": "OfferCatalog",
    "name": "Monthly packages",
    "itemListElement": [
      {
        "@type": "Offer",
        "name": "<Care plan name>",
        "description": "Hosting, security updates, backups, monthly GA4 report, 1 hour of edits.",
        "price": "<monthly price>",
        "priceCurrency": "USD",
        "priceSpecification": { "@type": "UnitPriceSpecification", "price": "<monthly price>", "priceCurrency": "USD", "unitCode": "MON" }
      },
      { "@type": "Offer", "name": "<Growth plan name>", "description": "Care plan plus SEO/GEO, Google Business Profile and AI-answer tracking." },
      { "@type": "Offer", "name": "<Ads and social plan name>", "description": "Google Ads and Meta ads management plus AI-assisted social content." }
    ]
  }
}
```

For 3D rendering on Services, repeat the Service block with `"name": "3D product rendering"` and `"serviceType": "3D modeling and rendering"`.

### 4. FAQPage (any page with a visible FAQ)

The questions and answers must match the visible text word for word. Google now shows FAQ rich results only for a small set of authoritative sites, but AI engines still read this markup, so it stays.

```json
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "What is GEO and how is it different from SEO?",
      "acceptedAnswer": { "@type": "Answer", "text": "<the same 40 to 60 word answer shown on the page>" }
    },
    {
      "@type": "Question",
      "name": "What is included in a website care plan?",
      "acceptedAnswer": { "@type": "Answer", "text": "<visible answer>" }
    }
  ]
}
```

### 5. Person (About)

```json
{
  "@context": "https://schema.org",
  "@type": "Person",
  "@id": "https://www.snowden-design.com/about#blake",
  "name": "Blake Snowden",
  "jobTitle": "Web Developer and 3D Artist",
  "worksFor": { "@id": "https://www.snowden-design.com/#business" },
  "url": "https://www.snowden-design.com/about",
  "image": "https://www.snowden-design.com/<headshot>.jpg",
  "homeLocation": { "@type": "City", "name": "Denver" },
  "knowsAbout": ["Wix Studio", "3D rendering", "SEO", "GEO", "Google Analytics 4"],
  "sameAs": ["<LinkedIn URL>"]
}
```

### 6. Portfolio project (Work, one per featured project)

```json
{
  "@context": "https://schema.org",
  "@type": "CreativeWork",
  "name": "MONGRAIN 3D product renders",
  "creator": { "@id": "https://www.snowden-design.com/about#blake" },
  "about": "Photorealistic 3D modeling and rendering for MONGRAIN",
  "image": ["https://www.snowden-design.com/<render-1>.webp"],
  "dateCreated": "<YYYY>",
  "keywords": "3D product rendering, jewelry 3D rendering, product visualization"
}
```

The `@id` values tie the blocks together so search engines and AI models read one business, one founder and one website.

## What Wix embeds can and can't control

**The biggest risk to rankings on this build: Wix renders every Embed Code element inside an iframe** ([Wix: HTML iFrame element](https://support.wix.com/en/article/studio-editor-adding-an-html-iframe-element)). Google may index iframe content separately or not credit it to the page at all, and AI crawlers mostly skip it. So the embed pages the other threads are building need a hybrid layout.

| Element | Where it must live | Why |
| --- | --- | --- |
| Title tag, meta description, URL slug | Page's SEO panel (Pages > More Actions > SEO Basics) | An embed can't reach the parent page's head |
| OG / X social tags, custom meta, canonical | SEO panel > Social share and Advanced SEO | Same |
| JSON-LD schema | SEO panel > Advanced SEO > Structured data markup ([Wix guide](https://support.wix.com/en/article/adding-structured-data-markup-to-your-sites-pages-2546962)); site-wide blocks can go in Settings > Custom Code (head), which doesn't need Velo | Schema inside an iframe is not attributed to the page |
| H1, intro paragraph, H2 section headings, FAQ answers, service descriptions, NAP footer | Native Wix text elements (set heading level in the text settings) | Crawlable, quotable, credited to the page |
| Images that should rank (renders, portfolio) | Native Wix image or gallery elements, with alt text set in Wix | Wix serves them optimized and indexable; images inside an iframe usually aren't |
| Animations, 3D viewers, interactive pricing toggles, the sample analytics dashboard, custom layouts | HTML embed | Visual and interactive parts where indexing doesn't matter |
| robots.txt, sitemap, 301 redirects | SEO & GEO dashboard > Tools and settings | Site-level, Wix-managed |

**Rule for the page threads:** each embed page keeps its keyword-bearing text in native Wix elements above and between embeds, or, if a section must stay in the embed, the same H1/intro/FAQ text is repeated in a native text block on the page. Give each embed an accessible name describing its content.

### Wix launch checklist (BLAKE, before the site-wide publish)

- [ ] Connect www.snowden-design.com to the new site and confirm https + www canonical
- [ ] Rename slugs per the assignments table; add 301s from /projects and /contact-1
- [ ] Paste title, description and OG image into each page's SEO panel
- [ ] Paste each page's JSON-LD into Structured data markup; run the Rich Results Test
- [ ] Edit robots.txt to allow AI crawlers (GEO rule 7)
- [ ] Connect Google Search Console (Wix SEO & GEO dashboard) and submit the sitemap; add Bing Webmaster Tools
- [ ] Connect GA4 via Settings > Marketing Integrations, and mark contact-form and tel: clicks as key events
- [ ] Update the Google Business Profile to 720-340-2611, Denver service area, website URL, and services list
- [ ] Change the phone on every directory and social profile to 720-340-2611
- [ ] Run PageSpeed Insights on Home and Work on mobile; fix anything over the targets in the on-page rules

As of this draft, Velo is off, which is fine: nothing in this spec needs it.
