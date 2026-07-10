# denisbaciu.com

The permanent, canonical home for Denis Baciu's writing and projects.
Plain HTML, one stylesheet, zero dependencies, no build step.

## Philosophy (three rules)

1. **This site is canonical.** Anything published elsewhere gets a copy
   here with a provenance block. Platforms are syndication, not storage.
2. **Zero dependencies.** No framework, no JS, no external fonts, no CDN.
   Nothing here can be broken by someone else's deprecation notice.
3. **Git is the archive.** The repository history is the audit trail.
   The host is a commodity; the domain is the identity. Only the domain
   is irreplaceable — keep auto-renew on, registered to you personally,
   at a registrar independent of the host.

## Deploy in ~20 minutes (GitHub Pages)

1. Create a GitHub repository (public or private) — e.g. `denisbaciu.com`.
2. Push this folder to it:
   ```
   git init && git add -A && git commit -m "Genesis"
   git branch -M main
   git remote add origin git@github.com:YOURUSER/denisbaciu.com.git
   git push -u origin main
   ```
3. Repo → **Settings → Pages** → Source: *Deploy from a branch* →
   Branch: `main`, folder `/ (root)`.
4. Still in Pages settings, set **Custom domain**: `denisbaciu.com`
   (the `CNAME` file in this repo keeps it pinned).
5. In **Porkbun** → your domain → **DNS records**, delete the parking
   records and add:

   | Type  | Host | Answer                  |
   |-------|------|-------------------------|
   | A     | (blank / @) | 185.199.108.153  |
   | A     | (blank / @) | 185.199.109.153  |
   | A     | (blank / @) | 185.199.110.153  |
   | A     | (blank / @) | 185.199.111.153  |
   | CNAME | www  | YOURUSER.github.io      |

6. Back in GitHub Pages settings, tick **Enforce HTTPS** once the
   certificate is issued (can take up to an hour after DNS propagates).

Done. Every future update is `git push`.

### Alternative hosts (same files, zero changes)

Cloudflare Pages or Netlify both deploy this folder as-is. That's the
point: if the host annoys you, moving is an afternoon, and nothing about
the site changes. The URLs must never change — cool URIs don't.

## Email

Porkbun includes free email forwarding: domain → **Email Forwarding** →
forward `hello@denisbaciu.com` to your real inbox. Do this before
deploying the About page, or swap the address there.

## Adding a post

1. Copy `writing/_template-imported.html` (imports) or the shape of
   `writing/2026-07-boring-on-purpose.html` (new writing) to
   `writing/YYYY-MM-slug.html`.
2. Fill in the provenance block.
3. Add one row to `writing/index.html` under the right year, and update
   the "Latest writing" row on `index.html`.
4. Commit with a plain message. Push.

## Importing your history

See `MIGRATION.md` — per-platform export instructions and the
provenance convention.

## When you outgrow this

If the archive passes ~30 posts and hand-editing the index annoys you,
graduate to a static generator (Eleventy is the closest spirit). Rules
for the migration: keep every URL identical, keep the provenance
blocks, keep zero client-side dependencies. The git history carries
everything forward.

## Pre-publish checklist

- [ ] Every `<!-- EDIT -->` comment resolved and deleted
- [ ] Employer-related wording checked against your contract /
      outside-interests policy (nothing beyond your public CV)
- [ ] Email forwarding live
- [ ] Domain auto-renew ON, personal card, personal account
