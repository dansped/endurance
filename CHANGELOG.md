# Changelog

All notable changes to the Endurance wizards.

## 2026-06-10

- **Token & memory practices, all guides** (learned from a live vault overhaul):
  - **Lazy boot** — the assistant reads the minimum at greeting (reminders + a digest) and loads everything else on demand; "full boot" on request. Cuts per-session start-up cost roughly in half.
  - **Rolling journal digest** — a small "latest" file (last ~5 days, 2 sentences + open items each) is what the assistant reads at start-up; full month files become archive. On ChatGPT this doubles as the small re-uploaded knowledge file; on monday.com it's a "Latest" Doc or filtered view.
  - **Rules-only operating manual** — history and old diagnoses move to a linked reference note; the boot file/manual stays lean because it loads every session.
  - **Findability & pruning** — `[[wikilink]]` + `Related:` footer habits so notes stay discoverable, and archive-don't-bloat for backlogs and lists.
- Master guide: added "Boot light, load on demand" to the traveling best practices; digest folded into the journal practice.

## 2026-06-05

- **Named the method "Endurance"** and added this hub + changelog.
- **Claude wizard — mobile/portable rework:** your assistant now lives in claude.ai Profile preferences, so it works on the web and your phone with no Project required. Added a comfort-based setup path (simplest vs. a bit more memory), an upgrade ladder, a greeting intro + end-of-chat handoff, email-first phone-to-computer notes, and clearer "which device does what" guidance.
- **Self-update check:** the Claude boot file now checks this repo for new versions (monthly or on demand), and offers to walk you through any improvement — best-effort, and never applied without your OK.
- ChatGPT and monday.com wizards: still on the earlier mobile section — update pending.
