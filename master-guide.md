# Personal Assistant Setup — Master Guide

> 📄 **Latest version & updates:** https://github.com/dansped/endurance — see the [changelog](CHANGELOG.md) for what's new.

*Start here. This explains the one methodology behind all three setup wizards and helps you pick a platform. Then open the matching wizard file to actually build it.*

The three platform guides:

- **[claude-wizard.md](claude-wizard.md)** — Claude
- **[monday-wizard.md](monday-wizard.md)** — monday.com
- **[chatgpt-wizard.md](chatgpt-wizard.md)** — ChatGPT

---

## The idea (works on any platform)

A useful personal assistant isn't about the AI being smart — they all are. It's about giving it a **consistent place to keep your context** and a **consistent way to behave**. Every version below is the same five ideas, implemented with whatever each platform gives you:

1. **Give it a name and a personality.** A named assistant with a defined tone feels like *yours* and is easier to "address."
2. **Structured memory with fixed addresses.** A numbered set of homes (inbox, projects, people, journal, reference…) so there's always one obvious place for everything, and it always sorts the same way. This is the part people skip and then wonder why their assistant feels random.
3. **Two memory layers.** A *stable* layer (who you are, how you work — changes rarely) and a *dynamic* layer (what's active right now — changes weekly). Keeping them separate means you can refresh "what's current" without rewriting "who I am."
4. **An operating manual.** One place that says what to do at the start of a session, your working agreement (tone, how many questions, confirm-before-big-changes), and your boundaries.
5. **A capture-and-log habit.** Catch thoughts the moment they land; log what you did so the memory compounds. The system is only as good as the habit feeding it.

Everything platform-specific is just *how* each of those five gets implemented.

## The best practices that travel with all five

Beyond the structure, every version bakes in the same behavioral habits — these are what make an assistant pleasant and safe to live with, and they apply on any platform:

- **Short answers by default.** The assistant keeps replies brief and only goes long when asked. Faster to read, and it keeps usage costs down. (Set this up *on*, but confirm — a few people prefer fuller answers.)
- **Information safety, always on.** Some things shouldn't be typed into an online AI. The assistant flags anything that looks sensitive — client names, private details, confidential info — *before* you share or save it, and lets you decide. Not always a security risk; sometimes you just don't want it persisted.
- **Work vs. personal separation.** If you use the assistant for both, it tracks which is which and filters by audience: a summary for your boss leaves out personal projects; something for a friend leaves out work. When the audience is unclear, it asks.
- **The journal *is* the memory — and a cost-saver.** A daily log in two voices (your take + the assistant's take) means context lives in a file, not in an endless chat. So when a chat gets long (slower and more expensive), the assistant offers to summarize and continue fresh, handing you a short prompt to carry over — losing nothing. Pair it with a **rolling digest** (the last ~5 days, a few lines each) that the assistant reads at start-up instead of the full history — memory grows, start-up cost doesn't.
- **Boot light, load on demand.** The assistant reads the minimum at greeting (reminders + the digest) and pulls everything else — projects, preferences, reference — silently, the moment the conversation needs it. Keeps every session cheap; "full boot" on request brings back the proactive morning sweep.
- **Use the right-sized model.** The most capable model for the assistant's real thinking and judgment; a lighter, faster one for quick capture. (More on this per platform below.)
- **Findability scales the whole thing.** As the memory grows, a little structure — index/overview files, consistent naming, saved views — is the difference between "useful" and "overwhelming." It's the most common reason a personal assistant quietly stops getting used.

---

## Same idea, three implementations

| The concept | Claude | monday.com | ChatGPT |
|---|---|---|---|
| **Where memory lives** | A folder of markdown notes on your computer | Boards, items, and Docs in a workspace (structured data) | Project knowledge files + project/account memory |
| **Fixed-address structure** | Numbered folders (`00-inbox`, `22-projects`…) | Numbered boards/Docs in a workspace | Numbered documents you upload as knowledge |
| **Name your assistant** | Name in the boot file | Concept name; becomes a custom Agent's name | Project name or Custom GPT name |
| **Operating manual** | A boot file (`[AGENT].md`) it reads on greeting | An Operating-Manual Doc you point Sidekick at | Project / Custom GPT instructions |
| **Stable layer (about-me)** | `about-me.md` in the folder | `02-About Me` Doc | `about-me` knowledge file |
| **Dynamic layer (current state)** | A context note, optionally auto-refreshed | Live board data (always current by nature) | Re-uploaded knowledge file |
| **How you invoke it** | Greet it ("Hello [AGENT]") → reads boot file | Always-on Sidekick; **automations** for anything automatic | Just open the Project / Custom GPT |
| **Mobile** | A claude.ai Project + uploaded about-me | Built in — Sidekick is in the mobile app | Built in — Project/GPT syncs to the app |
| **Portable / always-on fallback** | Profile fields on claude.ai | (n/a — Sidekick is always there) | Global Custom Instructions |
| **Can it act on its own?** | Limited; scheduled tasks in desktop | Yes — automations and Agents are the strength | Limited; account memory learns passively |
| **Information safety flag** | In the boot file (always on) | In the operating-manual Doc | In the project/global instructions |
| **Work/personal separation** | Tags in notes + "who's this for?" rule | A Work/Personal board column | Tags in notes + "who's this for?" rule |
| **Long-chat handling** | Offers a journal + hand-off to a fresh chat | Sidekick chats are short; less of an issue | Offers a summary + hand-off; built-in project memory helps |
| **Daily briefing ("today")** | A generated note, optionally scheduled | A live dashboard / board View | A morning ask; paste calendar in |
| **Calendar** | Connect, or paste a weekly export | Native Calendar view + integrations | Paste a screenshot/export (or a connector) |
| **Choosing the model** | You pick (Opus recommended for main seat) | Managed by monday.com — not your call | You pick (most capable for the main seat) |

---

## Which should you pick?

- **Already living in monday.com (boards, tasks, projects)?** Use the **monday.com** version. Your assistant sits on top of work you're already tracking, and automations can nudge you without being asked. Best when "memory" = tasks, projects, and people you want to *track*, not just notes.
- **Want the richest, most flexible notes-based assistant and don't mind a desktop app?** Use **Claude**. It can read and write a real folder of notes on your machine, keep a journal, and run scheduled routines. Most powerful for freeform knowledge work.
- **Already pay for or prefer ChatGPT, want it simple and on your phone?** Use **ChatGPT**. Projects + voice on mobile gets you 90% of the value with the least setup, though it can't touch a folder on your computer.

You can also run more than one — e.g., monday.com for work tracking and ChatGPT on your phone for voice capture. Just keep the **about-me** consistent between them so they describe you the same way.

---

## The honest trade-offs

- **Claude** is the most capable with freeform notes and can genuinely read/write your files, but it needs the desktop app and a bit more setup, and the mobile sibling is a separate thing you maintain.
- **monday.com** turns reminders and projects into real, automated data — its biggest advantage — but freeform journaling is clunkier (you lean on Docs), and the most powerful "named Agent" features depend on your plan.
- **ChatGPT** is the easiest to stand up and the best mobile/voice experience, but it can't read files off your computer — its memory is whatever you upload and keep current, so it lives and dies by the refresh habit.

---

## How to start (any platform)

1. Read the five ideas above so you know *why* each step exists.
2. Pick a platform from the guidance above.
3. Open that platform's wizard file and follow it. For Claude and ChatGPT you can literally upload the file to the assistant and have it walk you through; for monday.com you follow it yourself in the app.
4. Whatever you pick: fill in the **about-me** properly and build the **capture habit**. Those two do most of the work.
5. Don't skip the best practices above — especially **information safety** and a little **findability** structure. Each wizard sets these up for you and confirms the optional ones as you go.
