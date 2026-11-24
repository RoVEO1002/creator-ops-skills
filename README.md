# Creator Ops Skills

Eight Claude skills I use every week as a designer running content accounts — planning short-form video, breaking down what went viral, picking weekly topics, locking image prompts, handing work to Codex, and kicking off web, game and festival projects.

Works with **Claude Code** and **Claude apps** that support Agent Skills (a folder with a `SKILL.md`).

| Skill | What it does |
|---|---|
| `short-form-planner` | Research → two-step hook → one CTA → timed shot list for Reels / Shorts / TikTok |
| `viral-post-breakdown` | Finds posts that did 3× the median on reference accounts and breaks down why |
| `weekly-topic-scout` | Scores topic candidates (10-point rubric) into a 7-slot weekly plan built for follows |
| `image-prompt-lock` | Rewrites image requests into clean prompts that keep your character's identity |
| `codex-handoff` | A fill-in directive format for handing batches, images or code review to OpenAI Codex |
| `web-project-kickoff` | Brief → wireframe → design system → stack → build → mobile QA |
| `game-design-doc` | One-page game design doc + minimum playable checklist (Roblox / browser) |
| `festival-prep` | Packing checklist, day timeline and stamina basics from official notices |

## Install

**Claude Code**
```bash
git clone https://github.com/RoVEO1002/creator-ops-skills.git
mkdir -p ~/.claude/skills
cp -R creator-ops-skills/skills/* ~/.claude/skills/
```
Then type `/` in Claude Code to see them.

**Claude app**: zip a single skill folder (e.g. `skills/festival-prep`) and upload it under Settings → Capabilities → Skills.

## Notes
- Skills never post, schedule, delete or upload on their own — anything public waits for your approval.
- Built and tested on my own accounts; adapt the account rules and sources to yours.

## License
MIT
