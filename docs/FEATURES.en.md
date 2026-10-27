# GT-100 USB Editor improvements

[Português (Brasil)](FEATURES.md) · **English**

[← Main page](../README.en.md) · [Download for Windows](../windows/README.en.md) · [Acknowledgments](../README.en.md#acknowledgments)

GT-100 USB Editor modernizes the experience of editing the BOSS GT-100. This page covers the improvements the project adds: a new interface with Brazilian Portuguese support, Assign shortcuts, automatic scenes, Pseudo IR, setting copying, and edit history.

## Modernized interface

The new interface brings the signal chain and the selected effect's parameters together on one screen. Block states and the A/B signal paths are shown visually, and effects can be reordered by dragging them.

Knobs support dragging, fine adjustment with **Shift**, and numeric entry. The vector interface follows Windows display scaling. Changes received from the processor update the editor.

## Brazilian Portuguese support

In addition to English, the editor offers a **Brazilian Portuguese** interface, with translated menus, controls, and messages. To change the language, open **Settings → Language** and select **Português (Brasil)**. English is the application's default language.

Your language preference is kept for the next launch. Patch names and other user data are preserved when changing the interface language.

## Copying settings and protecting saved patches

Copy and paste settings between compatible blocks through the context menu to reuse your adjustments. You can also copy a complete tone to another user patch slot.

## Assign shortcuts

Right-click a compatible knob or switch and choose **Assign → Assign 1–8**. The editor fills in the target and its limits, making it easier to link that parameter to a pedal or controller.

The Assign source, mode, and state remain available for configuration. Parameters without a compatible target do not offer the shortcut; resources used by scenes are protected against conflicts.

## Scenes with automatic configuration

Prepare a **Standard** configuration and variations for **ACCEL** and **LOOP** within the same patch. The editor compares the settings and organizes the pedal functions and Assigns needed to switch between them.

You can review the resources used and check the result before saving. Scenes depend on the GT-100's controls and **eight physical Assign slots**: the number of differences between configurations determines what can be generated. Once saved in the patch, the configured changes are carried out by the processor itself.

## Pseudo IR

Pseudo IR uses a **cabinet IR in WAV format as a reference** and searches for internal GT-100 settings that approximate its frequency response. This lets you save the configuration in a patch and use the processor without a computer.

### Watch how it works

**English · 3:44 · visual explanation, without narration.** The video covers fixed and CUSTOM cabinets, Color, expanded search, both EQ priorities, FX types and order, individual EQ contributions, guitar previews and the null test.

https://github.com/user-attachments/assets/1e754c09-5605-4b4a-804e-ede91b7fbcee

[Chapters and full explanation](pseudo-ir/en/README.md) · [Download MP4](pseudo-ir/en/how-it-works.mp4) · [English captions](pseudo-ir/en/captions.en.vtt)

### Import and compare

1. Open the **Pseudo IR** page and add a WAV IR.
2. Review the selected cabinet and the calculated versions.
3. Compare the graph and listen to the alternatives using the application's guitar samples.
4. Choose a version and apply it to the desired preamp channel.
5. Test the tone on the processor and use **WRITE** to keep the result.

Each conversion offers four trade-offs between approximation and resource use:

| Version | Blocks used |
| --- | --- |
| Cabinet only | The preamp's cabinet and microphone simulation |
| Cabinet + EQ | Cabinet and dedicated equalizer |
| Cabinet + EQ + 1 FX | Cabinet, EQ, and one FX configured as an equalizer |
| Cabinet + EQ + 2 FX | Cabinet, EQ, and both FX blocks configured as equalizers |

Using more EQs occupies blocks that you might want to reserve for other effects. With the one-FX version, you can choose **FX1** or **FX2**. FX blocks can use parametric or graphic EQ, with at most one graphic EQ. The search also compares mixed block orders to reduce predicted intermediate gain.

The default search includes **CUSTOM cabinets**, experimental **Low/High Color** predictions, and **expanded Color + EQ search**. It refines several promising bases and selects one cabinet using the result with EQ + 2 FX; the four versions then share that base. Both **80 Hz–6 kHz** and **200 Hz–5 kHz** EQ fitting strategies are compared, with automatic selection by full-band error. **Nerd Mode** exposes these choices and each EQ's contribution for closer comparison.

Use **Prepare preview** with the GT-100 connected and the selected patch preamp enabled. It prepares **Open Chords, Power Chords and Melody**, restoring the patch before listening and reusing valid cached previews. Compare the recorded preamp convolved with the original IR against recordings through the GT-100 cabinet and EQ blocks. You can switch versions, pause, loop and choose the playback output. Conversions are kept in your library for reuse.

### Interpreting the result

The goal is to approximate the **magnitude of the frequency response** within the analyzed range. The proximity percentage compares spectral shape after aligning volume; it is not a percentage of sonic or perceptual fidelity.

Nerd Mode also offers a **waveform null test** on prepared preview audio. This phase-sensitive residual is a separate diagnostic; it does not rank cabinet candidates or express a percentage of audible fidelity.

The GT-100 **does not load the WAV file or run IRs**. The patch uses its own cabinets and equalizers. Phase, time response, and the original IR's dynamic behavior are not fully reproduced. The conversion curves remain magnitude predictions; check the result with your guitar and output system. Pseudo IR remains under development.

## Undo and redo

Use **Ctrl+Z** to undo and **Ctrl+Y** or **Ctrl+Shift+Z** to redo edits to the current patch. The history groups a knob drag into a single action and covers parameters, on/off states, chain order, Assigns, and other editing operations. Switching or reloading the patch, saving, or disconnecting starts a new history.

[Back to the main page](../README.en.md)
