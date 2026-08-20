# Interview Drill

`interview-drill` is a Codex skill for adaptive interview practice. It reads a
resume, job description, project materials, or a stated technical domain; asks
one interview question at a time; and gives evidence-based feedback before the
next question.

## Install

### Codex agent instructions

To install this skill, clone this repository into the local Codex skills
directory. In PowerShell, run:

```powershell
git clone https://github.com/cxxCoolStar/interview-drill.git "$env:USERPROFILE\.codex\skills\interview-drill"
```

If the directory already exists, update it instead:

```powershell
git -C "$env:USERPROFILE\.codex\skills\interview-drill" pull --ff-only
```

Start a new Codex task after installation so Codex discovers the new skill.
The skill is available as `$interview-drill`.

### macOS and Linux

```bash
git clone https://github.com/cxxCoolStar/interview-drill.git "$HOME/.codex/skills/interview-drill"
```

To update an existing installation:

```bash
git -C "$HOME/.codex/skills/interview-drill" pull --ff-only
```

## Use

Provide the materials to interview from, then invoke the skill:

```text
Use $interview-drill to interview me from my resume and this job description.
Ask one question at a time, give factual feedback after each answer, and answer
my counterquestions before continuing.
```

You can also specify a topic or difficulty, for example:

```text
Use $interview-drill to run a senior backend interview based on this project.
Focus on distributed-systems tradeoffs.
```

## Requirements

- Codex with local skill discovery enabled.
- Git, used only to install and update this repository.

No package installation, API key, or build step is required.

## Repository layout

- `SKILL.md`: skill instructions read by Codex.
- `agents/openai.yaml`: Codex UI metadata and default prompt.
