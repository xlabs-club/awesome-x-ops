# Contributing to awesome-x-ops

Thanks for helping improve awesome-x-ops.

This repository is a curated map, not a link dump. Please keep every change focused, accurate, and useful for teams building or operating production systems.

## What belongs here?

Good candidates usually match at least one area:

- AI Ops, LLM Ops, LLM observability, RAG observability, or agent observability
- DataOps, DevOps, GitOps, FinOps, DevSecOps, or Platform Engineering
- Kubernetes operations, infrastructure automation, IAM, CI/CD, IaC, testing, or developer experience
- Production-grade open-source tools with clear docs and active maintenance

## What does not belong here?

Please avoid:

- Abandoned projects
- One-off demos or toy examples
- Vendor-only marketing pages without a useful open-source repository
- Duplicate projects or tools already covered by an equivalent entry
- Unrelated AI apps, SaaS products, or generic productivity tools
- Long descriptions that make the README hard to scan

## Entry style

Use one short sentence:

```markdown
- [Project](https://github.com/org/project): Concise explanation of why it matters for X-Ops.
```

Rules:

- Prefer GitHub links when the repository is the canonical source.
- Keep product and project names unchanged.
- Use natural technical language; do not force literal translations.
- Add the same project to both `README.md` and `README.zh-CN.md`.
- Put the project under the most specific useful category.

## Pull request checklist

Before opening a PR:

- [ ] I checked the project is not already listed by name, URL, organization/repo, or obvious alias.
- [ ] I added or updated both English and Chinese README files when adding entries.
- [ ] Descriptions are short, factual, and useful.
- [ ] Links are stable and preferably point to GitHub repositories.
- [ ] The PR is focused and does not mix unrelated changes.

## Suggesting a project

If you are unsure where a project belongs, open an issue with:

- Project name and URL
- Category suggestion
- Why it matters for production operations or platform teams
- Evidence of maintenance or adoption, if available
