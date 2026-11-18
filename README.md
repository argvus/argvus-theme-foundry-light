# Foundry Light theme for ARGVUS

ARGVUS Light theme, `foundry-light`, with its Sticky and Float layouts.

## Theme identity

| Field | Value |
| --- | --- |
| Theme ID | `foundry-light` |
| Display name | Foundry Light |
| Mode | `light` |
| Package | `argvus-theme-foundry-light` |
| Wallpaper | `/usr/share/backgrounds/argvus/abstract/light/foundry-light-abstract-light.jxl` |

The theme is `src/usr/share/argvus/themes/foundry-light/theme.toml`: its name,
category, wallpaper and palette. Every component of the desktop renders its
files from that palette when the theme is applied, so the manifest and the
wallpaper are the whole package.

The original palette pairs light steel gray and graphite with an oxidized copper highlight (`#783D2A`).
The abstract wallpaper depicts overlapping steel plates under hard side lighting and was generated with ImageGen.

## Working on the theme

```sh
make check     # render every component in both layouts and report errors
make try       # install it as your own theme, then: argvus theme apply foundry-light
make untry     # remove that copy
make validate  # repository and packaging checks
make build     # build the package into build/dist/
make install   # install the package (sudo pacman -U)
```

Git installation reads the theme files from `src/`; `packaging/` is optional and only used to build Arch Linux packages. Publish this repository with its wallpaper. Users can install it with
`argvus theme install https://HOST/USER/argvus-theme-foundry-light.git`,
apply it with `argvus theme apply foundry-light`, and remove it with
`argvus theme uninstall foundry-light`. Installed themes appear in Custom themes.

See [DEVELOPMENT.md](DEVELOPMENT.md) for the build and release details.

## License

GPL-3.0-only. See [LICENSE](LICENSE).
