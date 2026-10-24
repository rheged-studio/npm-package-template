---
title: correct the extends guidance and drop the dead scripts include
release_note: ""
created_at: "2026-10-24T16:04:38Z"
merged_at: ""
branch: r-2949-npm-package-template-correct-the-extends-guidance-and-drop
pr:
commit: ""
author: rob@rheged.studio
co_authors: []
category: docs
breaking: false
issues:
  - R-2949
stats:
  loc_added:
  loc_removed:
  files_changed:
version: ""
---

## Changed

- **`CLAUDE.md` now describes `extends` correctly ([R-2949](https://linear.app/rheged-studio/issue/R-2949)).** TypeScript inherits `files`/`include`/`exclude` from the base config; an extending config's own values replace them. The note previously claimed only `compilerOptions` were inherited.
- **Dropped the dead `infrastructure/scripts/**/*.ts` include ([R-2949](https://linear.app/rheged-studio/issue/R-2949)).** `infrastructure/scripts/` has been shell-only since [R-808](https://linear.app/rheged-studio/issue/R-808), so the pattern in `tsconfig.tools.json` and `tsconfig.eslint.json` matched no files. The `CLAUDE.md` coverage description is updated to match.
