# Coupled Harmonic Oscillator Visualization

<p align="center">
  <img src="https://img.shields.io/badge/vanilla-JavaScript-yellow?style=flat-square" alt="Vanilla JS">
  <img src="https://img.shields.io/badge/HTML5-Canvas-orange?style=flat-square" alt="HTML5 Canvas">
  <img src="https://img.shields.io/badge/license-MIT-blue?style=flat-square" alt="MIT License">
  <img src="https://img.shields.io/badge/no%20dependencies-✓-brightgreen?style=flat-square" alt="No Dependencies">
</p>

<p align="center">
  <strong>An interactive visualization demonstrating how linear oscillations create the illusion of circular motion through precise phase relationships.</strong>
</p>

<p align="center">
  <a href="#demo">View Demo</a> •
  <a href="#the-illusion">The Illusion</a> •
  <a href="#features">Features</a> •
  <a href="#the-mathematics">Mathematics</a> •
  <a href="#usage">Usage</a>
</p>

---

## 🎯 The Illusion

**Every ball moves only in a straight line through the center.** No ball ever travels in a curve — yet together they appear to rotate in a perfect circle!

This is the famous "Crazy Circle Illusion," and this visualization lets you explore the mathematics behind it by adjusting the **phase-angle coupling ratio (k)**.

| k = 0 | k = 0.5 | k = 1 ✓ | k = 2 |
|:-----:|:-------:|:-------:|:-----:|
| All synchronized | Elliptical pattern | **Perfect circle!** | Double phase |

The magic happens at **k = 1**, where each oscillator's phase exactly equals its line angle.

---

## ✨ Features

### Core Visualization
- **Phase-Angle Coupling Control (k)** — The key parameter that creates or breaks the illusion
- **Adjustable oscillator count (n)** — From 2 to 32 balls
- **Real-time parameter animation** — Smooth transitions between states
- **Multiple visualization modes:**
  - Phase Illusion (primary)
  - Hypocycloid/Spirograph
  - Side-by-side comparison

### Visual Options
- 🎨 **6 color themes** — Dark, Orange Glow, Purple Night, Deep Ocean, Sunset, Matrix
- 🌈 **Rainbow mode** — Balls cycle through the spectrum
- ✨ **Motion trails** — Visualize the actual linear paths
- 🔮 **Glow effects** — Beautiful ball rendering with gradients
- 📐 **Guide lines** — Show the straight-line axes
- ⭕ **Apparent circle** — Highlight the illusory circular path

### Educational Demo Mode
- **12-chapter guided tour** explaining the mathematics
- **Live parameter display** showing equations updating in real-time
- **Smooth animated transitions** between demonstration states
- **Status indicator** showing when the illusion is perfect or broken

### Export & Recording
- 📷 **Screenshot** — Save as PNG
- 🎬 **Video recording** — Export as WebM
- ⛶ **Fullscreen mode** — Immersive presentation

---

## 📐 The Mathematics

For **n** oscillators, each oscillator **i** (from 0 to n−1) follows these equations:

### Line Angle (fixed axis of oscillation)
```
αᵢ = π × i / n
```

### Phase Offset (with coupling ratio k)
```
φᵢ = k × αᵢ
```

### Position (Simple Harmonic Motion)
```
dᵢ(t) = 2R × cos(ωt − φᵢ)
xᵢ = dᵢ × cos(αᵢ)
yᵢ = dᵢ × sin(αᵢ)
```

### The Key Insight

When **k = 1**, the phase equals the line angle (φᵢ = αᵢ). This creates a special condition:

- At any instant, all oscillators lie on a circle of radius R
- The center of this apparent circle orbits at distance R from the true center  
- Each oscillator's amplitude is 2R, allowing it to pass through the origin

This is the mathematical inverse of projecting circular motion onto multiple lines — here we **reconstruct the circle** from properly-phased linear motions!

---

## 🎮 Usage

### Quick Start

1. Open `coupled_harmonic_oscillator.html` in any modern browser
2. Click **"▶ Demo Mode"** for a guided tour
3. Adjust the **k slider** to break and restore the illusion
4. Explore different **n values**, **themes**, and **visualization options**

### Keyboard Shortcuts

| Key | Action |
|-----|--------|
| `Space` | Play / Pause |
| `D` | Start demo mode |
| `Esc` | Exit demo mode |
| `F` | Toggle fullscreen |
| `S` | Take screenshot |
| `R` | Reset to defaults |
| `K` | Snap k to 1.0 (perfect illusion) |
| `L` | Toggle guide lines |
| `C` | Toggle apparent circle |
| `↑` `↓` | Adjust speed |
| `←` `→` | Adjust phase |
| `[` `]` | Change oscillator count |

### Presets

| Preset | Description |
|--------|-------------|
| **Perfect** | k=1, n=8 — The classic illusion |
| **Broken** | k=0.7 — See how off-values look |
| **Double** | k=2 — Double phase offset patterns |
| **Sync** | k=0 — All balls move together |
| **Chaos** | k=φ (golden ratio) — Never-repeating patterns |
| **YouTube** | Orange theme matching the famous video |
| **Hypnotic** | Slow with trails |
| **Rainbow** | Color-cycling balls |

---

## 🔬 Real-World Applications

This mathematical principle appears throughout science and engineering:

- **Three-phase AC power** — Uses 120° phase offsets (k=1 with n=3)
- **Fourier analysis** — Decomposing signals into oscillations
- **Molecular vibrations** — Coupled atomic oscillators in crystals
- **Quantum mechanics** — Wave function phase relationships
- **Signal processing** — I/Q modulation and demodulation
- **Animation** — Creating smooth circular movements from linear interpolation

---

## 🛠 Technical Details

### Built With
- **Vanilla JavaScript** — No frameworks or dependencies
- **HTML5 Canvas** — Hardware-accelerated 2D rendering
- **CSS3** — Modern styling with custom properties and animations
- **Web APIs** — MediaRecorder for video export

### Browser Support
- Chrome 60+
- Firefox 55+
- Safari 11+
- Edge 79+

### Performance
- 60 FPS animation loop
- Efficient trail rendering with history buffer
- Responsive canvas sizing

---

## 📄 License

MIT License — feel free to use, modify, and distribute.

---

## 🙏 Acknowledgments

- Inspired by the viral ["Crazy Circle Illusion" video](https://www.youtube.com/watch?v=pGOiU6kJOzQ)
- Mathematical foundations from [Slate's explanation of cycloid motion](https://slate.com/technology/2014/07/cycloid-motion-an-illusion-based-on-spirographics.html)
- Built with ❤️ by [Accelerate Solutions](https://github.com/accelerate-solutions)

---

<p align="center">
  <strong>⭐ Star this repo if you found it educational or beautiful! ⭐</strong>
</p>

<p align="center">
  <sub>Created by Accelerate Solutions © 2025</sub>
</p>
