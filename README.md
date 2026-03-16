# SynthVoice by theRealla 🦭

**An EMS-style Erica SynthVoice-inspired synthesizer** built with **Amorph** AI — no heavy coding required, just pure prompt magic turned into a playable VST/AU/CLAP/Standalone plugin.

Created by **Lewis Seals Jr** (aka **theRealla**), Memphis rapper, producer, and plugin experimenter under Organic Music LLC.

## About This Project

This is my first public Amorph-generated instrument: a warm, analog-flavored synth voice reminiscent of classic EMS Synthi systems — think rich filters, modulation, and experimental sound design perfect for rap beats, ambient layers, or glitchy Memphis productions.

- **Prompt inspiration**: "EMS-STYLE Erica SynthVoice-like synthesizer with EMS filter, warm analog tones, versatile modulation, and sidechain-friendly dynamics"
- **Tech stack**: Amorph (prompt → Cmajor code) → cmaj generate → JUCE export → multi-format builds
- **Formats available**: VST3, AU (macOS), CLAP, Standalone app (Windows/macOS). AAX possible with SDK.

Perfect for DAWs like Ableton, FL Studio, Reaper, Logic, or Pro Tools.

## Screenshots

### Amorph in Action (Prompt to Plugin)

![Amorph Interface Screenshot](images/amorph-screenshot.png)
*(Amorph DSP sandbox: Type your idea, compile, and play — here's the lab view with generated parameters like FM Index, Ratio, Feedback, etc.)*

### Generated SynthVoice UI Example

![SynthVoice Plugin UI](images/synthvoice-ui.png)
*(The compiled plugin interface — classic EMS-style matrix patching, oscillators, filters, and envelope controls for deep sound sculpting.)*

### EMS Synthi Inspiration

![EMS Synthi Vintage Synth](images/ems-synthi.jpg)
*(Classic EMS Synthi hardware that inspired the sound — pin matrix, joystick, quirky oscillators — my version brings that vibe into modern DAWs.)*

### In a DAW (Reaper/FL Example)

![Plugin in DAW](images/plugin-in-daw.png)
*(Loaded in a DAW session — ready to drop on beats or experimental tracks.)*

(Upload your actual screenshots to `/images/` folder in the repo for best results. If you don't have them yet, grab similar ones from Amorph demos or EMS pics online.)

## How to Build & Use

1. **Prerequisites** (one-time setup):
   - Download **cmaj** CLI: https://github.com/cmajor-lang/cmajor/releases
   - Install **CMake** (cmake.org)
   - Download **JUCE** framework (juce.com)
   - (Optional) Avid AAX SDK for Pro Tools support

2. **Build the Plugin**:
   - Clone this repo
   - Run the builder script (or manually):
     ```bash
     cmaj generate --target=juce SynthVoice.cmajorpatch --output=Builds
     cd Builds/SynthVoice_JUCE
     cmake -B Build -DJUCE_BUILD_VST3=ON -DJUCE_BUILD_AU=ON -DJUCE_BUILD_CLAP=ON
     cmake --build Build --config Release
     ```
   - Find your plugins in `Build/` (e.g., `SynthVoice.vst3`, `SynthVoice.component`, etc.)

For a one-file builder .exe (Windows), check my separate script repo or use PyInstaller locally.

## Installation

- Copy the built plugin files to your DAW's plugin folder:
  - Windows: `C:\Program Files\Common Files\VST3\`
  - macOS: `~/Library/Audio/Plug-Ins/Components/` (AU) or `/VST3/`
- Rescan plugins in your DAW.

## License

MIT License — feel free to fork, modify, and use in your productions. Credit appreciated: "SynthVoice by theRealla (Lewis Seals)".

## Connect

- 🎤 X / Twitter: [@realla_the](https://x.com/realla_the)
- 🌐 GitHub: [TheRealla](https://github.com/TheRealla)
- 🎵 Music & more: Search "theRealla" on streaming platforms

Drop a star ⭐ if this inspires your beats! Let's collab on more Amorph experiments — Memphis sound meets AI DSP.

🦭 Made in Memphis, TN | 2026
