# MechWild Firmware

Prebuilt firmware for MechWild products. 

Use [the releases section on the right of the page](https://github.com/MechWild/mw_firmware/releases) to download prebuilt binaries for each board that you are interested in.

The firmware here is intended to provide functionality unavailable through [QMK Configurator](https://config.qmk.fm/). Primarily this means compatibility with dynamic remapping tools like [Vial](https://get.vial.today) and [VIA](https://usevia.app), but also experiments and pre-release firmware.

If you have feedback that needs to be addressed, please feel to open an issue stating the problem you are facing.

## Common Questions/Problems

### Which file do I choose?

#### BlackPill boards (OBE, Waka60, PuckBuddy...)

- **All boards should use `F401` firmware files unless you know exactly why not.** The only BlackPills MechWild currently sells are the [F401](https://mechwild.com/product/blackpill/) model, so there is a 99% chance this means you!
- **If your board has an EEPROM chip installed, you may use the `eeprom` firmware.** If it doesn't, avoid anything with `eeprom` in the filename.

**`vial` files are built for [Vial](https://get.vial.today). `via` files are built for [VIA](https://usevia.app).** While the Vial program will often work with VIA keyboards and vice versa, that may not always be true. If you know you will be using a specific program, flash with the appropriate firmware for maximum compatibility.

### What do I do with these files?

First, download the appropriate zip file from [Releases](https://github.com/MechWild/mw_firmware/releases) and extract the contents.

The firmware of your choice will need to be flashed onto your keyboard. Instructions for doing this can likely be found in [your board's build guide](https://mechwild.com/guides/build-guides/).

If there is a `*_via_layout_defn.json` file in the zip, you may need to sideload this file to make the board remappable in VIA.

### I downloaded a .hex/.bin/.uf2 file from GitHub and flashed it, but nothing changed!

If QMK Toolbox looks like the following, the flash didn't complete because the file is corrupt.

![QMK Toolbox screenshot of a failed flash](https://cdn.discordapp.com/attachments/837441710698004531/1000516201551773827/unknown.png)

Please use [the releases page](https://github.com/MechWild/mw_firmware/releases) for downloads instead of hunting through the repo; that's why it's there!
