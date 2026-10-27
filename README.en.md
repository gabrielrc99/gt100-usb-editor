# GT-100 USB Editor

[Português (Brasil)](README.md) · **English**

GT-100 USB Editor aims to fight obsolescence by refreshing the experience of using this nearly 15-year-old effects processor. It brings a more modern interface and quality-of-life additions such as preset copying, Assign shortcuts on knobs, automatic scene-based Assign configuration, and **Pseudo IR**: a tool that uses guitar cabinet IRs as a reference to approximate their frequency response using only the GT-100's internal blocks.

**[Download the Windows alpha](https://github.com/gabrielrc99/gt100-usb-editor/releases/tag/v0.1.3-alpha.1)** · **[Explore the improvements](docs/FEATURES.en.md)**

![Current GT-100 USB Editor interface on Windows, shown in Brazilian Portuguese](docs/images/editor-windows.png)

## Download and getting started

**0.1.3 Alpha 1**, for **64-bit Windows**, is available as a [pre-release](https://github.com/gabrielrc99/gt100-usb-editor/releases/tag/v0.1.3-alpha.1). This is the end-user distribution. The alpha is still being tested.

- **Installer (.exe):** per-user installation, with shortcuts and an uninstaller.
- **Portable (.zip):** extract the archive and run `GT100-USB-Editor-Portable.exe`. Keep the `GT100-data` folder when moving or updating the application.

Install the [BOSS USB driver compatible with your GT-100 and Windows version](https://www.boss.info/us/support/by_product/gt-100/), connect the processor via USB, and open the editor. **You do not need to install Python or Tone Studio.**

## Added features

- **Modernized interface**, with an interactive effects chain, block reordering, and vector controls.
- **Brazilian Portuguese support**, alongside English, with language selection in the interface.
- **Assign shortcuts** on compatible knobs and switches.
- **Scenes with automatic Assign configuration**, using the GT-100's own resources.
- **Pseudo IR**, with cabinet matching and EQ fitting to approximate a conventional IR, a local library, and audio comparisons.
- **Preset and effect-setting copying**, with a backup of the destination before it is overwritten.
- **Undo and redo**, with an edit history for the current patch.

Pseudo IR approximates the frequency response using internal cabinets and EQs; it does not make the GT-100 load the WAV file or perform convolution. See the [feature guide](docs/FEATURES.en.md#pseudo-ir) for the available versions and limitations.

Edits affect the temporary patch. Use **WRITE** to save to the processor's memory; the editor backs up the destination before overwriting it.

## Planned features

- Extend scenes to external pedals and the numbered footswitches.

## License

GT-100 USB Editor is distributed under the [MIT license](LICENSE). Dependencies retain their own licenses and notices, which are included in the packages.

This alpha provides compiled Windows packages; publication of the application source code is planned for a later stage.

## Acknowledgments

A big thank you to **[GT-100 Fx FloorBoard](https://fxfloorboard.sourceforge.io/info.php?model=gt-100)**, which served as a reference for this project.

---

The **Windows packages** are available in the [alpha release](https://github.com/gabrielrc99/gt100-usb-editor/releases/tag/v0.1.3-alpha.1), with installer and portable versions. This is an independent project, unaffiliated with BOSS/Roland.
