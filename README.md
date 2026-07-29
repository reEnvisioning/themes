# reEnvisioning themes

Portable theme packs for the reEnvisioning desktop ecosystem.

Install for local use:

```sh
mkdir -p ~/.config/reEnvisioning

# If Nix/Home Manager previously created this directory, move it away first.
# Do this after rebuilding to the NixOS version that no longer manages themes.
mv ~/.config/reEnvisioning/themes ~/.config/reEnvisioning/themes.bak.$(date +%s) 2>/dev/null || true

git clone https://github.com/reEnvisioning/themes.git ~/.config/reEnvisioning/themes
```

Expected runtime shape:

```text
~/.config/reEnvisioning/themes/
├── sakura/
│   ├── theme.toml
│   ├── theme.json        # compatibility for current apps/scripts
│   ├── colors.toml
│   ├── typography.toml
│   ├── spacing.toml
│   ├── animation.toml
│   ├── icons.toml
│   ├── wallpapers.toml
│   ├── assets/
│   └── apps/
└── horror/
    └── ...
```

Each `apps/*.toml` file carries metadata so tools do not need app-specific hardcoding. Current `reTheme` supports generic `handler = "file"`; `handler = "settings"` is still applied by the NixOS `external-theme` bridge until those handlers move out of NixOS.

## Assets

Wallpaper assets must be project-owned or otherwise cleared for public redistribution before this repository is published.
