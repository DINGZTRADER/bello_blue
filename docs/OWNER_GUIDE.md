# Bello & Blue Events — Owner Update Guide

## Live website
https://bello-blue-events.vercel.app

## Main contact used by the website
0777 680 861

## Easiest image update workflow
The site uses fixed image filenames. Replace the file, keep the same filename, then deploy the updated `main` branch.

- `assets/logo.webp` — Bello & Blue logo
- `assets/hero-event.webp` — homepage hero/event setup
- `assets/equipment-board.webp` — equipment-hire catalogue image
- `assets/tablescape.webp` — premium styling/tablescape image

### Image rules
- Use WebP.
- Keep photographs sharp but lightweight; aim for roughly 100–300 KB when practical.
- Do not stretch images to a different aspect ratio.
- Keep the exact filename when replacing an existing slot.
- Check the mobile version after every replacement.

## Updating text
Primary website copy is in `index.html`.

Before changing text, search for the existing sentence or heading and edit only that section. Do not remove element IDs such as `#quote`, `#services`, `#hire`, or `#start`; the navigation and conversion flow depend on them.

## Updating the phone / WhatsApp number
The current international WhatsApp number is `256777680861` and the display number is `0777 680 861`.

If the number changes, update every occurrence in:
- `index.html`
- `app.js`
- structured data / metadata in `index.html`

Then test:
- Call buttons
- WhatsApp buttons
- Structured quote submission

## Publishing an update
The current Vercel deployment history does not contain Git-trigger metadata. Treat production deployment as manual until Vercel Git integration is explicitly connected.

After changing GitHub `main`:
1. Verify the changed files in GitHub.
2. Deploy the repository state to the existing Vercel project `bello-blue-events`.
3. Confirm `https://bello-blue-events.vercel.app` returns HTTP 200.
4. Test the homepage, WhatsApp enquiry, phone link, `robots.txt`, and `sitemap.xml`.

## Safe rollback
Vercel keeps previous production deployments. If an update breaks the site, restore the last known good production deployment rather than editing live files under pressure.

## Do not store credentials in this repository
Vercel passwords, domain registrar passwords, email passwords, API keys and recovery codes must stay in the account owner's password manager, never in GitHub files.