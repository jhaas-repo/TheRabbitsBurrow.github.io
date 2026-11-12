# Publish to GitHub Pages

Repo: **TheRabbitsBurrow.github.io**  
Site URL (after publish): **https://therabbitsburrow.github.io/**

## Site map

| Path | URL |
|------|-----|
| Home | `https://therabbitsburrow.github.io/` |
| WID project | `https://therabbitsburrow.github.io/wid/` |
| WID Privacy Policy | `https://therabbitsburrow.github.io/wid/privacy.html` |
| WID Beta Tester Notes | `https://therabbitsburrow.github.io/wid/beta.html` |

Use the privacy URL in Google Play Console → App content → Privacy policy.

## Push these files to your repo

Copy everything inside this folder to the **root** of `TheRabbitsBurrow.github.io` (or clone and replace):

```
index.html
css/style.css
wid/index.html
wid/privacy.html
wid/logo.png
```

Example (from a machine with git):

```bash
git clone https://github.com/TheRabbitsBurrow/TheRabbitsBurrow.github.io.git
cd TheRabbitsBurrow.github.io
# copy the files above into this directory
git add .
git commit -m "Add home page and WID privacy policy"
git push origin main
```

If the default branch is `master`, use that instead of `main`.

## Enable Pages (if not already)

1. GitHub → repo **Settings** → **Pages**
2. Source: **Deploy from a branch**
3. Branch: `main` (or `master`), folder: **/ (root)**
4. Save — wait 1–2 minutes, then open the site URL

## Before go-live

1. In `wid/privacy.html`, replace **`[INSERT CONTACT EMAIL]`** with your real email (two places).
2. Optional: update the footer GitHub link if the org/user URL differs.

## Adding a new project later

1. Create a folder, e.g. `my-app/`
2. Add `my-app/index.html` (and `privacy.html` if needed)
3. Add a card on the home page `index.html` pointing to `my-app/`
4. Commit and push

## Play Store

Privacy policy link:

```
https://therabbitsburrow.github.io/wid/privacy.html
```
