---
name: openfile
description: Form a U.S. company or file a U.S. trademark with OpenFile. Use when the user asks about forming an LLC or corporation, state filing fees or annual reports, checking or filing a trademark, or where an OpenFile order or filing stands.
---

# OpenFile

OpenFile forms U.S. companies and files U.S. trademarks. The tools prepare
drafts; the owner signs and pays on joinopenfile.com. Nothing is filed or
charged from the agent.

## Before drafting anything

- Call `plan_task` for the job and ask the user every question it lists that
  they have not answered. Never fill in names, addresses, owners, classes or
  answers yourself.
- Quote first (`quote_formation`, `quote_application`) so the user sees every
  fee, with the government's marked.
- After `create_formation` or `create_application`, give the user the
  `review_url` and say they sign and pay there.

## Common jobs

- State facts: `list_states`, `get_state`.
- Trademarks: `screen_mark`, then `search_marks`; `suggest_classes` for wording;
  `suggest_alternatives` when a name looks risky.
- Status: `get_order` for a company, `get_filing` for a trademark.
- How OpenFile works: `search_docs`, `read_doc`.

This is information and form filling, not legal advice.
