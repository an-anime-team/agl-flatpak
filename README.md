# agl-flatpak

Flatpak builds for [anime-games-launcher](https://github.com/an-anime-team/anime-games-launcher).

## Installation

Download the latest `.flatpak` from the [Releases](https://github.com/an-anime-team/agl-flatpak/releases) page, then:
```sh
flatpak install /path/to/anime-games-launcher.flatpak
```

Or double-click the file in your file manager.

## Maintaining

Bump the `anime-games-launcher` submodule and push a `v*` tag matching upstream's
version — this triggers a CI release automatically.