# Agent Teams (migrated from wshobson/agents)

**English** | [简体中文](README.zh.md)

An [Agent Roster](https://github.com/STofone/dsh-agent-roster) archive: the upstream team's role definitions
converted into a `roster.yaml`, with fields mapped one to one. Drop it into your local roster library and run
it on top of `dsh-agent-teams`.

## Upstream

- Repo: [`wshobson/agents`](https://github.com/wshobson/agents/tree/main/plugins/agent-teams/agents)
- License: MIT
- Stars: 41,969
- Scope: frontmatter and body of `plugins/agent-teams/agents/*.md`; the `context-manager` agent in the same
  plugin belongs to the engineering plugin and is not migrated.

Upstream text is kept in its original wording. Only three things changed: field names were moved to this
roster format, tool names were mapped to DSH tool names, and the orchestration logic (action pipeline /
workflow) was left to the team runtime.

## Usage

```bash
# Validate the archive you just checked out
npx --yes @stofone/dsh-agent-roster@latest validate --dir rosters

# List members
npx --yes @stofone/dsh-agent-roster@latest list --dir rosters
```

With DSH installed, open the panel's "Sources" tab, add this repository's collection to `indexes` and click
"Pull to this machine". After that, inspect members with `roster_show` and generate `add_member` calls with
`roster_create`.

## Files

```
registry.json                     public registry entry (used by registry fetch)
rosters/agent-teams/roster.yaml   the roster itself
.github/workflows/validate.yml    validation on push
```

## License

Upstream is MIT; the migrated files are MIT as well, see `LICENSE`.
