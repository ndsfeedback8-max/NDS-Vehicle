# Vehicle Running Chart

A single-page mobile app for logging vehicle trips and fuelling, with automatic
distance and fuel-average calculations, a monthly report, and per-vehicle QR
codes for quick entry.

It's a single static HTML file — no build step, no server, no dependencies to
install. All data is stored in the browser's `localStorage`, on the device
that's using it.

## Features
- **Trips**: date, vehicle, from/to, reason, start/end mileage → auto distance
- **Fuel**: odometer reading, litres, amount paid → auto fuel average (km/l)
  based on the previous fill for that vehicle
- **Settings**: add vehicles and locations, with autocomplete everywhere else;
  generate a QR code per vehicle (stick it on the dashboard — scanning it
  opens the app with that vehicle already selected)
- **Report**: pick a month (and optionally a vehicle) for totals, per-vehicle
  breakdown, and full trip/fuel tables, with a print/PDF button

## Deploying with GitHub Pages
1. Create a new GitHub repository and upload `index.html` (and this
   `README.md` if you like) to it.
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to `Deploy from a branch`,
   pick the `main` branch and the `/ (root)` folder, then **Save**.
4. GitHub will publish the site at `https://<your-username>.github.io/<repo-name>/`
   within a minute or two. That URL is what you scan the vehicle QR codes
   against — generate them from the app's Settings tab *after* it's live at
   its permanent URL, so the codes don't change later.

## Notes
- Data lives only in the browser it was entered on — it won't sync between
  a phone and a laptop. Each device builds up its own log.
- Everything runs client-side; no backend or database is required.
