# Brain Fuzzer

A neuroscience-grounded visual stimulation tool that explores the boundaries of human visual perception by targeting specific dopaminergic pathways, neural oscillation frequencies, and perceptual processing mechanisms through precisely crafted visual stimuli.

**WARNING: This program produces intense visual stimulation including stroboscopic flicker, looming motion, and luminance transients. It may cause disorientation, afterimages, nausea, or discomfort. Not recommended for individuals with photosensitive epilepsy or similar conditions. Stroboscopic effects in the 4-45 Hz range can trigger seizures in susceptible individuals.**

<img width="811" height="836" alt="image" src="https://github.com/user-attachments/assets/6fd85252-2ec9-4e17-83f8-ea6d1ede2279" />

## Features

- **21 Visual Effects** spanning geometric, post-processing, and neuroscience-grounded perceptual exploits
- **6 Color Modes**: Psychedelic, fire, ice, matrix, monochrome, and dopamine (warm/red/high-saturation for DA/norepinephrine arousal)
- **Brain-Mode Sequencer**: Auto-cycles through 10 neuroscience-timed effect sequences targeting different dopamine pathways
- **13 Built-in Presets** including dopamine-stack, subcortical, gamma-red, and curiosity
- **Real-time Controls**: 30+ keyboard shortcuts for intensity, chaos, effect toggles, and brain-mode activation
- **Fullscreen Support**: Auto-detects native display resolution (tested at 4K)
- **Preset System**: Save and load custom configurations as JSON
- **Session Management**: Set duration limits or run indefinitely

## Neuroscience Foundations

The effects are designed around documented perceptual and dopaminergic mechanisms:

| Effect | Neural Target | Pathway |
|--------|--------------|---------|
| **Looming** | Superior colliculus | SC->VTA subcortical fast lane (70-150ms) |
| **Luminance Transients** | Lateral nucleus accumbens | Direct photonic DA release (peaks 434ms) |
| **Stroboscopic Flicker** | Visual cortex oscillations | Alpha (8-13Hz) / Gamma (34-40Hz) entrainment |
| **Novelty Injector** | VTA prediction error | Variable ratio reinforcement schedule |
| **Ambiguity Resolve** | OTC->vmPFC->striatum | Perceptual curiosity/dopamine loop |
| **Motion Aftereffect** | V5/MT direction neurons | Neuron fatigue -> waterfall illusion |
| **Peripheral Drift** | Retinal motion detectors | Asymmetric luminance (Kitaoka-style) |
| **Ganzfeld** | Cortical pattern generators | Perceptual deprivation -> hallucination |
| **Hermann Grid** | Retinal ganglion cells | Lateral inhibition -> illusory spots |
| **Opponent Color** | Cone photoreceptors | Opponent-process fatigue -> afterimages |
| **Moire Patterns** | Spatial frequency processing | Interference -> phantom motion |

## Requirements

- Python 3.10 or higher
- pygame 2.x
- numpy 2.x

## Installation

```bash
# Clone the repository
git clone https://github.com/geeknik/brain-fuzzer.git
cd brain-fuzzer

# Create virtual environment (recommended)
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Run the fuzzer
python main.py
```

## Usage

### Basic Usage

```bash
# Run with defaults (800x800 window, 2 minutes)
python main.py

# Fullscreen mode (auto-detects native resolution)
python main.py --fullscreen --intensity 0.9

# 60-second session with maximum chaos
python main.py --duration 60 --chaos 0.8

# Custom resolution
python main.py --width 1920 --height 1080
```

### Brain Fuzzing Presets

```bash
# Dopamine stack - hits all three DA pathways simultaneously
python main.py --preset dopamine-stack --fullscreen

# Auto-sequenced brain assault (10 phases, ~167s cycle)
python main.py --preset full-brain --fullscreen

# Pure gamma entrainment (36Hz red light, strongest gamma waves)
python main.py --preset gamma-red --fullscreen

# Curiosity/dopamine loop (blur-to-resolve + variable reward)
python main.py --preset curiosity --fullscreen --duration 0

# Subcortical pathway targeting (looming + luminance transients)
python main.py --preset subcortical --fullscreen
```

### Classic Presets

