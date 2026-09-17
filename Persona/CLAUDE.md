# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

A single static HTML "business card" page (`index.html`) about one person (Оля, a logistician in Grodno). There is no build system, package manager, linter, or test suite — it's a plain HTML file with inline `<style>`, opened directly in a browser. There are no commands to run; editing `index.html` and opening it in a browser is the whole workflow.

## Structure

- `index.html` — the entire site: hero section, "about", "work", photo gallery, "facts", and finale/quote sections, all styled via inline `<style>` in the `<head>`. Section order and content are hand-written directly into the HTML, not templated or generated.
- `про-меня.md`, `проекты.md`, `факты.md`, `profile.md` — Russian-language source notes (bio, work, personality facts, and a consolidated profile) that the prose in `index.html` is drawn from. When updating bio/personality/work text, treat these `.md` files as the source of truth and update `index.html` to match — there is no automated sync between them.
- `images/` — photos referenced by `index.html`. `images/CREDITS.md` is a stale license-attribution template left over from an earlier placeholder image set (Queen Elizabeth/corgi/palace stock photos) — it does **not** describe the actual images currently in the folder, which are personal photos. Don't treat it as accurate; flag this mismatch if asked to update licensing info, and don't add real attribution entries for personal photos.

## Working in this repo

- Any change to displayed text should keep `index.html` and the corresponding `.md` note file consistent (e.g. editing the "Какая я" facts section should be reflected in `факты.md` and vice versa).
- Image references in `index.html` use exact filenames from `images/` (including Cyrillic filenames from Viber exports) — preserve exact filenames when adding/replacing images.
