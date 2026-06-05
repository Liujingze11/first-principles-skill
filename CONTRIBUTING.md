# Contributing

Thanks for helping improve First Principles Skill. The project should stay lightweight, practical, and tool-neutral.

## Principles

- Prefer clear prompts over complex frameworks.
- Keep content usable across many AI coding agents.
- Do not add dependencies, build tools, or generated assets unless clearly justified.
- Do not invent platform-specific commands or configuration behavior.
- Make tradeoffs explicit when adding or changing guidance.

## Good Contributions

- New scenario prompts with a clear use case.
- Improvements to existing prompts that reduce ambiguity.
- Integration examples for additional AI coding tools.
- Realistic examples that show how to reason before coding.
- Documentation that helps users adapt the prompts safely.

## Prompt Quality Checklist

Before submitting prompt changes, check that the prompt:

- Separates facts from assumptions.
- Asks for constraints before choosing an approach.
- Pushes toward root cause instead of surface symptoms.
- Compares multiple options when meaningful.
- Prefers simple, reversible, verifiable implementation paths.
- Includes verification, risks, and rollback.
- Avoids hype-driven technical choices.

## Security Checklist

Do not commit:

- API keys, tokens, cookies, or credentials.
- Private SSH keys.
- Personal credentials or private contact details.
- Local absolute paths, machine names, or IDE-specific settings.
- Temporary files, logs, caches, or binary artifacts.
- Proprietary customer, employer, or project information.

## Local Review

Before committing, run:

```bash
git status
rg -n "api[_-]?key|token|secret|password|cookie|BEGIN .*PRIVATE KEY|ssh-rsa|sk-" .
```

Review every match manually. False positives are fine; real secrets are not.

## License

By contributing, you agree that your contribution will be licensed under the MIT License.
