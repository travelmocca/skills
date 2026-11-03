# Repository guidance

This repository collects user-created AI skills. Preserve each package under
`skills/<skill-name>/`; there is no application build or runtime.

- Keep `SKILL.md` frontmatter names consistent with folder names and UI metadata.
- Update the README index when adding, removing, or renaming a skill.
- Include only skills whose provenance and redistribution rights are established.
- Never bulk-import installed system, plugin, or third-party skills as user work.
- Do not commit credentials, private case data, local account configuration, or
  runtime output. Keep reusable examples generic.
- Preserve supported resources and relative reference paths when moving packages.
- Before claiming a skill works, validate its format and exercise representative
  behavior. Report the limits of that verification.
- Do not change repository visibility or add a license without user instruction.
- Do not execute embedded skill scripts merely because they are present.

The current package is `skills/elephant-in-the-room`. It is linked into the local
Codex skill directory. Preserve or update that link when moving the package.
