Create a self-contained, 60-second motion design showreel titled "ULTRABLUE" as a single executable HTML file

The aesthetic is high-contrast Swiss typography meets procedural 3D generative art. It should look refined, intentional, and modern,

---

### 1. TECHNICAL STACK & SETUP

- **Viewport & Aspect Ratio**: Fixed 16:9 canvas (1920×1080 logical resolution), auto-centered with responsive black letterboxing on any screen size.
- **Master Timeline**:
  - Exactly 60.0 seconds total duration at 60 FPS.
  - Driven by a deterministic global clock variable `currentTime` (0.0 to 60.0s) and normalized `progress = currentTime / 60.0`.
  - All procedural animations, camera paths, shaders, and audio events MUST evaluate directly against `currentTime` so the entire reel is fully scrubbable and frame-accurate.

---

### 2. COLOR PALETTE & VISUAL DIRECTION

- **Void Black**: `#02040B` (negative space, background)
- **Deep Ultramarine**: `#182BCE`
- **Electric Blue**: `#4D6BFE` / `#2155FF` (primary accents, emission)
- **Ice Blue / Specular**: `#C6E5FF` & Pure White `#FFFFFF`
- **Typography & UI**: High-contrast Swiss style (clean geometric sans-serif / monospace technical metadata, tracking, tight grid alignment).

---

### 3. THREE-ACT CHOREOGRAPHY

#### ACT I — SIGNAL & KINETIC TYPOGRAPHY (00:00 – 00:18)

- **Visual**: Begins in near-total darkness. A central electric-blue point emits concentric geometric interference rings (polar coordinate wave shaders).

#### ACT II — TOPOLOGY & PROCEDURAL FIELD (00:18 – 00:42)

- **Visual**: The lines extrude into a 3D architectural ribbon / twisted torus structure using dynamic vertex displacement (Simplex/Curl noise simulation).
- \

#### ACT III — CRESCENDO, COLLAPSE & SIGNATURE (00:42 – 01:00)

- **Visual (00:42–00:52)**: The ribbon accelerates and violently collapses inward into a single, highly polished monolithic geometric crystal.

  The structure gently loops back to the initial single micro-point at 60.0s.

---

### 4. PROCEDURAL SOUND DESIGN (WEB AUDIO API)

Synthesize an original, minimalist electronic IDM soundtrack using native Web Audio API oscillators and noise buffers:

- **00s–18s**: Low-pass filtered sub-bass drone (45–55 Hz) with rhythmic microscopic transient clicks.
- **18s–42s**: Syncopated polyrhythmic 130 BPM glitch percussion, resonant sweeps, and subtle stereo panning.
- **42s–52s**: Tension riser with frequency-modulated pitch sweep leading to an explosive sub-drop at the flash.
- **52s–60s**: Instant release into a single warm ambient pad chord that softly fades out.
- *Audio must automatically handle browser autoplay policies via an initial click/user interaction.*

---

### 5. CINEMATICS & PLAYER CONTROLS

- **Minimalist HUD Overlay**:
  - Auto-hides after 2 seconds of mouse inactivity.
  - Top bar: Timecode display `[ 00:00:00 / 00:60:00 ]`, frame counter, and FPS.
  - Bottom bar: Minimal scrubbable timeline bar, Play/Pause toggle, and Fullscreen button.
- **Keyboard shortcuts**: `Space` (Play/Pause), `R` (Restart to 0s), `Left/Right Arrows` (Step ±1 second when paused).

---

### DELIVERABLE REQUIREMENTS

Output the entire, ready-to-run HTML code directly without placeholders or missing implementations. Ensure 60 FPS performance on standard hardware through instanced geometry and optimized shader loops.
