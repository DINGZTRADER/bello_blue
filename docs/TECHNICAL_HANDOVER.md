# Bello & Blue Events — Technical Handover

## Production
- Live URL: `https://bello-blue-events.vercel.app`
- Vercel project: `bello-blue-events`
- Vercel project ID: `prj_xxEZ8eGtdfzdaoTungXFsb32DkqA`
- Repository: `DINGZTRADER/bello_blue`
- Default branch: `main`
- Current stack: static HTML + CSS + vanilla JavaScript on Vercel
- Backend/database: none

## Production architecture
The site is intentionally lightweight. All public pages are static. Quotations are generated client-side and sent through WhatsApp to `+256 777 680 861`.

Core files:
- `index.html` — content, SEO metadata, structured data and page structure
- `styles.css` — responsive design
- `app.js` — enquiry logic, WhatsApp message generation and analytics event hooks
- `vercel.json` — security headers and platform configuration
- `robots.txt` — crawler policy
- `sitemap.xml` — search-engine sitemap
- `assets/` — optimized Bello & Blue brand imagery

## Security baseline
Production is configured with:
- HTTPS / HSTS
- Content-Security-Policy
- X-Content-Type-Options
- X-Frame-Options
- Referrer-Policy
- Permissions-Policy

## SEO baseline
Configured:
- index/follow robots metadata
- canonical URL
- meta description
- Open Graph metadata
- Twitter/X social preview metadata
- Organization structured data
- `robots.txt`
- `sitemap.xml`

## Analytics
The front end contains Vercel Analytics event hooks for calls, WhatsApp clicks and quote submissions. Vercel Web Analytics must be enabled at the Vercel project/account level before analytics data is available.

## Domain
The canonical URL currently uses the Vercel domain. When Bello & Blue obtains or supplies its production domain:
1. Attach the domain to the existing Vercel project.
2. Replace the canonical URL in `index.html`.
3. Replace `og:url` and structured-data URL.
4. Update `robots.txt` sitemap URL.
5. Update URLs inside `sitemap.xml`.
6. Verify HTTPS and redirects.

## Deployment model
Current deployment records show no Git source metadata. Do not assume GitHub commits automatically deploy. Continue explicit production deployment until Git integration is intentionally configured.

## Rollback
Previous Vercel production deployments are available as rollback candidates. Always verify the production alias after a rollback.

## Release acceptance checks
A release is complete only when all of the following pass:
- homepage HTTP 200
- responsive layout on phone and desktop
- call link launches the dialer
- WhatsApp buttons target `256777680861`
- quote form generates a structured message
- hero and equipment images load
- `/robots.txt` HTTP 200
- `/sitemap.xml` HTTP 200
- production deployment state READY
- production alias has no alias error