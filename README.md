# reEnvisioning themes

Portable Base16 theme packs for reEnvisioning.

```sh
mkdir -p ~/.config/reEnvisioning
git clone https://github.com/reEnvisioning/themes.git ~/.config/reEnvisioning/themes
retheme switch sakura
```

## Pack layout

The canonical minimal pack contains only:

```text
my-theme/
├── theme.toml
└── base16.yaml
```

`theme.toml` identifies the pack; `base16.yaml` is its single Base16 palette (`base00` through `base0F`). Detailed app data is optional. If present under `apps/<app>/...`, it is inert app-native data; it is not executable and cannot choose arbitrary write targets or handlers. Other optional metadata may use TOML.

A pack may also include `wallpapers.toml` and the referenced image files under `assets/`. These are optional pack data, and asset paths are relative to the pack directory. Only include wallpapers and other assets cleared for public redistribution.

## Ownership

reTheme selects themes and wallpapers, resolves pack-relative wallpaper paths, and passes the selected path onward. reWallpaper only applies an explicit image path; it does not discover theme packs or select a theme or wallpaper. NixOS only provides fonts, non-theme settings, and stable generated Kitty/btop paths.
