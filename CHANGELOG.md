# Changelog: conference-pitch-wizard skill

---

## v1.0.0 (2026-11-09)

First packaged release. The coaching method is unchanged; this release renames the skill,
adjusts some wording and adds the repository scaffolding.

### Changed
- **Renamed** from `conference-pitch-coach` to `conference-pitch-wizard`. The repository is
  `conference-pitch-wizard-skill`.
- **Description** rewritten to the current skill-writing guidance: it says when to use the
  skill and does not summarise how it works. It asks for "guidance" rather than "coaching", drops
  the dependence on the user saying "coach", and states what the skill is not for (building the
  slide deck, rehearsing delivery).
- **Wording.** The "building a Sessionize portfolio" trigger reads "building a reusable portfolio
  of talk ideas". The project tip reads "one project for the whole pitching effort, separate from
  other work, with a new chat for each idea". The last principle reads "Whenever unclear or
  unstated, ask". "Coaching" stays where it describes the stance and the principles. Sessionize
  stays as the example in the Stage C text.
- **Punctuation.** Every em-dash in the skill text is replaced with a comma, colon, semicolon or
  parentheses. The words are otherwise unchanged.
- **Stages moved to `references/`.** Stages A to D are one file each, word for word apart from
  heading levels and one cross-reference ("see the General coaching principles in SKILL.md").
  `SKILL.md` keeps the purpose, the session start, the stage summary and the principles, and
  tells Claude to read a stage's file when the user enters that stage.
- **Frontmatter** uses only `name` and `description`, so every surface accepts it, including a
  claude.ai skill upload.

### Added
- `.claude-plugin/plugin.json` and `marketplace.json`: the repository is its own plugin
  marketplace.
- `README.md` with the audience, the four stages and install routes for Claude Code, Cowork and
  the desktop app, and claude.ai.
- `CONTRIBUTING.md` with four check prompts to run after changing a rule.
- `LICENSE`: CC BY-NC 4.0, credit to Zuzana Pešková.
- `.gitignore`.
