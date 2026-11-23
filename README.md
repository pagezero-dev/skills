# skills

PageZERO agent skills. Install with [vercel-labs/skills](https://github.com/vercel-labs/skills).

| Skill | Description |
|-------|-------------|
| `pr-create` | GitHub PRs with conventional naming |
| `pr-merge` | Squash-merge current branch PR after checks pass |
| `component-create` | UI component scaffold (PageZERO layout) |
| `theme-change` | shadcn/ui OKLCH theme in `apps/core/styles/tailwind.css` |
| `pagezero-upgrade` | Upgrade a PageZERO-based project to the latest starter |

## Install

```bash
# project
bunx skills add pagezero-dev/skills

# global
bunx skills add pagezero-dev/skills -g
```

```bash
# local clone
bunx skills add .
```

## Update

```bash
bunx skills update        # all
bunx skills update -p     # project only
bunx skills update -g     # global only
```

MIT — [LICENSE](LICENSE)
