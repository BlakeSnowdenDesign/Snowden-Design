# Working together: Claude + Replit

Two agents work in this repo. These rules keep them from overwriting each other.

## Branches

- `main` is the approved source. Nobody pushes to it directly; everything lands through a pull request that Blake merges.
- Claude works on `claude/<topic>` branches. Replit works on `replit/<topic>` branches.
- One branch per page or task. Start it from the latest `main`, and pull `main` in again before opening the PR.
- Never force-push, and never push to the other agent's branch. To change the other agent's work, leave a PR comment or open your own PR.

## Who owns what

| Path | Owner | Notes |
| --- | --- | --- |
| `pages/<page>/` | Whoever is listed in the table below | Each page is one Wix Embed HTML file plus its `preview.html`. |
| `velo/` | Replit | Velo page code, backend and public files for the Wix site. |
| `shared/` | Both, by PR only | Design tokens, fonts, shared snippets. Any change needs Blake's OK. |
| `REPLIT-HANDOFF.md`, `COLLABORATION.md`, `README.md` | Both, by PR only | Keep the page table current. |

### Page assignments

| Page | Owner | Status |
| --- | --- | --- |
| Home (`pages/home/`) | Claude | Draft built; copy awaits Blake's approval |
| Work (`pages/work/`) | _unassigned_ | |
| About (`pages/about/`) | _unassigned_ | |
| Contact (`pages/contact/`) | _unassigned_ | |
| 3D Visualization (`pages/3d-visualization/`) | Claude | Mongrain 3D showcase built; awaits Blake's review |

Claim a page by editing this table in your PR before you start it.

## Wix

- Build target: the Wix Studio site **Snowden Design 2**. Content source: the original **Snowden Design** site (snowden-design.com). Don't edit the original.
- Pages and elements are added in the Studio Editor by Blake. Agents supply the code that goes into them.
- Pushing to GitHub does not change Wix. Blake pastes the code (or synced Velo code updates in the editor) and presses Publish himself.
