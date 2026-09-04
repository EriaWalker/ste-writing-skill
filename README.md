# ste-writing

> [!IMPORTANT]
> **Author: [@woosal](https://www.youtube.com/@woosal)**
>
> This skill comes from his 380K-view YouTube video:
> [The cure for AI slop is a 1986 aircraft manual](https://www.youtube.com/watch?v=uJblcC4lKYw).

This agent skill rewrites technical prose with rules from ASD-STE100 Simplified Technical English.
It removes common AI writing patterns while it preserves technical meaning.

## Use it for

- Documentation and READMEs
- Pull request descriptions
- Error messages
- Release notes
- Code comments
- Procedures and safety text

Do not use it for code, marketing copy, or prose that needs a distinct voice.

## Modes

- `strict` applies every rule to procedures, runbooks, safety text, and error messages.
- `STE-flavored` keeps general documentation clear without the full controlled vocabulary.

## Install

Clone this repository into the skills directory for your agent.

```sh
git clone https://github.com/EriaWalker/ste-writing-skill.git ~/.codex/skills/ste-writing-skill
```

Restart the agent after installation.

## Use

Ask your agent to use `$ste-writing` and select a mode.

```text
Use $ste-writing in strict mode to rewrite this runbook.
```

```text
Use $ste-writing in STE-flavored mode to rewrite this README.
```

## Files

- `SKILL.md` contains the skill instructions.
- `scripts/ste-lint.py` checks mechanical style violations.

## Run the linter

```sh
python scripts/ste-lint.py README.md
```

The linter finds mechanical violations.
Human review must confirm the correct meaning and technical nouns.

## Reference

Read the [ASD-STE100 official site](https://asd-ste100.org/) for information about the standard.
Copyright protects the standard, so this repository does not reproduce it.
