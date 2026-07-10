# MIGRATION — pulling your history into the archive

A public web search finds essentially nothing under "Denis Baciu",
"denisbaciu", or "baciudenis" (checked July 2026). So the real inventory
lives behind logins, in exports only you can trigger. Work through this
checklist once; most exports arrive by email within 24–72 hours.

## 1. Trigger the exports

| Platform | Where | What you get |
|---|---|---|
| **LinkedIn** | Settings & Privacy → Data privacy → *Get a copy of your data* → select Articles, Shares, Comments | CSV/HTML of every post & comment |
| **X / Twitter** | Settings → Your account → *Download an archive of your data* | Full archive incl. tweets.js |
| **Facebook / Instagram** | Accounts Center → Your information and permissions → *Download your information* → Posts | HTML/JSON archive |
| **Medium** | Settings → Security and apps → *Download your information* | Zip of every story & draft |
| **dev.to** | Settings → Account → *Export content* | Emailed zip |
| **Blogger / YouTube / old Google stuff** | takeout.google.com | Everything Google holds |
| **Reddit** | reddit.com/settings/data-request | Posts & comments CSV |
| **Stack Overflow** | Your profile → Answers/Questions (manual copy for the few that matter) | — |
| **GitHub** | Already git — repos *are* archived. Clone any gists: `git clone https://gist.github.com/ID` | — |

## 2. Sweep for dead things

- **Wayback Machine** (web.archive.org): search any old blog URLs,
  usernames, or defunct project domains you remember owning. Save what
  you find as HTML.
- **Old email**: search your inboxes for "published", "your post",
  "welcome to" — sign-up receipts are a map of forgotten accounts.
- **The harness**: your Claude Code sessions contain READMEs, design
  notes, and post-mortems. Export the good ones — they're writing too.

## 3. Triage (be ruthless)

For each item: **Archive** (worth keeping verbatim), or **Skip**
(small talk, memes, replies without standalone value). Don't polish.
An archive that edits its past isn't an archive. Expect the keep-pile
to be small — that's fine. The site's job is to catch everything from
today forward; history is a bonus.

## 4. Convert

One file per kept item, from `writing/_template-imported.html`:

- Filename: `YYYY-MM-short-slug.html` (original publish date)
- Provenance block, always:
  `source · original URL · originally published · imported · canonical copy`
- Text pasted **verbatim** — typos, dated opinions and all. If you must
  answer your past self, add a dated editor's note *below* the piece.
- One row in `writing/index.html` under the right year.

## 5. Going forward: publish here first

The POSSE rule — Publish on your Own Site, Syndicate Elsewhere:

1. New piece goes on denisbaciu.com first.
2. Then post it (or an excerpt) to LinkedIn / X / wherever the audience
   is, with a link back to the canonical copy.
3. The platforms get the reach; the archive keeps the record.

That's the whole system. Platforms come and go; the ledger stays.
