<p align="center"><img src="c948d88d3d5c5948a7c7acdbeb6ba1bc4e2a8ed1d174348ea4c903b22ab4c1e9.png" width="160" alt="Creator Monk Studios"></p>

# Creator Monk Studios — Agent Skills

Free, open skills for AI agents, built and used in production by [Creator Monk Studios](https://creatormonk.in) — a digital marketing, automation and growth agency from Greater Noida, India. *Fuel the future.*

These skills teach AI agents (Claude, Muse and other SKILL.md-compatible agents) how to do real agency work the way a professional team does it: with checklists, quality gates and zero guesswork.

## Skills in this repository

### 1. Agency Content Planner with Duplicate Prevention
`skills/agency-content-planner/`

Run a multi-client social media content planner end to end: intake, captions, client approvals, scheduling and circle-close. Its hard gates make sure no creative is ever posted twice — the most expensive mistake in agency content operations.

### 2. Short-Form Video Editing (Reels and Shorts)
`skills/short-form-video-editing/`

Edit vertical short-form videos that are ready to publish without fixes: hook-first structure, pacing, captions inside safe zones, audio mixing, a brand-pure end card, export specs and a full final-watch quality check.

### 3. Low-Token Playbook — Agent Self-Discipline
`skills/low-token-playbook/`

Run any AI agent on a small token quota without losing quality: answer-first output discipline, tool-output filtering before it enters context, and session habits that stop quota waste.

### 4. Facebook and WhatsApp Browser Discipline
`skills/facebook-whatsapp-browser-discipline/`

Operate Facebook, Business Suite, Messenger and WhatsApp Web through an agent browser without killing the login session: reuse the existing tab, verify the session before acting, and recover cleanly when it expires.

### 5. YouTube Channel Standard
`skills/youtube-channel-standard/`

Apply a locked channel standard to every video and Short: the right thumbnail format per item type (vertical for Shorts, landscape for videos), bold high-CTR thumbnails, consistent category and language, and captions taken only from real auto-captions — never invented.

## How to use a skill

1. Copy the skill's folder into your agent's skills directory.
2. The agent reads `SKILL.md` for the method and `skill.yaml` for its metadata.
3. Adapt brand names, folders and tools to your own setup — the workflow and the gates stay the same.

## Install

**Claude Code**
```bash
git clone https://github.com/creatormonkstudios/creatormonk-skills.git
cp -r creatormonk-skills/skills/agency-content-planner ~/.claude/skills/
```
Copy any skill folder the same way. Each skill is a standard SKILL.md package.

**Muse**
Copy the skill folder into `~/workspace/custom-skills/` — the format (SKILL.md + skill.yaml) loads as-is.

**Any SKILL.md-compatible agent**
Point your agent at the skill's folder, or paste the raw SKILL.md URL into its skills setup.

## Why free?

We learned these lessons the expensive way, in live client work. Sharing them makes the whole ecosystem better — and if your agency outgrows doing this by hand, you know where to find us.

## Contributing

Issues and pull requests are welcome. If a gate in these skills saved you from a duplicate post or a bad export, we would love to hear about it.

## License

MIT — free for anyone to use, copy and adapt, including commercially. See [LICENSE](LICENSE).

---

**Creator Monk Studios** · creatormonk.in · Greater Noida, India
Digital marketing · Automation · Growth
