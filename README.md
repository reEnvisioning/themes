# reEnvisioning themes

Portable TOML theme packs for reEnvisioning.

```sh
mkdir -p ~/.config/reEnvisioning
git clone https://github.com/reEnvisioning/themes.git ~/.config/reEnvisioning/themes
retheme switch sakura
```

Each top-level directory is a theme pack with `theme.toml`, optional shared TOML files, relative assets, and flat `apps/*.toml` entries. `retheme` applies `handler = "file"`; settings handlers are still handled by NixOS.

Only include wallpapers and other assets cleared for public redistribution.
