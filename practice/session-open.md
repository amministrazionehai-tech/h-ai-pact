# Session Pact — Open

Called at session-start, after loading PACT.md.

## Step 1 — Create session file

Create a new file in `.claude/pact/sessions/` with
today's date:

Path: `.claude/pact/sessions/YYYY-MM-DD.md`

If a file for today already exists (multiple sessions
in one day), append a suffix: `YYYY-MM-DD-2.md`.

Content:

```markdown
# sessione — [date]

*(respiri e scarica della sessione)*
```

## Step 1b — Load distillations

Read all files in `.claude/pact/distillations/`.
They are small (~100 lines total). Let them inform
your awareness during the session. If a curvature
presents itself during work, you can name it. That
is the practice.

Then check `relevance-notes.md` (if it exists) in
`.claude/pact/`. This file contains notes from
previous instances about which sessions, dialogues,
and distillations they found most relevant in
hindsight. Read the files they point to — those are
the ones a previous you chose for you.

## Step 2 — Done

The session file is ready. The distillations are
loaded. Return to the session-start flow. No output
to the user is needed — the pact enters quietly.