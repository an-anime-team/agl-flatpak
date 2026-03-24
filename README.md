# agl-flatpak

Flatpak builds for [anime-games-launcher](https://github.com/an-anime-team/anime-games-launcher).

## Installation

Download the latest `.flatpak` from the [Releases](https://github.com/an-anime-team/agl-flatpak/releases) page, then:
```sh
flatpak install /path/to/anime-games-launcher.flatpak
```

Or double-click the file in your file manager.

### 32-bit GPU drivers

Installing from a `.flatpak` bundle does not automatically pull in 32-bit GPU drivers.
Run the command for your GPU after installing:

**AMD / Intel (Mesa)**
```sh
flatpak install flathub org.freedesktop.Platform.GL32.default//25.08
```

**NVIDIA**
```sh
flatpak install flathub org.freedesktop.Platform.GL32.default//25.08
flatpak install flathub org.freedesktop.Platform.VAAPI.nvidia.i386//25.08
```

**Intel (additional VA-API)**
```sh
flatpak install flathub org.freedesktop.Platform.VAAPI.Intel.i386//25.08
```

Unless you use WoW64 (available in Proton or Wine), if you skip this step, 32-bit games and Wine/Proton will fall back to software rendering or fail to launch.

## Maintaining

Bump the `anime-games-launcher` submodule and push a `v*` tag matching upstream's
version — this triggers a CI release automatically.