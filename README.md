# Cincinnati Area Hotel Hugo Website

This is a professional static Hugo website for an independent or medium-level hotel in the Cincinnati, Ohio area. It includes a responsive homepage, room, amenities, gallery, location, reviews, and contact pages, plus SEO metadata and Hotel schema.org structured data.

The project intentionally uses placeholders where exact hotel details are unknown. Replace those values before publishing.

## Local Development

```powershell
hugo server
```

## Build

```powershell
hugo
```

The generated static site will be in the `public/` folder.

## Cloudflare Pages

Use these settings:

- Framework preset: `Hugo`
- Build command: `hugo`
- Build output directory: `public`
- Hugo version: `0.160.1` or newer
- Environment variable, if needed: `HUGO_VERSION=0.160.1`

Cloudflare Pages should build the site from source. The generated `public/` folder is ignored and should not be committed.

## GitHub Push Instructions

After creating a GitHub repository, connect this local project with:

```powershell
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
git branch -M main
git push -u origin main
```

If the remote already exists, update it with:

```powershell
git remote set-url origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
git push -u origin main
```

## Replace These Placeholders

Most hotel facts live in `data/hotel.yaml`:

- `name`: hotel display name
- `legal_name`: legal or business name
- `phone` and `phone_href`: visible phone number and `tel:` link
- `email` and `email_href`: visible hotel email address and `mailto:` link
- `address`: street, city, state, ZIP, country
- `directions_url`: Google Maps directions link
- `booking_url`: Expedia, Hotels.com, or official booking link
- `maps_embed_url`: Google Maps iframe URL
- `facebook_url`, `instagram_url`, `linkedin_url`: real social profile links
- `amenities`: verified amenities only
- `room_highlights`: verified room details only

Page-specific text is in `content/`:

- `content/rooms.md`
- `content/amenities.md`
- `content/gallery.md`
- `content/location.md`
- `content/reviews.md`
- `content/contact.md`

## Photos

The first version uses visual placeholders. Replace them with real, property-owned hotel photos before launch. Good starting images include:

- Exterior
- Lobby
- Guest rooms
- Bathrooms
- Breakfast or common areas, if verified
- Business, fitness, pool, or other amenities only if available
- Nearby Cincinnati or Mason points of interest, if relevant

To add real images, place files in `static/images/` and update the templates or page markdown to use them.

## Google Maps

Replace the map placeholder in `content/location.md` or the homepage location section with the verified Google Maps embed iframe. Also update `directions_url` in `data/hotel.yaml`.

## SEO Notes

The site includes:

- Per-page title tags and meta descriptions
- Open Graph tags
- Hotel schema.org structured data
- `robots.txt` through Hugo
- `sitemap.xml` through Hugo
- Natural Cincinnati, Ohio, Mason, and nearby attraction language

Before publishing, remove or replace every `[PLACEHOLDER ...]` value. Search the project for `[PLACEHOLDER` to find remaining items.

## License

This project is licensed under the MIT License. See `LICENSE`.
