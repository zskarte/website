# ZS-Karte website

This repository publishes the public website at `https://zskarte.ch` through
GitHub Pages from `main`, directory `/`. Its `CNAME` is `zskarte.ch`; with the
matching DNS records, GitHub redirects `www.zskarte.ch` to the apex domain.

The production application is hosted separately at `https://app.zskarte.ch`.
Login and guest links point there. `404.html` preserves old app links for
`/login`, `/operations`, `/main`, `/map`, `/share` and `/help`, including their query
strings and fragments. Other missing paths remain a normal 404 page. GitHub
serves these redirects with HTTP 404 before the browser navigates to the app.
The legacy printed-map path `/map` is normalized to `/main/map`.

For the production domain binding, DNS records and verification sequence, see
the [production domain cutover in zskarte/zskarte](https://github.com/zskarte/zskarte/blob/main/docs/production-domain-cutover.md).

Publish the domain switch only after `app.zskarte.ch` serves the app with valid
HTTPS. Changes to Pages settings and **Enforce HTTPS** require a repository
administrator. No Azure deployment or API changes are needed to publish this
website.
