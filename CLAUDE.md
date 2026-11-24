# Namanga Secondary School website (repo `massawes/namanga`): notes for every Claude session

Claude does not remember old chats: **this file is the memory**. Update "WHERE WE STOPPED" after each piece of work,
so the owner can continue from any terminal. The owner writes Swahili: reply in short, simple Swahili.

## What it is
- Public school website + learning resource centre (notes, summaries, past papers, practicals, software, gallery,
  student task uploads, admin panel `/admin/`). Plain PHP + MySQL. Full description: `README.md`.
- Live: https://namangawebsite.freepage.cc (InfinityFree). Branch **master**.
- Sister repo `massawes/barakanamanga` is a newer copy of the same site (Docker, AI assistant, last work 2026-11-17).
  Before working, ask the owner which of the two repos is the live one.
- Other Namanga projects: namanga-ssms, namanga-form1 (VPS 185.205.209.83), namanga-results, namanga-files
  (Android app files), namanga-keepalive (Supabase ping). Each has its own CLAUDE.md.

## SYNC RULE (owner 2026-11-24): local = GitHub = live
- Local folder: `C:\xampp\htdocs\namanga` (clone with `GIT_LFS_SKIP_SMUDGE=1 git clone git@github.com:massawes/namanga.git`;
  the repo is big, ~1.7 GB, because of uploads/). `git pull` before starting.
- Every push to master runs `.github/workflows/deploy.yml`: builds `config/env.php` from GitHub secrets/vars and uploads
  by FTP to InfinityFree `htdocs/`. So: commit -> push -> watch the run (`gh run watch`) -> check the live page.
- Files in the deploy `exclude:` list never go to the website (README.md, CLAUDE.md, database/**, .github/**, ...).
- Commits that only change notes: add `[skip ci]` to the message so no deploy runs.

## WHERE WE STOPPED
- 2026-11-24: CLAUDE.md added (and excluded from the FTP deploy). No code change.
