# tankodrom-mapa

Old address of the Tankodrom Milovice site map: https://tankodrom-mapa.vercel.app. The printed leaflet (`mapka.pdf`, QR code) links here, so it must stay online.

Since 26 Oct 2026 this project is only a **redirect** to the website's map, the single source of truth:
https://tankodrom-milovice.vercel.app/mapa/index.html (repo `~/projects/tankodrom-prototype`, files `public/mapa/index.html` and `public/mapa/data.js`). Change the map there, never here.

## Files

- `vercel.json`: redirects every path except `og.jpg` and `favicon.svg`. `permanent: false` (307) on purpose, because the destination will move to the real domain at launch. At launch, change `destination` only.
- `og.jpg`, `favicon.svg`: still served from here because the website's map uses `https://tankodrom-mapa.vercel.app/og.jpg` as its og:image. Do not delete them while that is so.
- `index.html`: the old map, no longer served (the redirect covers it). Can be deleted.
- `tankodrom-liberation/` and `tankodrom-liberation.zip`: Ivona's separate party quiz. Leave them alone, never stage them.
- No `package.json`: `npm run dev` does not exist. Plain static servers ignore `vercel.json`; to test the redirect locally use `vercel dev`.

## How to work with Ivona

- Ivona commits and pushes herself. Make the change, check it, propose the commit (files plus message). Never `git push`.
- Linux Mint. No em dashes, in replies or in texts. GPS in decimal degrees only.

## Open: GitHub / Vercel connection (check 27 Oct 2026)

Ivona suspects the project is connected to the wrong GitHub account.

What was true on 26 Oct 2026 evening:

- Remote: `https://github.com/isla-mova/tankodrom-mapa.git` (public, owner `isla-mova`). The website repo uses the same account (`isla-mova/tankodrom-prototype`).
- `gh auth status`: logged in as `isla-mova`. Git identity: Ivona Slamova, ivona.slamova@gmail.com (global `~/.gitconfig`).
- Commit `b72dff7` (the redirect) was pushed (`main` level with `origin/main`), **but the live site did not redirect**: `/`, `/?lang=en` and `/og.jpg` all returned 200. So Vercel likely did not deploy the push.
- No `.vercel/` folder here, so this folder is not linked to a Vercel project locally.

To check:

1. On vercel.com, find the project serving tankodrom-mapa.vercel.app. Settings, Git: which GitHub account and repo is it connected to? Is it `isla-mova/tankodrom-mapa`, branch `main`?
2. Deployments tab: is there a deployment for `b72dff7`? If not, the Git connection points elsewhere (another account or a fork) or is missing.
3. Which Vercel account/team owns the project, and is the Vercel GitHub app installed on the `isla-mova` account with access to this repo?
4. Fix the connection (or deploy once by hand with `vercel --prod` after `vercel link` to the right project), then check:
   - `https://tankodrom-mapa.vercel.app/` and `/?lang=en` land on the new map (English for the second).
   - `https://tankodrom-mapa.vercel.app/og.jpg` still shows the image.

Once resolved, replace this section with the final state.
