# Ergodox EZ Configuration

This repository contains my custom configuration for the [Ergodox EZ](https://ergodox-ez.com/) keyboard. 

My layout is optimized for macOS

- `keymap.json` - Keymap file for use with [QMK Configurator](https://config.qmk.fm/#/ergodox_ez/LAYOUT_ergodox)
- `keymap/` - Backup of keymap source code in case the QMK Configurator ever goes offline.
- `ergodox_ez_keymap.hex` - Backup of compiled keyboard firmware, tracked in Git LFS

This keymap is geared towards macOS since that's where I spend most of my time typing. If you want to use this with Linux, swap OS for another Ctrl and put the Insert and Delete keys somewhere.

# How to Flash

## macOS

Use [Teensy Loader](https://www.pjrc.com/teensy/loader_mac.html)

## Arch Linux

```bash
# Install teensy loader
pacman -Syu teensy-loader-cli
# Flash the firmware
teensy-loader-cli -mmcu=atmega32u4 -w ergodox_ez_keymap.hex
# Push the reset button on the keyboard with a paper clip or pushpin
```
