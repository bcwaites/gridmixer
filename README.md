# Grid Mixer

A browser-based percussion "grid" exercise generator for marching band and drumline practice — part of the Marimba Warehouse suite of music tools (alongside Groove Mixer and Melody Mixer).

Grid Mixer generates randomized sticking/accent/ornament exercise patterns, renders them as real music notation, and plays them back with a synthesized snare sound — so a director or student can generate a fresh accent-grid or rudiment drill, hear it, print it, and share it, all in one page with no install.

## Features

- **Subdivisions**: straight 16th notes or 16th-note triplets ("Triplets")
- **Sticking**: built-in rudiment presets (alternating, doubles, paradiddle, paradiddle-diddle, triple paradiddle) or a fully custom R/L editor
- **Accent Grid**: three modes —
  - *Static*: hand-pick fixed accent positions
  - *Rotating*: a single accent that shifts by beat / 2 beats / measure, forward or backward
  - *Mixed*: density-based random accents that vary independently every measure
- **Flams & Drags/Diddles**: independent density and eligible-position controls for each, with a Fixed/Mixed pattern mode (Fixed repeats the same pattern every measure; Mixed rolls a fresh pattern per measure so longer phrases don't just loop the same bar)
- **Release Measure**: optional trailing measure (one quarter-note stroke + three quarter rests) that acts as an ending cue and, combined with Loop, doubles as a 1-bar recount before the pattern repeats
- **Playback**: synthesized snare (layered filtered-noise snap + pitched thump), tempo control, 2-bar count-in, metronome, loop, strong accent/unaccented velocity contrast (125% vs. 25%)
- **Mixer**: horizontal Stroke / Click / Master volume strip in the top toolbar
- **Notation**: real engraved music notation via [OpenSheetMusicDisplay](https://opensheetmusicdisplay.org/), including correct flam/drag/tremolo/tuplet rendering
- **Share & export**: shareable settings links (full generator state encoded in the URL) and Save-as-PDF via the browser print dialog, both accessible from the top toolbar

## Usage

This is a single self-contained HTML file — no build step, no server, no dependencies to install.

1. Open `index.html` in any modern browser (or visit the GitHub Pages URL for this repo, if enabled).
2. Set your subdivision, sticking, accents, flams/drags, and measure count in the left sidebar (defaults to a 2-measure, alternating-sticking, rotating-accent-every-beat grid).
3. Click **MIX IT UP!** to generate a new pattern.
4. Click **Play** to hear it, or **Save Grid (PDF)** to print it.

All libraries (notation rendering and audio synthesis) are loaded from CDN at runtime — an internet connection is required on first load.

## Tech stack

- Vanilla JavaScript, HTML, CSS — no framework, no build tooling
- [OpenSheetMusicDisplay](https://opensheetmusicdisplay.org/) (v1.8.4, pinned) for MusicXML rendering
- [Tone.js](https://tonejs.github.io/) for audio synthesis and playback scheduling

## Project status

Actively developed. See commit history for the feature timeline — this tool started as an adaptation of Groove Mixer's UI shell, tailored specifically to drumline "grid" exercises (accent grids, rudiment drills, flam/drag placement), with the notation and audio engines built out iteratively based on director feedback.

## License

Add a license of your choice here (e.g. MIT) before making this repository public, if that's the intent.
