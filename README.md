# Open 3D SFCave

A 3D twist on the classic sfcave game, played from a first-person perspective inside a procedurally generated tunnel.

### Play at >> https://cs-util-com.github.io/OpenSFCave3d/ <<

## Overview

- **Concept:** Maneuver a dot (representing a plane) through a narrowing 3D tunnel while avoiding obstacles.  
- **Perspective:** First-person view (camera parented to the dot).  
- **Objective:** Survive as long as possible to achieve a high score.

## Key Features

1. **Procedural Tunnel Generation:**  
   - A random or user-specified seed determines the tunnel layout.  
   - Tunnel gradually narrows to increase difficulty over time.
2. **Obstacle & Power-Up Placement:**  
   - Obstacles are positioned along the tunnel and must be avoided.  
   - Collectible power-ups offer temporary benefits like slow-motion, score boosts, or auto-firing capabilities.
3. **Ghost Run System:**  
   - The game records your run (position/timing).  
   - When replaying the same seed, see a "ghost" of your previous best run.
4. **One-Tap Vertical Control & Sensor-Based Steering:**  
   - Tap/Click provides an upward impulse.  
   - Tilt or mouse movement controls horizontal movement.
5. **Scoring & Progress Tracking:**  
   - Base score from distance traveled.  
   - Bonus points from destroying obstacles and collecting power-ups.  
   - High scores are recorded locally for each seed.

## How to Play

1. **Open `index.html` in a Browser:**  
   - No additional server setup is needed.  
   - Requires an internet connection for Babylon.js and Cannon.js CDN dependencies (unless downloaded and referenced locally).
2. **Seed Selection:**  
   - On first load or refresh without a seed, a random one is chosen.  
   - You can specify your own seed by editing the URL parameter, e.g. `?seed=1234`.
3. **Controls:**
   - **Desktop:**  
     - Click to jump (upward impulse).  
     - Move mouse left/right to steer horizontally.  
   - **Mobile:**  
     - Tap to jump.  
     - Tilt your device left/right for horizontal control.
4. **Goal:**  
   - Avoid obstacles.  
   - Stay within the tunnel walls.  
   - Collect power-ups to maximize your score.  
   - Your run ends when you collide with an obstacle or leave the tunnel.

## Ghost Runs

- Your position is recorded on every frame.  
- After a run finishes (game over), the run data (including final score) is saved in `localStorage`.  
- If you replay the same seed, a semi-transparent "ghost" appears, replicating your best run’s path.

## Modifying the Code

- **Babylon.js & Cannon.js Dependencies:**  
  - Loaded via CDN in the `<head>` of the HTML file.  
- **Game Settings:**  
  - Tunable constants such as `FORWARD_SPEED`, `UP_IMPULSE`, `SLOW_MO_DURATION`, etc., can be modified in the `<script>` section of `index.html`.
- **Seed Logic:**  
  - Implemented with a simple linear congruential generator (LCG) for reproducible random values.

## Local Data

- **Where Runs Are Stored:**  
  - The player’s ghost data is saved using `localStorage`.  
  - This data is keyed by `ghostPositions_<seed>` for each unique seed.
- **Clearing Data:**  
  - You can clear your browser’s local storage to remove ghost data and high scores for fresh starts.

## Contributing

- **Issues & Feature Requests:**  
  - Use GitHub’s Issue Tracker to submit bug reports or suggestions.
- **Pull Requests:**  
  - Fork the repository, make changes, and open a PR explaining your enhancements.
