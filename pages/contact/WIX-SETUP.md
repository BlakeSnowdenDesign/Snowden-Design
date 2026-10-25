# Contact page: Wix setup

## Page structure (Wix Studio)
1. Native site header.
2. **Embed HTML**, full width: paste `snowden-contact.html`. Height: **1,720 px** desktop, **2,050 px** tablet, **2,520 px** phone. It ends with a "The form is just below" panel.
3. **Native Wix Form** (Add > Contact & Forms), placed directly under the embed, inside a section with background `#FAFCFC` and a content width of about 1,240 px.
4. Native site footer.

## Native form spec
| Field | Type | Required |
| --- | --- | --- |
| Name | Short text | Yes |
| Email | Email | Yes |
| Phone | Phone | No |
| Project type | Dropdown: Web design and development; Branding, graphics and 3D; Video; SEO and GEO; Marketing and lead generation; Something else | Yes |
| Tell me about the project | Long text, placeholder "A few lines is plenty" | Yes |

- **Submit button:** "Start the conversation". Pill shape, fill Midnight Ink `#0A1D26`, white Satoshi Bold text, hover fill Studio Teal `#16B3A6`, height at least 48 px.
- **Success message:** "Thanks. I'll be in touch."
- **Fields:** Mist `#EEF3F4` fill, 1.5 px border `rgba(10,29,38,.12)`, 20 px corner radius, Satoshi 16 px, focus border Studio Teal. Field labels: Satoshi Bold 12 px, uppercase, letter spacing 0.14em, Slate `#4A5F68`.
- **Notifications:** send submissions to blake@snowden-design.com (Form settings > Notifications).
- Under the button, add a native text line: "Prefer email or phone? blake@snowden-design.com / 720.340.2611", with both items linked (mailto: and tel:+17203402611).

## SEO settings
- **URL slug:** keep `/contact-1` so existing links keep working, or change it to `/contact` and add a 301 redirect from `/contact-1`.
- **Title tag:** Contact Snowden Design | Hire a Web Designer in Denver
- **Meta description:** Start a project with Snowden Design in Denver, Colorado. Web design and development, video, branding and digital marketing. Email blake@snowden-design.com or call 720.340.2611.
- **Open Graph:** same title and description.

## Structured data
```json
{
  "@context": "https://schema.org",
  "@type": "ContactPage",
  "url": "https://www.snowden-design.com/contact-1",
  "about": {
    "@type": "ProfessionalService",
    "name": "Snowden Design",
    "url": "https://www.snowden-design.com",
    "email": "blake@snowden-design.com",
    "telephone": "+1-720-340-2611",
    "areaServed": "Denver, Colorado",
    "address": { "@type": "PostalAddress", "addressLocality": "Denver", "addressRegion": "CO", "addressCountry": "US" }
  }
}
```
