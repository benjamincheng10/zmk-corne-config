# ZMK Corne Config

Typeractive Corne 42-key wireless keyboard, nice!nano v2 controllers, ZMK firmware, macOS + US layout.

## Keymap

![Corne keymap](keymap-drawer/corne.svg)

## Generating Keymap SVG Locally

Requires [mise](https://mise.jdx.dev/). Run from the repo root:

```sh
mise install
pip install keymap-drawer==0.23.0
keymap -c keymap_drawer.config.yaml parse -z config/corne.keymap > keymap-drawer/corne.yaml
keymap -c keymap_drawer.config.yaml draw keymap-drawer/corne.yaml > keymap-drawer/corne.svg
```

The SVG is also regenerated automatically by GitHub Actions on push when keymap files change.

## References

- [urob/zmk-config](https://github.com/urob/zmk-config) — timeless homerow mods, Numword, combo-based symbols
- [TimothyBesada/zmk-corne-config](https://github.com/TimothyBesada/zmk-corne-config) — colleague's Corne setup

## Building

Push to `main` — GitHub Actions builds firmware automatically. Download `.uf2` artifacts from the [Actions tab](../../actions).

## Flashing

1. Connect nice!nano via USB
2. Double-tap the reset button — a USB drive appears
3. Copy the `.uf2` file to the drive
4. Flash left half first, then right half
