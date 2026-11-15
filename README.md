# Email signature images

Images used by the Skillup MENA email signature. The signature HTML links to these files, so
they have to stay at the same addresses for as long as emails that use them exist.

- `2027/` holds the images of the 2027 design. A new design gets a new folder, so older
  emails keep showing their own images.
- The folder is published on Cloudflare with `npx wrangler deploy` (settings in
  `wrangler.jsonc`, cache headers in `_headers`).
