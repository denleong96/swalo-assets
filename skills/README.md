# Claude skills from the "10 folders" carousel

The actual skill folders from [this Instagram post](https://www.instagram.com/p/Db0wyP_Ev1G/)
by [@divyannshisharma](https://www.instagram.com/divyannshisharma/), vendored here so they
can be dropped straight into `~/.claude/skills/`.

Slide-by-slide transcription of the post lives in
[`../research/claude-skills-from-ig-Db0wyP_Ev1G.md`](../research/claude-skills-from-ig-Db0wyP_Ev1G.md).

## What's here

| # | Slide skill | Folder | Upstream |
|---|---|---|---|
| 1 | Frontend Design | `frontend-design/` | anthropics/skills |
| 2 | Algorithmic Art | `algorithmic-art/` | anthropics/skills |
| 3 | Systematic Debugging | `systematic-debugging/` | obra/superpowers |
| 4 | Canvas Design | `canvas-design/` | anthropics/skills |
| 5 | Theme Factory | `theme-factory/` | anthropics/skills |
| 6 | Web Artifacts Builder | `web-artifacts-builder/` | anthropics/skills |
| 7 | Superpowers | `superpowers/` (14 skills) | obra/superpowers |
| 8 | File Search | `file-search/` | massgen/massgen |
| 9 | — | — | slide not in the post |
| 10 | Skill Creator | `skill-creator/` | anthropics/skills |

Two notes on the table:

- **Skill 9 is missing from the carousel itself.** The slides run SLIDE 2–10 and then jump
  to SLIDE 12, so only 9 of the promised 10 are shown. Nothing to download for it.
- **`systematic-debugging/` is duplicated inside `superpowers/`.** The post lists it as its
  own skill (Skill 3) and it ships as part of the Superpowers bundle (Skill 7). It's kept at
  the top level so it can be installed on its own; install one or the other, not both.

The Superpowers bundle here is the skill set only. The upstream repo is a full plugin with
hooks and scripts — if you want that, install from source rather than copying this folder.

## Install

Copy the folders you want:

```bash
mkdir -p ~/.claude/skills
cp -r skills/frontend-design ~/.claude/skills/
```

Or all of them at once (skipping the duplicate, taking Superpowers' skills flat):

```bash
mkdir -p ~/.claude/skills
cp -r skills/{frontend-design,algorithmic-art,canvas-design,theme-factory,web-artifacts-builder,skill-creator,file-search} ~/.claude/skills/
cp -r skills/superpowers/*/ ~/.claude/skills/
```

Restart Claude, then name the skill in your prompt:

> "Using the frontend-design skill, build me a landing page for…"

In Claude Code you can also skip all of this and install straight from GitHub:

```
/install-github-skill https://github.com/anthropics/skills/tree/main/skills/frontend-design
```

## Provenance

Fetched 2026-08-10 at these commits:

| Repo | Commit |
|---|---|
| `github.com/anthropics/skills` | `f17010c9bb483898c1d9c9f42dde2b3a98889434` |
| `github.com/obra/superpowers` | `44c9b2d6e889982ac18c27d05a19fefe335194e1` |
| `github.com/massgen/massgen` | `007bd8579298d7dc3ff2a43c378e27a284902f22` |

Each folder keeps its upstream licence. These are third-party skills, not Swalo assets —
they're vendored for convenience and are not maintained here.
