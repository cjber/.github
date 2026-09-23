# Contributing

Thanks for helping. These notes apply to every WoW: Forever addon repository here; a repository's own
`AGENTS.md` adds its specifics.

## Before you start

- Open an issue before working on a feature, so the idea can be agreed before code is written. Small
  bug fixes can go straight to a pull request.
- Report security problems privately, as [SECURITY.md](SECURITY.md) describes.

## Code

- The addons are Lua 5.1 running in the WoW: Forever client's sandbox: no `require`, and every file
  the client loads is listed in the addon's `.toc`.
- Never hand-edit generated files under `Data/`. Change the generator script (the file's header or
  the repository's `AGENTS.md` names it) and regenerate.
- Run the repository's gate before pushing. The exact commands are under **Commands** in its
  `AGENTS.md`; CI runs the same gate.

## Commits

- Signed commits (`git commit -S`) in the [Conventional Commits](https://www.conventionalcommits.org/)
  format, for example `fix(tracker): keep the waypoint when the quest log reorders`.
- One idea per commit. The body says why the change is needed.

## Pull requests

- Fill in the pull request template: why, what, the gate output, and in-game checks.
- The tests run headless with stubbed client APIs. List anything they cannot reach (frames, menus, map
  pins, the tracker) as `/reload` checks a reviewer can run in game.
