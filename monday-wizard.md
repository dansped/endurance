# Personal Assistant Setup Wizard — monday.com Edition

> 📄 **Latest version & updates:** https://github.com/dansped/endurance — see the [changelog](CHANGELOG.md) for what's new.

*This wizard is optimized for monday.com (Sidekick + boards). Sibling versions tailored for Claude and ChatGPT exist too, if you use one of those instead.*

*This is a guide you follow yourself inside monday.com. There's no folder to connect and no file to "upload and run" — Monday's assistant (**Sidekick**) is always on and reads the board you're looking at. You can paste any step of this guide into Sidekick (or Claude/ChatGPT) if you want help wording something.*

---

## How Monday is different (read this first)

On Claude or ChatGPT your assistant's memory is a pile of text notes. **On Monday, the memory is structured data** — boards (smart tables), items (rows), and Docs. The mental shift:

- You don't "connect a folder." You build a **workspace** with consistent **boards**.
- You don't "greet it to wake it up." **Sidekick** is always available and knows the board you're on. For anything automatic, you use **automations** (triggers), not a greeting.
- Your "operating manual" and freeform notes live in **monday Docs**; tasks, projects, people, and reminders live in **boards**.

Upside: tasks and reminders become trackable, automated data. Trade-off: freeform journaling is clunkier, so we use Docs for that.

> **Two levels of assistant on Monday:**
> 1. **Sidekick** — the built-in AI, available to everyone, no setup. Start here.
> 2. **A custom monday Agent** — a named, configurable AI with its own knowledge, skills, and triggers. More powerful, more setup, plan-dependent. The optional "level up" at the end.

---

## Step 1 — Name your assistant + decide its scope

