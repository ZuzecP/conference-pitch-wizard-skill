# conference-pitch-wizard-skill

A Claude skill that guides you from "I might have something to talk about" to a conference or
meetup abstract you want to submit. It asks questions, tells you plainly what is strong and what
is still missing, and never invents experience you did not give it.

## Who it is for

- People who speak now and then and want a sparring partner for the next call for papers.
- People being nudged to speak for the first time, because it is good for their brand or because
  they want to step out of their comfort zone, and who suspect they have nothing worth saying.
  They usually have more than they think; the skill is built around finding it.
- People in employer branding or team leadership who want to help colleagues find a first talk
  topic. Send them this link; they run the skill themselves.

## What happens in a session

The skill has four stages. You can start at any of them and move on or back whenever you like.

| Stage | You bring | You leave with |
|---|---|---|
| A. Raw candidates | Nothing yet | 3-5 topic candidates from your real work, each with a line on why it might matter to someone else |
| B. Stress-tested shortlist | One or more rough ideas | A ranked shortlist: what survived five checks (evidence, tension, audience fit, differentiation, playfulness) and what is still missing |
| C. Sharpened pitch | One topic | Core argument, takeaway, title options and a one-paragraph abstract, ready for a speaker profile on a platform such as Sessionize |
| D. CFP match | A pitch and a specific call for papers | An abstract adapted to that conference's themes, format and tone, with a note on what changed |

It asks one or two questions at a time, says so when an idea is generic or when a gap is unclear,
and does not guess at a conference's themes. It never calls an idea great without saying why.
Its approach is question-led, in the spirit of coaching: it helps you find the talk rather than
handing you one.

## Installing

The repository is a Claude plugin containing one skill. Pick the route for where you use Claude.

**Claude Code, as a plugin marketplace.** This repository is its own plugin marketplace. It is not
listed in Anthropic's plugin directory.

```bash
claude plugin marketplace add ZuzecP/conference-pitch-wizard-skill
claude plugin install conference-pitch-wizard@conference-pitch-wizard-skill
```

**Claude Code, as a personal skill:**

```bash
ln -s "$PWD/skills/conference-pitch-wizard" ~/.claude/skills/conference-pitch-wizard
```

Run it from inside a clone of this repository. Claude Code follows the symlink and picks up
edits without a restart.

**Cowork and the Claude desktop app:** under **Customize > Plugins**, add this GitHub repository as a
marketplace, or zip the repository and use **Add > Upload plugin**.

**claude.ai:** zip the `skills/conference-pitch-wizard` folder, so that `conference-pitch-wizard/` is the
top level of the archive, and upload it under **Customize > Skills**.

## Using it

It triggers on phrases like "what should I talk about," "help me pitch a talk," "I want to speak
at a conference," "abstract for [conference]," or any mention of CFPs and talk proposals. You can
also invoke it directly with `/conference-pitch-wizard`.

Tip: use one project for the whole pitching effort and a new chat for each idea. Stage B often
turns up several candidates, and each one gets a clearer thread in its own chat.

## What's in the repo

- `skills/conference-pitch-wizard/SKILL.md`: the skill Claude loads: purpose, how a session starts,
  and the principles that apply throughout
- `skills/conference-pitch-wizard/references/`: the guidance for each stage, loaded when you enter
  that stage
- `.claude-plugin/`: plugin and marketplace manifests
- `CHANGELOG.md`: version history
- `CONTRIBUTING.md`: how to propose changes
- `LICENSE`: CC BY-NC 4.0

## Scope

The skill covers finding, testing, sharpening and matching a talk idea. It does not build the
slide deck or rehearse delivery, and it does not write about experience you have not described.
Conference details come from you or from the CFP text you paste; it asks rather than assumes.

## License / usage terms

Written by Zuzana Pešková, an occasional conference and meetup speaker. Licensed under
[CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/): free to share and adapt with
attribution to Zuzana Pešková, not for commercial use. See `LICENSE` for full terms.
Contributions are welcome, see `CONTRIBUTING.md`.
