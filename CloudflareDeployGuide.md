# Deploy The Children of War Project to Cloudflare Pages (free)

**What you upload to Cloudflare is your website files — the HTML — not a Markdown file.** Everything you need is in the **`cow-site`** folder (also provided as `cow-site.zip`):

- `index.html` — the homepage (this file name must stay exactly as-is)
- `legal.html` — the Terms & Parental Consent page
- `certificate.html` — the Change Maker certificate maker

Each file is fully self-contained (logo, photos, and fonts are built in), so there are no other files or folders to manage.

---

## Step 1 — Create a free Cloudflare account
Go to **dash.cloudflare.com** and sign up (the Pages plan is free).

## Step 2 — Create a Pages project and upload
1. In the dashboard, open **Workers & Pages → Create → Pages → Upload assets** (this is the "Direct Upload" option — no coding or GitHub needed).
2. Give it a project name, e.g. **children-of-war**.
3. **Drag the `cow-site` folder** (unzip `cow-site.zip` first) into the upload area, or click to select the three files. Make sure **`index.html` sits at the top level** (not inside another sub-folder).
4. Click **Deploy**. In about 30 seconds you'll get a live preview URL like `children-of-war.pages.dev` — open it to confirm the site looks right.

## Step 3 — Connect your GoDaddy domain
1. In your Pages project, go to **Custom domains → Set up a domain** and enter your domain (e.g. `www.childrenofwarproject.org`).
2. Cloudflare will give you a **DNS record** to add. Easiest path:
   - In GoDaddy: **My Products → your domain → DNS → Add**, and add the **CNAME** record exactly as Cloudflare shows (name/host and the `…pages.dev` target).
   - *(Alternative, fuller option: change your domain's nameservers to Cloudflare — Cloudflare walks you through this and then manages DNS for you.)*
3. Wait for it to verify (usually minutes, sometimes a few hours). Your site is then live on your own domain with **free HTTPS**.

## Updating the site later
Edit the file(s) and re-upload the folder to the **same** Pages project (**Create new deployment → Upload**). Cloudflare swaps the new version in automatically. Just send me your changes and I'll hand you back updated files to re-upload.

---

## Before you go fully live — quick checklist
Open `index.html` and edit the small **SITE settings** block at the very top:

- **`donateURL`** — paste your **Zeffy** donation-page link so every Donate button works.
- **`formEndpoint`** — paste your **Formspree** endpoint so Change Maker sign-ups email you (leave blank to keep it in preview mode for now).
- **`email`** — your real contact email.
- **`raisedSoFar`** — update this number as donations come in; the dashboard gauge and "to go" figure update automatically.
- **`changeMakers`** — add a line per person to fill the Change Maker Wall.

Keep the three file names exactly as they are (`index.html`, `legal.html`, `certificate.html`) so the footer's Terms link and the certificate link keep working.

*(If you ever choose GoDaddy's Airo builder instead, that's a different route — use the `CoW-Website-Content-Pack-for-Airo.md` file for that, not these HTML files.)*
