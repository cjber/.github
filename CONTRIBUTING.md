# Contributing

Thanks for helping across these repositories. Start with the repository's `README.md` and, where present,
`AGENTS.md`; follow any `SKILL.md` those files reference for the task. Agent-assisted contributions are
welcome.

## Before you start

- Open an issue before working on a feature, so the idea can be agreed before code is written. Small
  bug fixes can go straight to a pull request.
- Report security problems privately, as [SECURITY.md](https://github.com/cjber/.github/blob/main/SECURITY.md)
  describes.

## Code

- Run the repository's checks before pushing. The canonical commands are in its `AGENTS.md` or `README.md`;
  CI should run the same checks.
- Preserve generated files according to the repository's instructions. If a file names a generator, change
  that generator and regenerate its output.

### WoW addons

- Addons run Lua 5.1 in the WoW: Forever client's sandbox: no `require`, and every file the client loads is
  listed in the addon's `.toc`.
- Never hand-edit generated files under `Data/`. Change the named generator and regenerate.
- Headless tests cannot cover every frame, menu, map pin or tracker path. List the remaining `/reload` checks
  in the pull request.

## Commits

- Signed commits (`git commit -S`) in the [Conventional Commits](https://www.conventionalcommits.org/)
  format, for example `fix(tracker): keep the waypoint when the quest log reorders`.
- One idea per commit. The body says why the change is needed.

## Pull requests

- Fill in the pull request template with why, what changed, and the actual check commands and results.
