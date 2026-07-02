# Humanoids Now — Kickstarter-style campaign page

A single-file, self-contained campaign page (`index.html` + `assets/`) that mirrors a full
Kickstarter campaign layout: hero/video slot, funding sidebar (pledged / goal / backers / days /
progress bar / all-or-nothing), tabs (Campaign · Rewards · FAQ · Updates · Community), full story
with budget & roadmap, reward tiers, risks & challenges, creator bio. Built honestly from the real
open anatomy/physiology project (all imagery is our own real renders — no CGI of a robot that
doesn't exist yet, per Kickstarter's rules).

See `KICKSTARTER_REQUIREMENTS.md` for the exhaustive list of what Kickstarter requires and where each
item lives on the page.

## Edit before launch
- Campaign numbers: the `RAISED / GOAL / BACKERS / DAYS` variables at the bottom of `index.html`.
- Copy, rewards, budget: inline in `index.html`.
- Video: drop your MP4/embed into the hero `.media` block.
- Location / team details: the creator section.

## Preview locally
```bash
cd humanoids-now && python3 -m http.server 8090
# open http://localhost:8090
```

## Host on GitHub Pages
```bash
# 1) Create an empty PUBLIC repo named humanoids-now (you do this — repo creation is human-gated):
gh repo create humanoids-now --public --description "Humanoids Now campaign page"

# 2) Push just this folder as the site:
cd humanoids-now
git init -b main && git add -A && git commit -m "Humanoids Now campaign page"
git remote add origin https://github.com/Farwalker3/humanoids-now.git
git push -u origin main

# 3) Enable Pages (serves from main / root):
gh api -X POST repos/Farwalker3/humanoids-now/pages -f source[branch]=main -f source[path]=/ 2>/dev/null \
  || echo "If that errors, enable it in the repo: Settings → Pages → Branch: main /(root)"
```
Live at **https://farwalker3.github.io/humanoids-now/** (a minute after Pages builds).

## Use your custom domain (humanoids-now.kodair.us)
```bash
echo "humanoids-now.kodair.us" > CNAME && git add CNAME && git commit -m "custom domain" && git push
```
Then add a DNS **CNAME** record: `humanoids-now` → `farwalker3.github.io`, and set the custom domain
in Settings → Pages (enable "Enforce HTTPS").
