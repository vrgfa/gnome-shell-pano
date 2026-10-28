# Fork notes (vrgfa)

Fork of [oae/gnome-shell-pano](https://github.com/oae/gnome-shell-pano) (TypeScript sources on `master`).

## Branches

| Branch | Purpose |
|---|---|
| `master` | Upstream, untouched. |
| `installed-build` | **What is installed** (`~/.local/share/gnome-shell/extensions/pano@elhan.io` is a symlink to this clone — keep this branch checked out). Orphan branch with the built extension, not the sources: commit 1 = Pano 1001 build from extensions.gnome.org (shell 45–46), commit 2 = local GNOME 50 patch. |

## Local changes log

- 2026-10-25 — GNOME 50 patch of the built bundle (`extension.js`, `metadata.json`):
  - `shell-version` 45–50.
  - GNOME 50 removed `Meta.Cursor` / `display.set_cursor()`: cursor set per actor with `set_cursor_type()`.
  - `St.ImageContent.set_bytes()` takes the Cogl context first.
  - Panel button: the click gesture opens the menu for any button; limited to the right button so left/middle click still toggle Pano.
- 2026-10-28 — Put into git on `installed-build`.

## To do for an upstream pull request

Port the patch to the TypeScript sources on a branch from `master`, build, and compare with `installed-build`.
