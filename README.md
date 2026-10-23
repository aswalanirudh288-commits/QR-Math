# QR Code Mathematics Model — website

Node + Express backend, SQLite (local) or Postgres (deployed), single-page frontend.

## Run locally
    npm install
    ADMIN_PASSWORD=yourpassword npm start      # http://localhost:3000
Admin dashboard: /admin.html

## Deploy on Render (free)
1. Push this folder to a new GitHub repo.
2. render.com → New → PostgreSQL (free). Copy its **Internal Database URL**.
3. New → Web Service → pick the repo. Build: `npm install`. Start: `npm start`.
4. Environment variables:
   - `ADMIN_PASSWORD` = your password
   - `DATABASE_URL` = the Postgres URL
5. Name the service something very short, e.g. `qrmath` → https://qrmath.onrender.com

## Short URL for the QR code
Version 2 (25×25) holds ~26 characters at level M, ~20 at Q, ~14 at H.
`https://qrmath.onrender.com` is 27 characters, so use level L (32) or a shorter name / custom domain.
Generate the pattern at qr-code-generator.com or any generator, choosing Version 2 and the lowest level that fits,
then copy the 25×25 grid onto the thermocol. Scan it before building!
