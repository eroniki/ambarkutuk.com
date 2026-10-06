# ambarkutuk.com

Landing page for the Ambarkutuks. Plain static HTML, no build step.

- `public/` is everything that gets served. `_headers` sets the security headers.
- `wrangler.jsonc` makes this a Cloudflare Worker with static assets (`public/` is the asset directory).
- Murat's site lives at murat.ambarkutuk.com and Zeynep's at zeynep.ambarkutuk.com, each in its own repo.

Deploy: connect this repo to the `ambarkutuk-com` Worker in Cloudflare (Workers & Pages, Settings, Builds),
production branch `main`, deploy command `npx wrangler deploy`. Every push to `main` publishes.
The custom domain is attached in the Worker's Settings, Domains & Routes, only at DNS cutover.
