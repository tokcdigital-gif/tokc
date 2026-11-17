# TOKCONSULT website: WordPress-ready pages

One file per page. Each file contains everything that page needs: fonts, styles, header, page content, footer and logo (built in, so there's nothing to upload).

| File | WordPress page |
|---|---|
| home.html | https://tokconsult.com.ng/ |
| business-audit-advisory.html | /business-audit-advisory/ |
| market-launch-entry.html | /market-launch-entry/ |
| operations-structuring.html | /operations-structuring/ |
| growth-revenue.html | /growth-revenue/ |
| partner-plan.html | /partner-plan/ |
| shop.html | /shop/ |
| packages-and-bundles.html | /packages-and-bundles/ |
| about.html | /about/ |
| resources.html | /resources/ |
| blog.html | /blog/ |
| contact-us.html | /contact-us/ |
| free-health-check.html | /free-health-check/ |
| business-in-a-box.html | /business-in-a-box/ |
| privacy-policy.html | /privacy-policy/ |
| terms-of-service.html | /terms-of-service/ |
| refund-policy.html | /refund-policy/ |

## How to add a page

1. Open the page in WordPress and set its template to **full width / no sidebar**. (Elementor: "Elementor Canvas". Most themes: "Full Width" or "Blank".)
2. Add **one Custom HTML block** (block editor) or **one HTML widget** (Elementor).
3. Open the file in Notepad or TextEdit, select all, copy, and paste into that block.
4. Update and view the live page.

**Don't** paste into the Classic editor's Visual tab. It adds extra paragraphs and breaks the layout.

## Footer

Each file contains the page content plus the TOKCONSULT footer and floating WhatsApp button. There's no header: your site's own menu handles navigation. If your theme already shows a footer, delete the part between the `FOOTER START` and `FOOTER END` comments so it doesn't appear twice.

## Why text now shows properly

The styles are locked to the TOKCONSULT content (everything sits inside `id="tok-site"`), and every colour, font and weight is set with `!important`. So the theme can no longer:

- turn headings dark on dark backgrounds (the hidden "Build a business that…" problem)
- remove bold from headings, prices, labels or `<strong>` text
- change fonts, make headings uppercase, or underline buttons

Every page was tested inside a deliberately hostile theme that forces dark, thin, uppercase headings and un-bolds all bold text. Every page passed on desktop and phone, with no hidden text and no lost bold.

## Free Health Check page

`free-health-check.html` contains the navy header plus the shortcode `[tok_health_check]`. The Health Check plugin must be installed and active.

- **Block editor:** shortcodes run inside the Custom HTML block, so pasting the file is enough.
- **Elementor:** the HTML widget doesn't run shortcodes. Paste the file into an HTML widget, delete the `[tok_health_check]` line, and add a **Shortcode** widget underneath containing `[tok_health_check]`.

## Images

The Shop product covers, the Resources guide thumbnails and the Business in a Box mock-up load from your Media Library (`/wp-content/uploads/2026/11/`). If you ever rename or re-upload one, keep the same file name or the image will disappear.

## Things still to connect

- **Social icons** in the footer: currently `#`.

## Legal pages

Create three pages with exactly these addresses: `/privacy-policy/`, `/terms-of-service/` and `/refund-policy/`. The footer, the Health Check consent box and the Contact form already link to them.

To change a link, search the file for the `#…` text above (Ctrl+F) and paste the real link in its place.

## Caching

If a page still looks old after pasting, clear your cache plugin (LiteSpeed, WP Rocket, etc.) and any Cloudflare cache, then reload.

## Blog page

1. Install and activate the **TOKCONSULT Blog** plugin (tok-blog.zip): Plugins → Add New → Upload Plugin.
2. Create a page called **Blog** with the address `/blog/`, full-width template, and paste `blog.html` into one Custom HTML block.
   - **Elementor:** paste `blog.html` into an HTML widget, delete the `[tok_blog]` line, and add a **Shortcode** widget in its place containing `[tok_blog]`.
3. Do **not** set this page as the "Posts page" under Settings → Reading. Leave that empty; the plugin lists the posts itself.
4. Publish posts as normal (Posts → Add New). Give each one a **featured image** (1600×1000 works best) and **one category** (e.g. Launch, Operations, Growth, Audit). New posts appear on the Blog page automatically, newest first.

Optional: `[tok_blog_latest count="3"]` shows the three newest posts on any other page (e.g. Home or Resources).

## Contact form and email sign-ups

Install the **TOKCONSULT Forms** plugin (tok-forms.zip). The forms on Contact, Resources and Blog then work as soon as the pages are pasted: each message is emailed to info@tokconsult.com.ng and saved under **Forms** in your dashboard (with CSV export). Install WP Mail SMTP so the emails don't land in spam.
