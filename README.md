# skills

PageZERO agent skills. Install with [vercel-labs/skills](https://github.com/vercel-labs/skills).

| Skill | Description |
|-------|-------------|
| `pr-create` | GitHub PRs with conventional naming |
| `pr-merge` | Squash-merge current branch PR after checks pass |
| `component-create` | UI component scaffold (PageZERO layout) |
| `theme-change` | shadcn/ui OKLCH theme in `apps/core/styles/tailwind.css` |

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