```bash
# List all built-in presets
python main.py --list-presets

# Load a preset
python main.py --preset mellow

# Save current config and exit
python main.py --width 1920 --height 1080 --save-preset my_config.json

# Load custom preset
python main.py --preset my_config.json
```

### Brain Effect Flags

```bash
# Enable specific brain effects
python main.py --looming --luminance-transient --novelty-injector

# Stroboscopic with custom frequency
python main.py --stroboscopic --strobe-freq 10

# Gamma entrainment mode (36Hz red light)
python main.py --stroboscopic --gamma-mode

# Full brain mode sequencer
python main.py --brain-mode --fullscreen

# Combine with classic effects
python main.py --looming --moire --aftereffect --color-mode dopamine
```

### Classic Effect Control

```bash
# Disable specific effects
python main.py --no-flicker --no-distortion

# Matrix-style visuals only
python main.py --color-mode matrix --no-flicker

# Minimal configuration
python main.py --intensity 0.5 --chaos 0.1 --no-fractals --no-particles
```

## Keyboard Controls

### General

| Key | Action |
|-----|--------|
| `+` / `-` | Increase/decrease intensity |
| `C` / `V` | Increase/decrease chaos level |
| `Up` / `Down` | Increase/decrease rotation speed |
| `SPACE` | Toggle high contrast flicker mode |
| `M` | Cycle through color modes |
| `P` | Pause/resume |
| `R` | Randomize all parameters |
| `S` | Save current config to timestamped file |
| `H` | Show/hide help overlay |
| `ESC` / `Q` | Quit |

### Classic Effects (number keys)

| Key | Effect |
|-----|--------|
| `1` | Toggle flicker |
| `2` | Toggle waves |
| `3` | Toggle spirals |
| `4` | Toggle tesseract |
| `5` | Toggle fractals |
| `6` | Toggle particles |
| `7` | Toggle distortion |
| `8` | Toggle scanlines |
| `9` | Toggle chromatic aberration |
| `0` | Toggle CRT |

### Brain Effects (function keys)

| Key | Effect | Dopamine Pathway |
|-----|--------|-----------------|
| `F1` | Stroboscopic flicker | Alpha/gamma entrainment |
| `F2` | Moire interference | Spatial frequency processing |
| `F3` | Motion aftereffect | V5/MT neuron fatigue |
| `F4` | Peripheral drift | Asymmetric luminance motion |
| `F5` | Ganzfeld | Perceptual deprivation |
| `F6` | Hermann grid | Lateral inhibition |
| `F7` | Opponent color | Cone fatigue afterimages |
| `F8` | Looming | SC->VTA subcortical (fastest) |
| `F9` | Luminance transient | Direct LNAc dopamine |
| `F10` | Novelty injector | Variable ratio reward |
| `F11` | Ambiguity resolve | Curiosity/dopamine loop |
| `G` | Gamma mode (36Hz red) | Cortical gamma entrainment |
| `B` | Brain-mode sequencer | Auto-cycles all pathways |

## Visual Effects

### Classic Effects

- **Tesseract**: Rotating 4D hypercube projection with motion trails
- **Fractals**: Recursive geometric patterns with random branching
- **Spirals**: Hypnotic multi-armed spiral patterns
- **Waves**: Oscillating sine wave distortions
- **Particles**: Dynamic particle system with physics simulation
- **Flicker**: Time-based periodic background noise (refactored for proper entrainment)
- **Distortion**: Screen jitter and radial blur
- **Chromatic Aberration**: RGB channel separation for color fringing
- **Scanlines**: CRT-style horizontal scanlines with scrolling
- **CRT**: Vignette, phosphor glow, and monitor simulation

### Brain Effects (Neuroscience-Grounded)

