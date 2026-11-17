# AGENTS.md

This is the **workspace** of Mini Train Store (minitrainstore.fr), a French model railway shop: it
gathers the repositories of the [MiniTrainStore](https://github.com/MiniTrainStore) organization
as Git submodules and contains no code of its own. Each submodule is built, tested and released on
its own and has its own `AGENTS.md`: follow that file when working inside a submodule.

## Layout

| Submodule | Repository | Owns |
| --- | --- | --- |
| `boutique/` | MiniTrainStore/boutique (private) | The online shop: Vendure server, Next.js storefront, shop configuration, MCP server, design documentation |
| `identite/` | MiniTrainStore/identite | Visual identity: logo, icon, business and shipping cards, artwork, and the scripts that export them |
| `extension/` | MiniTrainStore/extension | Browser extension for Leboncoin listings (WXT, Vue 3) |

`.local/` (gitignored) keeps local data of the former Leboncoin scripts, including secrets: never
read it into outputs, never commit it.

## Commands

- `git submodule update --init`: fetches the submodules (`boutique` needs access to the private
  repository).
- `git submodule update --remote`: moves every submodule to the latest commit of its `main`
  branch; then commit the new pointers here (`chore: update the submodules`). Dependabot opens the
  same update weekly.

## Rules

- Change code in the submodule's own repository: commit and push there first, then commit the new
  pointer here.
- Commit directly on `main`. Messages follow Conventional Commits (`chore(boutique): …`), in
  English. Do not mention AI tools or assistants, and add no `Co-Authored-By` or
  "Generated with" lines.
- User-facing content is in French; never use the em dash (the long dash) anywhere.
- Never commit customer data or secrets.
