# Quest ID cards

A single-page tool that turns a photo, name, designation, employee ID, mobile number and optional blood group into a printable Quest employee ID card. Everything runs in the browser — no server, no data leaves the machine.

## Putting it on GitHub Pages

1. Create a repository, e.g. `id-cards`.
2. Add `index.html` at the root.
3. Create a folder called `assets` and put two files in it:
   - `assets/logo.png` — the Quest logo, ideally with a transparent background
   - `assets/signature.png` — the scanned authorised signature
   Both load automatically, so nobody has to upload them each time. If they're missing, the tool falls back to manual upload.
4. Settings → Pages → Source: **Deploy from a branch**, branch `main`, folder `/ (root)`.
5. The site appears at `https://<username>.github.io/id-cards/` in a minute or two.

## Output

- **Download PNG** renders the card at 3× (about 2100 × 3000 px) — good for printing or sharing.
- **Print card** opens the browser print dialog sized to 74 × 105 mm. Choose "Save as PDF" for a print-shop file.

## Changing the fixed details

Company name, address, office number and website are editable in the form and printed on every card. To change the defaults permanently, edit the `value` attributes in the "Company details" section of `index.html`.

## Card size

The card is drawn on a 712 × 1013 px canvas and printed at 74 × 105 mm (A7). To use a different size, change the `@page size` rule and the `.scaler` scale factor in the print stylesheet.
