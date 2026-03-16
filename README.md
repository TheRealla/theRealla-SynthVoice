# SynthVoice by theRealla 🦭

**EMS-style Erica SynthVoice-inspired synthesizer**  
Built with **Amorph** AI → Cmajor → JUCE — turned into real plugins with zero heavy coding.

Created by **Lewis Seals Jr** (aka **theRealla**), Memphis rapper, producer, and AI-plugin experimenter under Organic Music LLC.

## About

My first public Amorph-generated instrument: a warm, analog-flavored synth voice inspired by classic EMS Synthi systems. Rich filters, deep modulation, experimental vibes — perfect for rap beats, ambient textures, glitchy Memphis productions, or sidechained drops.

- **Original Amorph prompt**  
  "EMS-STYLE Erica SynthVoice-like synthesizer with EMS filter, warm analog tones, versatile modulation, and sidechain-friendly dynamics"

- **Tech**  
  Amorph (text prompt → Cmajor code) → `cmaj generate` → JUCE project → multi-format builds

- **Formats**  
  VST3 • AU (macOS) • CLAP • Standalone (Win/macOS) • AAX (with SDK)

Works in Ableton, FL Studio, Reaper, Logic, Pro Tools, and more.

## Screenshots

(Add your real images to the `Images/` folder soon for best results!)

### Amorph Prompt → Plugin
*(Amorph DSP sandbox: enter idea → generate parameters like FM Index, Ratio, Feedback...)*

### SynthVoice Plugin UI
*(Compiled interface: EMS-style matrix patching, oscillators, filters, envelopes)*

### Classic EMS Synthi Inspiration
*(Vintage hardware reference: pin matrix, joystick, quirky oscillators — the soul of the sound)*

### Loaded in a DAW
*(Ready to play — drop it on beats or experimental tracks)*

## How to Build (Recommended: Use the Script)

1. **Prerequisites** (one-time)
   - [cmaj CLI](https://github.com/cmajor-lang/cmajor/releases) — add to PATH
   - [CMake](https://cmake.org/download/)
   - [JUCE](https://juce.com/get-juce) — unzip somewhere (e.g. `~/JUCE`)
   - (Optional) Avid AAX SDK for Pro Tools format

2. **Easiest way — use the builder script**
   - Download `build_synthvoice_all.py` from this repo (or the separate script repo if separate)
   - Place it next to `SynthVoice.cmajorpatch`
   - Run:
     ```bash
     python build_synthvoice_all.py
     ```
     Or with options:
     ```bash
     python build_synthvoice_all.py --juce ~/JUCE --aax-sdk ~/AAX_SDK
     ```

   → Builds VST3 / Standalone / CLAP / AU (macOS) automatically. Check `Builds/` folder for plugins.

3. **Manual build (alternative)**
   ```bash
   # Generate JUCE project
   cmaj generate --target=juce SynthVoice.cmajorpatch --output=Builds --jucePath ~/JUCE

   # Build
   cd Builds/SynthVoice_JUCE
   cmake -B Build -DCMAKE_BUILD_TYPE=Release \
     -DJUCE_BUILD_VST3=ON -DJUCE_BUILD_CLAP=ON -DJUCE_BUILD_Standalone=ON
   cmake --build Build --config Release --parallel
   
## License

MIT License — feel free to fork, modify, and use in your productions. Credit appreciated: "SynthVoice by theRealla (Lewis Seals)".

## Connect

- 🎤 X / Twitter: [@realla_the](https://x.com/realla_the)
- 🌐 GitHub: [TheRealla](https://github.com/TheRealla)
- 🎵 Music & more: Search "theRealla" on streaming platforms

Drop a star ⭐ if this inspires your beats! Let's collab on more Amorph experiments — Memphis sound meets AI DSP.

🦭 Made in Memphis, TN | 2026
