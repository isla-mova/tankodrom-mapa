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

## Open: Vercel did not deploy the redirect (checked 27 Oct 2026)

- Vercel project `tankodrom-mapa` (id `prj_tq1zCEk11ajY0lh994MhWAB4fLa1`) is in Ivona's personal team `isla-movas-projects` (CLI login `isla-mova`), linked to `isla-mova/tankodrom-mapa`, branch `main`. That link is correct.
- Cause: the Vercel GitHub app on `isla-mova` (github.com/settings/installations/82435583) is set to "Only select repositories" and listed only `tankodrom-prototype`, so pushes here (`b72dff7`) never reached Vercel. Last auto-deploy was `b48d3c3` (7 Sep). Ivona added `tankodrom-mapa` on 27 Oct 2026.
- Not a problem: the personal Vercel project `tankodrom-prototype` has no Git link on purpose (since 22 Oct the website deploys from the company project, see the website's CLAUDE.md). The live website map matched the repo on 27 Oct.

To do:

1. Push (e.g. the pending CLAUDE.md commit) so Vercel deploys this repo. Missed pushes are not replayed.
2. Check: `https://tankodrom-mapa.vercel.app/` and `/?lang=en` land on the new map (English for the second); `/og.jpg` still 200.

Once resolved, replace this section with the final state.