- **Stroboscopic**: Multi-band flicker — alpha (8-13 Hz) for relaxed-alert entrainment, gamma (34-40 Hz) with red light for strongest cortical gamma synchronization
- **Moire**: Overlapping rotating line grids creating interference patterns — phantom motion and texture from spatial frequency processing
- **Motion Aftereffect**: Continuously expanding/contracting log-spiral — fatigues direction-selective neurons in V5/MT, causing waterfall illusion on stationary surfaces
- **Peripheral Drift**: Kitaoka-style asymmetric luminance patterns (dark-medium-light-black) — appears to rotate in peripheral vision while stationary under direct fixation
- **Ganzfeld**: Slowly pulsating uniform color field — perceptual deprivation induces hallucinatory percepts as the brain seeks structure in structureless input
- **Hermann Grid**: White/colored lines on dark background — lateral inhibition in retinal ganglion cells creates illusory dark spots at intersections
- **Opponent Color**: Saturated color field with fixation cross, then neutral gray — cone fatigue produces complementary afterimages via opponent-process theory
- **Looming**: Radially expanding shapes completing in 200-500ms — one of the most potent activators of the superior colliculus, driving dopamine via the subcortical fast lane at 70-150ms
- **Luminance Transient**: Sharp dark-to-light transitions at variable intervals — directly triggers dopamine transients in lateral nucleus accumbens, peaking ~434ms post-onset, independent of reward history
- **Novelty Injector**: Variable ratio reward schedule delivering unexpected high-salience visual events — anticipation cues build tension before payoff, matching the VR pattern that produces the highest sustained dopamine response rates
- **Ambiguity Resolve**: Blur-to-clarity cycles — degraded shapes at intermediate confidence (peak curiosity) activate anterior insula/ACC, resolution activates striatal reward regions

## Color Modes

- **Psychedelic**: Full spectrum HSV color cycling
- **Fire**: Red-orange-yellow gradient with heat effects
- **Ice**: Blue-cyan palette with cool tones
- **Matrix**: Green phosphor terminal aesthetic
- **Monochrome**: Grayscale intensity variations
- **Dopamine**: Warm red-orange-yellow with high saturation — red increases beta wave activity and drives DA/norepinephrine arousal

## Built-in Presets

### Classic

- **mellow**: Low intensity (0.4), minimal chaos (0.2), ice colors
- **intense**: Maximum intensity (1.0), high chaos (0.8), fire colors
- **matrix**: Green terminal aesthetic, moderate intensity (0.6), flicker disabled
- **minimal**: Simple effects only, no fractals or particles
- **chaos**: Maximum everything with high contrast flicker

### Brain Fuzzing

- **dreamachine**: Alpha-wave stroboscopic (10 Hz) + ganzfeld — Brion Gysin principle
- **perception**: Moire + aftereffect + peripheral drift + Hermann grid — monochrome perceptual exploits
- **full-brain**: All 11 brain effects enabled + brain-mode auto-sequencer
- **afterimage**: Opponent color + ganzfeld — focused afterimage induction
- **dopamine-stack**: Looming + luminance transients + novelty injector + stroboscopic — hits SC->VTA, LNAc, and VR reward pathways simultaneously
- **subcortical**: Looming + luminance transients + motion aftereffect — subcortical pathway focus with dopamine color mode
- **curiosity**: Ambiguity resolve + novelty injector + ganzfeld — curiosity/dopamine loop
- **gamma-red**: 36 Hz red-light stroboscopic + looming — strongest gamma wave entrainment extending beyond visual cortex

## Brain-Mode Sequencer

When activated (`B` key or `--brain-mode`), automatically cycles through 10 neuroscience-timed sequences:

1. **Subcortical Blast** (12s) — Looming + luminance transients
2. **Alpha Entrainment** (15s) — Stroboscopic + ganzfeld
3. **Curiosity Loop** (18s) — Ambiguity resolve + novelty injector
4. **Motion Fatigue** (20s) — Motion aftereffect + moire
5. **Peripheral Assault** (15s) — Peripheral drift + Hermann grid
6. **Color Opponent** (20s) — Opponent color + ganzfeld
7. **Dopamine Stack** (15s) — Looming + luminance transients + novelty injector
8. **Full Spectrum** (12s) — Stroboscopic + moire + aftereffect + peripheral drift + looming + novelty
9. **Deep Ganzfeld** (25s) — Ganzfeld alone (extended deprivation)
10. **Gamma Entrainment** (15s) — Stroboscopic (gamma) + looming

Total cycle: ~167 seconds, then repeats.

## CLI Arguments

### Display Options

- `-W`, `--width`: Window width (default: 800)
- `-H`, `--height`: Window height (default: 800)
- `-f`, `--fullscreen`: Fullscreen mode (auto-detects native resolution)
- `--fps`: Target frame rate (default: 60)

### Session Options

