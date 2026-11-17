<h1 align="center"><a href="https://www.minitrainstore.fr/">Mini Train Store</a> : espace de travail</h1>

Workspace of [Mini Train Store](https://www.minitrainstore.fr/), the model railway shop of Arnaud ANNERAUD: every repository of the project, as Git submodules pinned to a known commit.

| Submodule | Repository | Content |
| --- | --- | --- |
| `boutique/` | [MiniTrainStore/boutique](https://github.com/MiniTrainStore/boutique) (private) | Online shop: Vendure server, Next.js storefront, configuration, MCP server, design documentation |
| `identite/` | [MiniTrainStore/identite](https://github.com/MiniTrainStore/identite) | Visual identity: logo, business and shipping cards, artwork |
| `extension/` | [MiniTrainStore/extension](https://github.com/MiniTrainStore/extension) | Browser extension for Leboncoin listings |

## Get started

```sh
git clone --recurse-submodules https://github.com/MiniTrainStore/espace-de-travail.git
cd espace-de-travail
```

`boutique/` is private: cloning it needs access to the repository. In an existing clone, `git submodule update --init` fetches the submodules, and `git submodule update --remote` moves them to the latest commit of their `main` branch (then commit the new pointers here).

Each repository is built, tested and released on its own; see its README.

## About

All rights reserved to [Alix ANNERAUD](https://alix.anneraud.fr/).
