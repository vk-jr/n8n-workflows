# Contributing

Thanks for contributing! This repo is a library of n8n workflow JSONs — here's how to add or improve them.

## How to Submit a Workflow

1. **Fork** the repository and create a branch: `git checkout -b workflow/my-workflow-name`
2. Export your workflow from n8n: **Workflow menu → Download**
3. **Remove all credential data** before committing — n8n exports credentials as empty references, but double-check
4. Place the JSON in a descriptive folder (create one if the category doesn't exist)
5. Update `README.md` with a short description of your workflow
6. Open a pull request

## Workflow Quality Checklist

Before submitting, make sure your workflow:

- [ ] Imports cleanly into a fresh n8n instance
- [ ] Has descriptive node names (not "HTTP Request1", "Set2", etc.)
- [ ] Contains **no hardcoded API keys, tokens, or passwords** — use n8n credential nodes
- [ ] Has sticky notes explaining non-obvious logic
- [ ] Is listed in `README.md` with trigger type, services used, and use case

## Folder Naming

Use a clear, human-readable folder name that describes the workflow's purpose:

```
Good: Sales Agent, Deep Research, Newsletter
Bad:  workflow1, test, my-stuff
```

## Bug Reports & Feature Requests

Use the GitHub issue templates:
- **Bug:** A workflow produces an error or unexpected output after import
- **Feature:** A new workflow category or enhancement you'd like to see

## Code of Conduct

Be constructive, be helpful, be kind.
