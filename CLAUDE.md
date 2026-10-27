# tankodrom-mapa

Old address of the Tankodrom Milovice site map: https://tankodrom-mapa.vercel.app. The printed leaflet (`mapka.pdf`, QR code) links here, so it must stay online.

Since 26 Oct 2026 this project is only a **redirect** to the website's map, the single source of truth:
https://tankodrom-milovice.vercel.app/mapa/index.html (repo `~/Desktop/projects/tankodrom-prototype`, GitHub `isla-mova/tankodrom-prototype`, deployed by the company Vercel project `tankodrom-milovice`, files `public/mapa/index.html` and `public/mapa/data.js`). Change the map there, never here.

## Files

- `vercel.json`: redirects every path except `og.jpg` and `favicon.svg`. `permanent: false` (307) on purpose, because the destination will move to the real domain at launch. At launch, change `destination` only.
- `og.jpg`, `favicon.svg`: still served from here because the website's map uses `https://tankodrom-mapa.vercel.app/og.jpg` as its og:image. Do not delete them while that is so.
- `index.html`: the old map, no longer served (the redirect covers it). Can be deleted.
- `tankodrom-liberation/` and `tankodrom-liberation.zip`: Ivona's separate party quiz. Leave them alone, never stage them.
- No `package.json`: `npm run dev` does not exist. Plain static servers ignore `vercel.json`; to test the redirect locally use `vercel dev`.

## How to work with Ivona

- Ivona commits and pushes herself. Make the change, check it, propose the commit (files plus message). Never `git push`.
- Linux Mint. No em dashes, in replies or in texts. GPS in decimal degrees only.
- After every task, update this CLAUDE.md so it matches the new state (files, decisions, open items; resolved items replaced by their final state). Include it in the proposed commit.

## Hosting

- Vercel: company team **Tankodrom Milovice** (`tankodrom-milovice`, Pro), project `tankodrom-mapa` (id `prj_tq1zCEk11ajY0lh994MhWAB4fLa1`), moved from Ivona's personal team with "Transfer project" on 27 Oct 2026. Same project id, address `tankodrom-mapa.vercel.app` kept.
- Deploys from GitHub `isla-mova/tankodrom-mapa` (Ivona's own repo), branch `main`. Every push to `main` deploys.
- The Vercel GitHub app on `isla-mova` (github.com/settings/installations/82435583) uses "Only select repositories". This repo must stay on that list, or pushes stop deploying silently. It was missing until 27 Oct 2026.
- Checked 27 Oct 2026 after the transfer: `/` and `/?lang=en` give 307 to the website map (with `?lang=en` kept); `/og.jpg` and `/favicon.svg` give 200.

## Open (27 Oct 2026)

- Not yet proven: that a push deploys in the company team. Check after the next push (Deployments in the company project, or the Vercel status on the commit in GitHub).
- `isla-mova` was raised to **Member** in the company team for the transfer (it had been auto-added as Developer on 22 Oct by a Git push). This contradicts the website CLAUDE.md ("never add isla-mova back"). Ivona to decide: keep, or remove after turning off auto-adding of Git committers, then check that both projects still deploy.
