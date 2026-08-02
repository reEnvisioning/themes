# reEnvisioning themes

Portable Base16 theme packs for reEnvisioning.

```sh
mkdir -p ~/.config/reEnvisioning
git clone https://github.com/reEnvisioning/themes.git ~/.config/reEnvisioning/themes
retheme switch sakura
```

Each top-level directory is a theme pack with `theme.toml`, exactly one `base16.yaml` containing `base00` through `base0F`, optional metadata/assets, and app data. reTheme owns the fixed runtime renderers; app files are not executable handlers and cannot declare arbitrary write targets. NixOS only provides fonts, non-theme settings, and the stable generated Kitty/btop paths.

Only include wallpapers and other assets cleared for public redistribution.