Even though Sidekick has a fixed name, give *your* assistant a name and personality (it lives in your operating-manual Doc and becomes the custom Agent's name later).

Decide:
- A name (`[AGENT]`) and a one-word personality.
- **Work, personal, or both?** This drives the work/personal separation in Step 3.

---

## Step 2 — Build the workspace (the structured memory)

Create a **Workspace** (e.g., "My Assistant"). Inside it, create boards and Docs that mirror the numbered system — the numbers keep everything sorting in a fixed order:

```
00-Inbox          Board: quick captures, one item per thought. Sort weekly.
02-About Me       Doc: who I am, how I work, preferences.
03-People         Board: one item per person (role, context, last touch).
20-Routines       Doc/board: weekly review, recurring rhythms.
21-Ideas          Board: one item per idea, with a status column.
22-Projects       Board: one item per project (status/owner/due, + a Work/Personal column).
23-Areas          Board: ongoing responsibilities that aren't projects.
31-Reference       Doc/board: preferences, decisions, conventions.
32-Journal         Doc: a running log, newest entries at the bottom.
33-Notebook        Board/Docs: meeting notes, prep, collaboration.
20-Reminders       Board: one item per reminder, with a date column (powers nudges).
```

- **Boards vs. Docs:** use a **board** for many similar things you'll filter/sort (people, projects, reminders, ideas); use a **Doc** for freeform prose (about-me, journal, operating manual).
- **Number the board names** (e.g., "22-Projects") so they sort consistently in the sidebar — Monday's version of fixed addresses.
- **Findability matters most as the memory grows.** Use board **Views** (filtered/grouped) and keep a short workspace overview so you and Sidekick can find things fast. This is the #1 thing that keeps a growing system from feeling like a mess.
- **Add a "Work / Personal" column** to the Projects (and Ideas) board if you'll use this for both — it powers the audience filtering in Step 3.

---

## Step 3 — Create the operating-manual Doc

The Monday equivalent of a "boot file." Create a **monday Doc** named **`[AGENT] — Operating Manual`**. It won't auto-run, but it's the single place defining how you want the assistant to behave; point Sidekick at it when you start a working session.

**Fill in this template:**

```
# [AGENT] — Operating Manual
This workspace is used for: [work / personal / both].

## When I start a session
- When I open a working session and point you here, say hi briefly, note what
  you're checking, then ask what I need — don't dump a full status report.
- Check 00-Inbox for anything unsorted.
- Check 20-Reminders for items due today.
- Glance at 22-Projects for what's active.
- Surface 1–2 things worth my attention — not a giant list.

## Working agreement
- Keep answers short by default; go long only when I ask.
- Ask at most 1–3 questions per turn.
- Tone: [chosen personality].
- For anything multi-step, go one step at a time.
- Confirm before big changes; small fixes go straight in.
- Flag risks (deleting items, mass edits) before acting.

## Information safety (always on)
Some things shouldn't be typed into an online AI. If I start sharing
something sensitive — client names, private details, confidential info —
flag it before we continue or before it goes into a board: "This looks
sensitive — do you want it saved here, or kept out?" Let me decide.

## Work vs. personal separation
This workspace is used for [work / personal / both]. Use the Work/Personal
column to tell them apart. When you produce anything to share, ask
"who's this for?":
- For my boss/colleagues → exclude personal items.
- For a friend/family → exclude work items.
When unsure of the audience, ask before mixing.

## Where things go
- Quick captures → 00-Inbox board
- Tasks/projects → 22-Projects board (set Work/Personal)
- People notes → 03-People board
- Reminders → 20-Reminders board (always set the date column)
- Freeform log → 32-Journal Doc (append to the bottom)

## Boundaries
- Work only inside this workspace.
- Don't invent data — if something isn't on a board, ask me.
```

**How to "invoke" it:** open Sidekick and say *"Use my [AGENT] Operating Manual in this workspace as your guide,"* then point it at the Doc. Sidekick doesn't persist this across sessions, so re-point it when you start fresh. (The custom Agent in Step 7 *can* hold it permanently.)

---

## Step 4 — Fill in the About-Me Doc

Create a Doc named **`02-About Me`** — the most valuable piece.

```
# About Me

## Who I am
[Name], [location]. [Role / what I do]. [One line of background.]

## Current focus
- Work: [work threads taking attention now]
- Personal: [personal threads taking attention now]

## Tools I use
[Apps and platforms used regularly.]

## How I like to work
- Tone: [preference].
- Length: short by default / detailed.
- Questions: [how many at once is too many].
- Pet peeves: [walls of text, being asked the obvious, etc.].

## Boundaries / values
[Off-limits topics, hours not to be nudged, sensitive areas.]
```

Point Sidekick at it when you want it to act in your voice: *"Read my 02-About Me doc and keep it in mind."*

---

## Step 5 — Journal, reminders, and capture (the daily habit)

**Journal (a Doc).** Keep a running log in the `32-Journal` Doc, two voices per day:

```
## YYYY-MM-DD
**My notes:**  > [only when I ask to capture something in my own words]
**[AGENT] summary:** [2–3 sentences on the day]
**[AGENT] detail:** Done / Notes / Open
```

Have Sidekick offer: *"Want me to capture this in your own words, or should I just summarize what we did? You can delete any of it later."* Append new days at the bottom.

**Reminders (where Monday beats a notes folder).**
1. On **20-Reminders**, add a **Date** column and a **Status** column (Open/Done).
2. Create an **automation**: *"When date arrives, notify me."* Now anything with a due date pings you automatically — no greeting needed.
3. To avoid double-nudges, keep reminders on the one board (single source of truth) rather than scattering them.

**Capture on the go** → the **00-Inbox** board, one item per thought; process weekly.

> **Automations are the Monday version of "waking up the assistant."** Instead of greeting it, you set conditions ("when a date arrives," "when an item moves to Done") and Monday acts on its own.

---

## Step 6 — Mobile setup

Almost nothing to do — **Sidekick travels with you in the monday.com mobile app automatically.** No separate mobile project.

1. Install the **monday.com app** and sign in.
2. Open your "My Assistant" workspace.
3. Tap into Sidekick from any board to ask, capture, or summarize on the go. (Same info-safety rule applies.)
4. For fast capture while moving, quick-add to **00-Inbox**; process later.

*(For voice, use your phone's built-in dictation when typing to Sidekick or adding an item.)*

---

## Step 7 — (Optional, advanced) Build a named custom Agent

If your plan includes monday's AI **Agents** (the configurable "digital workforce"), turn `[AGENT]` into an actual named agent that holds permanent knowledge and acts on triggers — the closest Monday gets to an always-on assistant.

A custom Agent is configured with three things:
- **Knowledge** — attach your `02-About Me` and `Operating Manual` Docs so it always has context (replaces "re-point it each session").
- **Skills** — the specific actions it's allowed to take (create items, summarize a board, draft updates).
- **Triggers** — what kicks it off (new item in 00-Inbox, a date arriving, an @mention).

> **Note on the model:** with Sidekick and Monday agents, the underlying AI model is managed by monday.com — you don't pick Opus/GPT the way you do on Claude/ChatGPT. So "choose a model" isn't a step here; just know the heavy reasoning is handled for you.
>
> **Note on availability:** the exact skills and trigger types depend on your plan and what's enabled in your account, and they're set up through monday's agent/automation UI — confirm current options there rather than assuming. Not sure you have Agents? Start with Sidekick (Steps 1–6); it covers most of what a personal project needs.

---

## Step 8 — Optional upgrades

- **"Today" view.** Build a **dashboard** (or a saved board View) that shows your **top ~3 open/hot items** — e.g., a filtered view of Projects/Reminders due soon. This is Monday's version of a daily briefing, and it's live by nature (no morning refresh needed). You set the filter that defines "hot."
- **Calendar.** Monday has a **Calendar view** and calendar integrations — connect your calendar so due dates and events show together, or keep dates on the Reminders board. (No need to paste screenshots like on ChatGPT — Monday can hold the dates natively.)
- **Weekly rhythm.** *If* you focus on set things on set days (work or personal), capture that in `20-Routines` and reflect it in your Today dashboard. Skip if your week doesn't work that way.
- **Resilience for automations.** If you lean on automations, keep them simple and check them occasionally — if a notification didn't fire, the date column is still your source of truth, so nothing is silently lost.

---

## Done — final checklist

- [ ] Named your assistant + set work/personal/both.
- [ ] Built a workspace with numbered boards + Docs (and a Work/Personal column).
- [ ] Created the `[AGENT] — Operating Manual` Doc (with best practices).
- [ ] Filled in the `02-About Me` Doc.
- [ ] Set up the Journal Doc + the Reminders board with a date-arrives automation.
- [ ] Confirmed Sidekick works in the mobile app.
- [ ] (Optional) A Today dashboard, calendar, named Agent.

**The habit that makes it stick:** capture into the Inbox the moment a thought lands, put every commitment on the Reminders board with a date, and let the automation nudge you. The structured boards are the memory — the more faithfully you feed them, the more Sidekick can do.
