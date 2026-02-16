# MFoods QR Codes

Time-limited QR code gate for MATA restaurant waitlist.

## How it works

1. Open `generator.html` locally to create QR codes for each service (lunch/dinner)
2. QR codes point to this deployed gate page (`index.html`)
3. Gate page validates the time window using São Paulo time (America/Sao_Paulo)
4. If valid → redirects to the MATA waitlist
5. If expired → shows "code has expired" message

## Files

- `index.html` — Gate/validation page (deployed to Vercel)
- `generator.html` — QR code generator (used locally, not deployed)

## Time validation

All time checks use `Intl.DateTimeFormat` with `America/Sao_Paulo` timezone, so validation is based on Brasília time regardless of the user's phone timezone.
