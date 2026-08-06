# Volunteer Mobile Auto Care website

Official multi-page website for Volunteer Mobile Auto Care, built for Cloudflare Pages.

## Pages

- Home
- Services
- Pricing
- About
- Fleet service
- Referral rewards and launch specials
- Contact and service request
- Privacy notice
- Branded 404 page

## Features

- Responsive mobile-first layout
- Click-to-call and click-to-text actions
- Search-engine files (`robots.txt` and `sitemap.xml`)
- Web app manifest and branded icons
- Cloudflare Pages Function for contact-form email
- Security headers and caching rules
- Proprietary license, Git ignore rules, and editor settings

## Local preview

```bash
python -m http.server 8000
```

Open `http://localhost:8000`. The contact form requires Cloudflare Pages and environment variables.

## Deploy with GitHub and Cloudflare Pages

1. Create an empty GitHub repository.
2. Clone it or open it with GitHub Desktop.
3. Copy this project into the repository.
4. Commit and push the files.
5. In Cloudflare, open **Workers & Pages** and create a Pages project connected to the GitHub repository.
6. Framework preset: **None**.
7. Build command: leave blank.
8. Build output directory: `.`
9. Deploy and attach the custom domain.

## Contact form setup

The form uses the Resend email API. Verify a sending domain in Resend, then add these production environment variables in Cloudflare Pages:

- `RESEND_API_KEY`
- `CONTACT_TO_EMAIL`
- `CONTACT_FROM_EMAIL`

Use `.env.example` only as a reference. Never commit real API keys. Redeploy after adding variables.

## Before launch

- Confirm the final domain and update canonical URLs in the HTML, `robots.txt`, and `sitemap.xml` if it is not `https://volunteermobileautocare.com`.
- Add the real Facebook page link.
- Confirm final service areas, prices, discount eligibility, giveaway rules, and warranty terms.
- Have the privacy notice reviewed for the business's final data practices.
- Test the form on desktop and mobile.

## License

Proprietary. See `LICENSE`.
