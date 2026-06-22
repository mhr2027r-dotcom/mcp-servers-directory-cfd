# Contributing

This is a curated directory of public **MCP servers**. Listings are pointers to
upstream projects (name, description, links, install command) — no third-party
code is vendored.

## Add or update a server

1. Edit [`data.py`](data.py) — add a `Server(...)` entry with an accurate
   description, category, maintainer, transport(s), install command, and repo URL.
2. Run `python main.py generate` to refresh `README.md`.
3. Run `pytest -q` (registry integrity + CLI smoke).
4. Open a PR describing the addition and linking the upstream project.

If you maintain a listed server and want it corrected or removed, open an issue.

## Quality bar

- Prefer first-party/official servers; mark `official=True` only when the entry
  is maintained by the vendor or the MCP reference project.
- Keep descriptions one line and factual. No marketing copy.
- `python main.py generate` must leave `README.md` unchanged in CI (keep it in sync).
