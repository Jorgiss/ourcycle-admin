# OurCycle admin dashboard

Static page that calls the `adminStats` Cloud Function and renders
aggregate metrics for the OurCycle iOS app.

- **Endpoint**: `https://us-central1-ourcycle-b6b97.cloudfunctions.net/adminStats`
- **Auth**: `X-Admin-Token` header. Token entered client-side, stored
  in `localStorage`, never committed.
- **Live URL**: <https://admin.ourcycle.app/>
- **Privacy**: aggregate counts only - no per-user identifiers leave
  the function. See [ourcycle.app/privacy](https://www.ourcycle.app/privacy)
  section 6a.

The dashboard contains no secrets - it's a static HTML/CSS/JS file
that talks to a server-side, token-gated function. Safe to keep
public.
