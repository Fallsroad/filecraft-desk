# FileCraft Desk site: publish steps

One-page site, a single self-contained file (`index.html`, inline CSS, no
external assets, no images). Built desk-side only. Nothing in this folder
has been pushed anywhere. Publishing waits on Sean's GitHub approval card;
every GitHub write prompts his approval.

## Before publishing (quick checks)

1. Proof slots: DONE November 21, 2026. Both slots in the "Check the
   work yourself" section are filled with the full text of
   `community/owned-site-post-1.md` and `community/owned-site-post-2.md`
   (page copy only; the internal QA notes at the end of those files are
   not on the page). The placeholder paragraphs and slot comments are
   removed.
2. Legiit link: no direct Legiit profile URL is recorded in the desk
   files, so the Order section links to https://legiit.com for now. When
   the direct profile link is known (it works even while services are
   hidden from Legiit browsing), swap that one href.

## Publish on GitHub Pages

1. Create the repo: on github.com, signed in as **Fallsroad**, create a
   new public repository named **filecraft-desk**. No README, no license,
   no .gitignore (keep it empty so the push is clean).
2. Push this folder's contents so `index.html` sits at the repo root
   (the README can go too; Pages serves `index.html` regardless):

   ```
   cd ~/workspace/venture-studio/businesses/filecraft-desk/site
   git init
   git add index.html README.md
   git commit -m "FileCraft Desk one-page site"
   git branch -M main
   git remote add origin https://github.com/Fallsroad/filecraft-desk.git
   git push -u origin main
   ```

   Each write step goes through Sean's approval card, as with all
   studio GitHub writes.

3. Turn on Pages: in the repo, Settings, then Pages. Under "Build and
   deployment", source is "Deploy from a branch"; branch is **main**,
   folder is **/ (root)**. Save.
4. Live URL, usually within a few minutes:
   **https://fallsroad.github.io/filecraft-desk/**
   Open it and check: headline renders whole, service rows and prices
   line up, the three marketplace links work.

## Later, only if Sean rules it

- Custom domain: the desk domain filecraftdesk.com was available and
  Sean deferred buying it. If bought and pointed at Pages later, add a
  `CNAME` file containing the domain and set the custom domain in the
  same Pages settings screen.
- After the site is live, the basics ride along per studio rule: submit
  the URL to Google Search Console and confirm the page is indexed.