- `-d`, `--duration`: Session duration in seconds (0 = infinite, default: 120)
- `-i`, `--intensity`: Effect intensity 0.1-1.0 (default: 0.7)
- `-c`, `--chaos`: Chaos level 0.0-1.0 (default: 0.5)
- `--color-mode`: Color palette (psychedelic|fire|ice|matrix|monochrome|dopamine)
- `--high-contrast`: Enable high contrast flicker mode

### Classic Effect Toggles

- `--no-tesseract`: Disable tesseract effect
- `--no-fractals`: Disable fractal effect
- `--no-spirals`: Disable spiral effect
- `--no-waves`: Disable wave effect
- `--no-particles`: Disable particle effect
- `--no-flicker`: Disable flicker effect
- `--no-distortion`: Disable distortion effect
- `--no-chromatic`: Disable chromatic aberration
- `--no-scanlines`: Disable scanline effect
- `--no-crt`: Disable CRT effect

### Brain Effect Enables

- `--stroboscopic`: Enable stroboscopic flicker
- `--strobe-freq`: Stroboscopic frequency in Hz (default: 10, range: 4-45)
- `--gamma-mode`: Force 36Hz red-light gamma entrainment
- `--moire`: Enable Moire interference patterns
- `--aftereffect`: Enable motion aftereffect spiral
- `--peripheral-drift`: Enable peripheral drift illusion
- `--ganzfeld`: Enable Ganzfeld effect
- `--hermann-grid`: Enable Hermann grid
- `--opponent-color`: Enable opponent-color afterimage induction
- `--looming`: Enable looming effect (SC->VTA pathway)
- `--luminance-transient`: Enable luminance transients (direct LNAc DA)
- `--novelty-injector`: Enable novelty injector (variable ratio reward)
- `--ambiguity-resolve`: Enable ambiguity-resolve (curiosity/dopamine loop)
- `--brain-mode`: Enable brain-mode auto-sequencer

### Preset Management

- `-p`, `--preset`: Load preset (built-in name or JSON file path)
- `--save-preset`: Save current config to JSON and exit
- `--list-presets`: List built-in presets and exit

### Debug Options

- `-v`, `--verbose`: Enable verbose logging
- `-q`, `--quiet`: Quiet mode (errors only)
- `--skip-intro`: Skip startup animation

## Examples

```bash
# Gentle introduction
python main.py --preset mellow --duration 30

# Full sensory overload
python main.py --fullscreen --preset chaos

# Dopamine stack — all three DA pathways simultaneously
python main.py --preset dopamine-stack --fullscreen

# Auto-sequenced brain assault
python main.py --preset full-brain --fullscreen --duration 0

# Pure gamma entrainment (36Hz red light)
python main.py --preset gamma-red --fullscreen

# Curiosity/dopamine loop
python main.py --preset curiosity --fullscreen --duration 0

# Custom brain cocktail
python main.py --looming --luminance-transient --stroboscopic --strobe-freq 10 --color-mode dopamine --fullscreen

# Custom matrix experience
python main.py --color-mode matrix --intensity 0.8 --no-flicker --fps 120

# Performance testing
python main.py --fps 144 --verbose --duration 60

# Create and use custom preset
python main.py --intensity 0.6 --chaos 0.4 --color-mode ice --save-preset ice_calm.json
python main.py --preset ice_calm.json --fullscreen
```

## Technical Details

- Built with pygame for cross-platform graphics
- NumPy for efficient array operations (chromatic aberration, CRT effects)
- 4D rotation matrices for tesseract projection
- Recursive fractal generation with depth limiting
- Real-time particle physics simulation
- Time-based phase accumulation for all periodic effects (not frame-dependent)
- Multi-layered rendering pipeline with 21 compositable effects
- Fullscreen auto-detects native display resolution via `pygame.display.Info()`
- Brain-mode sequencer auto-creates effects on-the-fly as needed

## License

[MIT License](LICENSE)

## Safety Notice

This software is intended for visual perception research and artistic exploration. Users should:

- Take breaks every 15-20 minutes
- **Avoid use if you have photosensitive epilepsy** — stroboscopic effects (4-45 Hz) can trigger seizures
- Stop immediately if you experience discomfort, nausea, or disorientation
- Be aware that gamma-mode (36Hz red light) is particularly intense
- Observe aftereffects (afterimages, visual persistence, motion aftereffects) as part of the experience
- Use responsibly and at your own risk
