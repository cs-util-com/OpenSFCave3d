# Open 3D SFCave

A modern, **3D twist on the classic sfcave** experience, viewed from a thrilling first-person perspective.  
Dive into a procedurally generated tunnel, dodge obstacles, and see how long you can survive!

### **Play Here:** [https://cs-util-com.github.io/OpenSFCave3d/](https://cs-util-com.github.io/OpenSFCave3d/)

---

## Overview

- **Concept:** Steer your aircraft through a tunnel that continuously **narrows** over time.  
- **Objective:** Survive as long as possible to rack up the highest score.

---

## Key Features

1. **Procedural Tunnel Generation**  
   - Each run is unique, shaped by a random **seed** that you can set or randomize.  
   - The tunnel **narrows** progressively, increasing the challenge.
2. **Obstacle & Power-Up Placement**  
   - **Bright, visible obstacles** threaten your path — avoid them at all costs.  
   - **Power-ups** like Slow-Mo, Score Boost, and Auto-Fire give you temporary advantages.
3. **Ghost Run System**  
   - The game **records your movements**, storing them locally.  
   - Replay the same seed to race against your own **ghost** and beat your previous record.
4. **Simple, Intuitive Controls**  
   - **Tap/Click** for upward impulse.  
   - **Tilt** or **mouse movement** to steer left and right.
5. **Scoring & Progress**  
   - Earn **distance-based** points; collect **bonuses** for power-ups and destroyed obstacles.  
   - High scores are stored locally by seed — challenge yourself or friends!

---

## How to Play

1. **Open `index.html` in Your Browser**  
   - No server needed; just an internet connection for Babylon.js & Cannon.js (CDN).
2. **Choose or Set a Seed**  
   - By default, a **random seed** is generated.  
   - Or append `?seed=1234` (for example) to the URL to replay or share a specific layout.
3. **Controls**  
   - **Desktop:**  
     - **Click** for an upward jump.  
     - **Move the mouse** left/right to steer horizontally.  
   - **Mobile:**  
     - **Tap** to jump.  
     - **Tilt** left/right to steer horizontally.
4. **Objective**  
   - Stay within the tunnel walls.  
   - Collect power-ups.  
   - Avoid obstacles at all costs.  
   - Colliding or leaving the tunnel ends the run.

---

## Ghost Runs

- Automatically **recorded** each time you play.  
- Saved in `localStorage` under a unique key tied to the **seed**.  
- Replay the **same seed** to watch a semi-transparent ghost representing your best performance.

---

## Modifying the Code

- **Game Settings:**  
  - Tweak constants (e.g., `FORWARD_SPEED`, `UP_IMPULSE`, `SLOW_MO_DURATION`) in the `<script>` section.  
- **Dependencies:**  
  - Babylon.js & Cannon.js are **CDN-based** in the HTML `<head>`.  
  - You can switch to local references if you prefer offline usage.
- **Seed Logic:**  
  - Uses a simple **linear congruential generator (LCG)** for deterministic placement of obstacles and power-ups.

---

## Local Data

- **Storage:**  
  - Ghost run data is kept in your **browser’s `localStorage`** under keys like `ghostPositions_<seed>`.  
- **Resetting:**  
  - Clear your browser’s local storage to remove old runs and high scores.

---

## Contributing

- **Issues & Feature Requests:**  
  - Report them on the project’s GitHub **Issue Tracker**.  
- **Pull Requests:**  
  - Fork this repo, commit improvements, and open a PR with details on what you changed.

---

Enjoy your flight through the ever-narrowing 3D cave, and don’t forget to **share your seed** so others can challenge your high score!