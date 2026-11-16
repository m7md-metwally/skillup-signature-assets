# Email signature images

Images used by the Skillup MENA email signature. The signature HTML links to these files, so
they have to stay at the same addresses for as long as emails that use them exist.

- `2027/` holds the images of the 2027 design. A new design gets a new folder, so older
  emails keep showing their own images.
- A file is never replaced once emails use it. Mail apps keep their copy of an image for a
  week (see `_headers`), so a replaced file would show up late and unevenly. A changed image
  goes into a new sub-folder instead, and the signature is pointed at it:
  - `2027/` first build.
  - `2027/v2/` same pictures, with their pixel density stored in the file. Classic Outlook
    needs it to give the header its right height.
  - `2027/v3/` the header with a larger badge (108px instead of 90px), so that it reads on
    phones. The other pictures are the same as in v2. This is the folder the signature uses.
    `header-desktop-left.png` and `header-desktop-left-wide.png` were added later: two
    other arrangements of the same header, with the badge on the left, to compare with the
    centred one. Adding a file does not change the ones already there.
- The folder is published on Cloudflare with `npx wrangler deploy` (settings in
  `wrangler.jsonc`, cache headers in `_headers`).
