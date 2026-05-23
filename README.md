# skills

PageZERO agent skills. Install with [vercel-labs/skills](https://github.com/vercel-labs/skills).

| Skill | Description |
|-------|-------------|
| `create-pr` | GitHub PRs with conventional naming |
| `merge-pr` | Squash-merge current branch PR after checks pass |
| `create-component` | UI component scaffold (PageZERO layout) |
| `change-theme` | shadcn/ui OKLCH theme in `apps/core/styles/tailwind.css` |

## Install

```bash
# project
npx skills add pagezero-dev/skills

# global
npx skills add pagezero-dev/skills -g
```

```bash
# local clone
npx skills add .
```

## Update

```bash
npx skills update        # all
npx skills update -p     # project only
npx skills update -g     # global only
```

MIT — [LICENSE](LICENSE)
