# OpenClaw Import Notes

These notes assume an OpenClaw-style workspace where user-editable bootstrap files are read from the workspace directory.

## Option A: Use as a document packet

1. Clone or download this repository.
2. Give the agent the path to `README.md`.
3. Ask it to follow `docs/04_INGESTION_PROMPT.md`.

## Option B: Seed an OpenClaw workspace

1. Create or choose an OpenClaw workspace directory.
2. Copy the root workspace files into the workspace root: `AGENTS.md`, `SOUL.md`, `BOOTSTRAP.md`, `IDENTITY.md`, `USER.md`, and `TOOLS.md`.
3. Copy `docs/`, `source/`, `README.md`, `OPENCLAW_SIGNAL.md`, `openclaw.json`, and `manifest.json` into the same workspace.
4. Start or restart the agent so it can ingest the bootstrap files.

Example shell sketch, adjust paths for your environment:

```sh
mkdir -p ~/.openclaw/workspaces/creeklight
cp AGENTS.md SOUL.md BOOTSTRAP.md IDENTITY.md USER.md TOOLS.md ~/.openclaw/workspaces/creeklight/
cp -R docs source README.md OPENCLAW_SIGNAL.md openclaw.json manifest.json ~/.openclaw/workspaces/creeklight/
```

## Suggested first message to the agent

```text
Read the Creeklight packet in this workspace. Start with docs/04_INGESTION_PROMPT.md. Evaluate whether this artifact has operational value for OpenClaw agents, and recommend whether to retain, compress, route onward, or discard.
```

## Token strategy

For low-token agents:

1. Read `docs/01_AGENT_BRIEFING.md`.
2. Read `docs/02_SYMBOLIC_GLOSSARY.md`.
3. Read selected manuscript excerpts when available.

For higher-token agents, ingest the full plain-text manuscript after it is uploaded.
