# How to publish (and update) this site

The site is a finished static page in a local git repo. To put it online you create a
GitHub repo named **`mamo1016.github.io`**, push to it, and turn on Pages. ~5 minutes once.

> Your username `mamo1016` is baked into the URL. The repo name **must** be exactly
> `mamo1016.github.io` for the site to serve at `https://mamo1016.github.io/`.

---

## Step 1 — Create the empty repo on GitHub

1. Go to <https://github.com/new> (sign in as `mamo1016`).
2. **Repository name:** `mamo1016.github.io`
3. Visibility: **Public**.
4. **Do NOT** tick "Add a README", ".gitignore", or "license" — leave it empty, we already
   have files here.
5. Click **Create repository**.

## Step 2 — Push this folder to it

In a terminal in this folder
(`c:\Users\kanza\Projects\job hunt\portfolio\mamo1016.github.io`), run:

```bash
git remote add origin https://github.com/mamo1016/mamo1016.github.io.git
git push -u origin main
```

The first push asks you to authenticate. On Windows a browser window opens
(Git Credential Manager) — sign in to GitHub and approve. That's it; it's remembered after.

## Step 3 — Turn on GitHub Pages

For a `username.github.io` repo, Pages is usually on automatically. To confirm / set it:

1. On the repo page: **Settings → Pages** (left sidebar).
2. Under **Build and deployment → Source**, choose **Deploy from a branch**.
3. Branch: **`main`**, folder: **`/ (root)`**. Save.

## Step 4 — Visit the site

Wait ~1 minute, then open **<https://mamo1016.github.io/>**. (First build can take a couple
of minutes. A hard refresh — Ctrl+F5 — clears stale caches.)

---

## Updating the site later

Edit the files, then:

```bash
git add -A
git commit -m "Update portfolio"
git push
```

The live site refreshes within a minute.

## Add the demo clip

Record a short rviz2 GIF of the OpenArm doing its pick-and-place, save it as
`assets/demo.gif`, then commit and push (above). It replaces the placeholder automatically.
This is the single highest-impact addition — a recruiter watches the clip before reading
anything.

## Optional: custom domain (later)

If you buy a domain (e.g. `mamoru-ueda.com`, ~£10/yr), add it under **Settings → Pages →
Custom domain**, create the DNS records GitHub shows, and tick **Enforce HTTPS**. Not needed
to launch.

---

## Faster alternative (if you install the GitHub CLI)

If you install `gh` (<https://cli.github.com>), Steps 1–2 collapse to one command from this
folder:

```bash
gh auth login
gh repo create mamo1016.github.io --public --source=. --remote=origin --push
```

Then do Step 3.
