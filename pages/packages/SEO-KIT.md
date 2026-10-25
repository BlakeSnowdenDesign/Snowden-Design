# Growth packages page: Wix SEO and GEO kit

Page: `/packages` · Primary keyword: **website maintenance plans** · Spec: [`docs/seo-geo-strategy.md`](../../docs/seo-geo-strategy.md) (PR #5)

Wix puts every Embed HTML element in an iframe, and Google gives text inside it little or no credit. So this page is a hybrid: the embed carries the visuals (plans, comparison table, sample dashboard, motion), and the text that has to rank lives in native Wix elements and the page's SEO panel. Build it top to bottom like this:

| Order | Element | Type | Content |
| --- | --- | --- | --- |
| 1 | Intro band | Native Wix text | H1 + answer-first intro + "Updated" line (below) |
| 2 | Packages embed | Embed HTML | `snowden-packages.html`, full width, height from the README table |
| 3 | FAQ | Native Wix text (or a Wix accordion) | H2 + nine questions as H3s, answers word for word (below) |
| 4 | NAP footer | Native Wix text, site-wide | Snowden Design · Denver, Colorado · 720-340-2611 · blake@snowden-design.com |

The embed keeps its own headings for accessibility; that's fine, because only the native H1 counts for the page.

## 1. Page SEO panel (Pages › Growth packages › SEO basics)

| Field | Value |
| --- | --- |
| URL slug | `packages` |
| Title tag | Website Maintenance Plans & Growth Packages \| Snowden Design |
| Meta description | Monthly website care plans: hosting, updates, security, GA4 reports, SEO/GEO, Google Ads and social media management from Snowden Design in Denver, CO. |
| Let search engines index this page | On |
| Social share image (og:image) | 1200 × 630 branded card or a Helen Falls Lodge screenshot, under 1 MB |
| Advanced SEO › Structured data | The JSON-LD in section 4 |

## 2. Native intro band (above the embed)

Set the heading as **Heading 1** in Wix text settings. Style it small (Archivo 28 to 34px) so it reads as an intro strip above the big hero.

**Website maintenance plans and growth packages** (H1)

Snowden Design's website maintenance plans keep your Wix site fast, secure and growing after launch. Three monthly plans, Basecamp, Ascent and Summit, cover managed hosting, backups and edits, SEO and GEO, AI-assisted social media, Google Ads and a Google Analytics 4 report every month, for businesses in Denver and across Colorado.

Updated October 2026

## 3. Native FAQ (below the embed)

**Questions about website maintenance plans** (H2)

**What is included in a website maintenance plan?** (H3)

A Snowden Design website maintenance plan covers managed Wix hosting, SSL, domain and email DNS, uptime and broken-link monitoring, monthly backups, content edits and a monthly Google Analytics 4 report. Higher plans add SEO and GEO, Google Business Profile management, new articles, AI-assisted social media, Google Ads and customer email follow-up.

**How much does a website maintenance plan cost?** (H3)

Basecamp is [$ ] per month, Ascent is [$ ] per month and Summit is [$ ] per month plus ad spend, which is paid directly to Google and Meta. Every plan includes managed hosting and a monthly GA4 report, and one-time projects such as 3D rendering are quoted separately.

**What is GEO and how is it different from SEO?** (H3)

Search engine optimization (SEO) helps your pages rank in Google's search results. Generative engine optimization (GEO) helps AI assistants such as ChatGPT, Google AI Overviews, Gemini, Perplexity and Claude understand your business, trust it and cite it in their answers. Both rely on fast pages, clear structured data and content that answers real questions.

**How do I get my business mentioned by ChatGPT or Google AI Overviews?** (H3)

Make your business easy to identify and quote: structured data that names your business, services and service area; clear answers to the questions customers ask; the same name, phone and address everywhere online; reviews and mentions on trusted sites; and a robots.txt file that lets AI crawlers read your site.

**What should a monthly website analytics report include?** (H3)

A useful monthly report compares users, sessions, engagement rate and leads with last month, breaks traffic down by channel with AI assistant referrals shown on their own, lists top pages and Google search queries, counts leads by source, and ends with a plain-language summary of what changed and what comes next.

**Do I need Google Ads if I have good SEO?** (H3)

Not always. SEO builds traffic that compounds over months, while Google Ads buys visibility today for searches you don't rank for yet, seasonal offers or new services. Many businesses run both: ads for fast leads and testing, SEO for a lower cost per lead over time.

**Does AI write my social media posts?** (H3)

AI helps research topics, draft options and pick posting times. A person at Snowden Design edits and approves every post before it goes live, so everything that carries your name sounds like you.

**Can I change plans later?** (H3)

Yes. Most clients start on the plan that fits their launch and move up as the site grows. Plans can be changed at the next billing cycle.

**Do you offer 3D modeling and rendering?** (H3)

Yes. Snowden Design creates 3D product, architectural and environment models, photoreal renderings and turntable animations as add-on projects that can be used on your website, in ads and on social media.

The second answer has price placeholders. Fill them with the same prices as the embed, or delete that question until prices are set (the schema must match the visible text).

## 4. Structured data (paste into Advanced SEO › Structured data markup)

It references `#business`, `#website` and `about#blake`, which the Home, About and Contact pages define (spec section 5). Validate with the [Rich Results Test](https://search.google.com/test/rich-results) after publishing.

```json
{
  "@context": "https://schema.org",
  "@graph": [
    {
      "@type": "WebPage",
      "@id": "https://www.snowden-design.com/packages#webpage",
      "url": "https://www.snowden-design.com/packages",
      "name": "Website Maintenance Plans & Growth Packages | Snowden Design",
      "description": "Monthly website care plans: hosting, updates, security, GA4 reports, SEO/GEO, Google Ads and social media management from Snowden Design in Denver, CO.",
      "inLanguage": "en-US",
      "dateModified": "2026-10-25",
      "isPartOf": {
        "@id": "https://www.snowden-design.com/#website"
      },
      "about": {
        "@id": "https://www.snowden-design.com/#business"
      },
      "author": {
        "@id": "https://www.snowden-design.com/about#blake"
      },
      "breadcrumb": {
        "@id": "https://www.snowden-design.com/packages#breadcrumb"
      },
      "mainEntity": {
        "@id": "https://www.snowden-design.com/packages#plans"
      }
    },
    {
      "@type": "BreadcrumbList",
      "@id": "https://www.snowden-design.com/packages#breadcrumb",
      "itemListElement": [
        {
          "@type": "ListItem",
          "position": 1,
          "name": "Home",
          "item": "https://www.snowden-design.com/"
        },
        {
          "@type": "ListItem",
          "position": 2,
          "name": "Services",
          "item": "https://www.snowden-design.com/services"
        },
        {
          "@type": "ListItem",
          "position": 3,
          "name": "Growth packages",
          "item": "https://www.snowden-design.com/packages"
        }
      ]
    },
    {
      "@type": "Service",
      "@id": "https://www.snowden-design.com/packages#plans",
      "name": "Website maintenance plans and growth packages",
      "serviceType": "Website maintenance and digital marketing",
      "provider": {
        "@id": "https://www.snowden-design.com/#business"
      },
      "url": "https://www.snowden-design.com/packages",
      "areaServed": [
        {
          "@type": "City",
          "name": "Denver"
        },
        {
          "@type": "State",
          "name": "Colorado"
        }
      ],
      "hasOfferCatalog": {
        "@type": "OfferCatalog",
        "name": "Monthly packages",
        "itemListElement": [
          {
            "@type": "Offer",
            "name": "Basecamp website care plan",
            "description": "Managed Wix hosting, SSL, domain and email DNS, uptime and broken-link monitoring, monthly backups, 1 hour of content edits a month, a quarterly technical SEO check and a monthly Google Analytics 4 report.",
            "itemOffered": {
              "@type": "Service",
              "@id": "https://www.snowden-design.com/packages#basecamp",
              "name": "Basecamp website care plan",
              "serviceType": "Website maintenance and managed Wix hosting",
              "description": "Managed Wix hosting, SSL, domain and email DNS, uptime and broken-link monitoring, monthly backups, 1 hour of content edits a month, a quarterly technical SEO check and a monthly Google Analytics 4 report.",
              "provider": {
                "@id": "https://www.snowden-design.com/#business"
              },
              "areaServed": [
                {
                  "@type": "City",
                  "name": "Denver"
                },
                {
                  "@type": "State",
                  "name": "Colorado"
                }
              ]
            }
          },
          {
            "@type": "Offer",
            "name": "Ascent growth plan",
            "description": "Everything in Basecamp with 3 hours of edits, plus monthly SEO and GEO, Google Business Profile management, 1 new article a month, 8 AI-assisted social posts a month on 2 platforms, a live analytics dashboard and a quarterly strategy call.",
            "itemOffered": {
              "@type": "Service",
              "@id": "https://www.snowden-design.com/packages#ascent",
              "name": "Ascent growth plan",
              "serviceType": "SEO, GEO and social media management",
              "description": "Everything in Basecamp with 3 hours of edits, plus monthly SEO and GEO, Google Business Profile management, 1 new article a month, 8 AI-assisted social posts a month on 2 platforms, a live analytics dashboard and a quarterly strategy call.",
              "provider": {
                "@id": "https://www.snowden-design.com/#business"
              },
              "areaServed": [
                {
                  "@type": "City",
                  "name": "Denver"
                },
                {
                  "@type": "State",
                  "name": "Colorado"
                }
              ]
            }
          },
          {
            "@type": "Offer",
            "name": "Summit performance plan",
            "description": "Everything in Ascent with 6 hours of edits, plus Google Ads and Meta ads management, 16 social posts a month on 3 platforms, email newsletter and lead follow-up automation, 2 new articles a month and a monthly strategy call. Ad spend is billed separately.",
            "itemOffered": {
              "@type": "Service",
              "@id": "https://www.snowden-design.com/packages#summit",
              "name": "Summit performance plan",
              "serviceType": "Google Ads, Meta ads, social media and email marketing management",
              "description": "Everything in Ascent with 6 hours of edits, plus Google Ads and Meta ads management, 16 social posts a month on 3 platforms, email newsletter and lead follow-up automation, 2 new articles a month and a monthly strategy call. Ad spend is billed separately.",
              "provider": {
                "@id": "https://www.snowden-design.com/#business"
              },
              "areaServed": [
                {
                  "@type": "City",
                  "name": "Denver"
                },
                {
                  "@type": "State",
                  "name": "Colorado"
                }
              ]
            }
          }
        ]
      }
    },
    {
      "@type": "Service",
      "@id": "https://www.snowden-design.com/packages#3d-rendering",
      "name": "3D modeling and rendering",
      "serviceType": "3D product, architectural and environment visualization",
      "provider": {
        "@id": "https://www.snowden-design.com/#business"
      },
      "url": "https://www.snowden-design.com/work"
    },
    {
      "@type": "FAQPage",
      "@id": "https://www.snowden-design.com/packages#faq",
      "mainEntity": [
        {
          "@type": "Question",
          "name": "What is included in a website maintenance plan?",
          "acceptedAnswer": {
            "@type": "Answer",
            "text": "A Snowden Design website maintenance plan covers managed Wix hosting, SSL, domain and email DNS, uptime and broken-link monitoring, monthly backups, content edits and a monthly Google Analytics 4 report. Higher plans add SEO and GEO, Google Business Profile management, new articles, AI-assisted social media, Google Ads and customer email follow-up."
          }
        },
        {
          "@type": "Question",
          "name": "How much does a website maintenance plan cost?",
          "acceptedAnswer": {
            "@type": "Answer",
            "text": "Basecamp is [$ ] per month, Ascent is [$ ] per month and Summit is [$ ] per month plus ad spend, which is paid directly to Google and Meta. Every plan includes managed hosting and a monthly GA4 report, and one-time projects such as 3D rendering are quoted separately."
          }
        },
        {
          "@type": "Question",
          "name": "What is GEO and how is it different from SEO?",
          "acceptedAnswer": {
            "@type": "Answer",
            "text": "Search engine optimization (SEO) helps your pages rank in Google's search results. Generative engine optimization (GEO) helps AI assistants such as ChatGPT, Google AI Overviews, Gemini, Perplexity and Claude understand your business, trust it and cite it in their answers. Both rely on fast pages, clear structured data and content that answers real questions."
          }
        },
        {
          "@type": "Question",
          "name": "How do I get my business mentioned by ChatGPT or Google AI Overviews?",
          "acceptedAnswer": {
            "@type": "Answer",
            "text": "Make your business easy to identify and quote: structured data that names your business, services and service area; clear answers to the questions customers ask; the same name, phone and address everywhere online; reviews and mentions on trusted sites; and a robots.txt file that lets AI crawlers read your site."
          }
        },
        {
          "@type": "Question",
          "name": "What should a monthly website analytics report include?",
          "acceptedAnswer": {
            "@type": "Answer",
            "text": "A useful monthly report compares users, sessions, engagement rate and leads with last month, breaks traffic down by channel with AI assistant referrals shown on their own, lists top pages and Google search queries, counts leads by source, and ends with a plain-language summary of what changed and what comes next."
          }
        },
        {
          "@type": "Question",
          "name": "Do I need Google Ads if I have good SEO?",
          "acceptedAnswer": {
            "@type": "Answer",
            "text": "Not always. SEO builds traffic that compounds over months, while Google Ads buys visibility today for searches you don't rank for yet, seasonal offers or new services. Many businesses run both: ads for fast leads and testing, SEO for a lower cost per lead over time."
          }
        },
        {
          "@type": "Question",
          "name": "Does AI write my social media posts?",
          "acceptedAnswer": {
            "@type": "Answer",
            "text": "AI helps research topics, draft options and pick posting times. A person at Snowden Design edits and approves every post before it goes live, so everything that carries your name sounds like you."
          }
        },
        {
          "@type": "Question",
          "name": "Can I change plans later?",
          "acceptedAnswer": {
            "@type": "Answer",
            "text": "Yes. Most clients start on the plan that fits their launch and move up as the site grows. Plans can be changed at the next billing cycle."
          }
        },
        {
          "@type": "Question",
          "name": "Do you offer 3D modeling and rendering?",
          "acceptedAnswer": {
            "@type": "Answer",
            "text": "Yes. Snowden Design creates 3D product, architectural and environment models, photoreal renderings and turntable animations as add-on projects that can be used on your website, in ads and on social media."
          }
        }
      ]
    }
  ]
}
```

## 5. Site-level GEO settings (once, for the whole site)

- **robots.txt** (SEO & GEO dashboard › Tools and settings): allow Googlebot, Bingbot, OAI-SearchBot, GPTBot, ChatGPT-User, PerplexityBot, ClaudeBot and Google-Extended.
- **GA4 key events**: contact form submit, `tel:` click, `mailto:` click. These feed the "Leads" tiles in the client report.
- **GA4 "AI assistants" channel** (Admin › Data display › Channel groups › copy the default group, add a channel above Referral): Source matches regex `chatgpt\.com|chat\.openai\.com|perplexity\.ai|gemini\.google\.com|copilot\.microsoft\.com|claude\.ai`. Set this up on every client site too, so the dashboard's AI row has data from month one.

## 6. Internal links in the embed

The embed links to `/services`, `/seo-geo` ("SEO services in Denver"), `/work` ("3D product rendering services"), `/3d-visualization` and `/contact?plan=…`. Those slugs follow the spec's page table. Rename `/contact-1` to `/contact` with a 301, and create the other pages, before publishing, or those links will 404.
