# Half Marathon Pace Simulator

[![Live Demo](https://img.shields.io/badge/Live-Demo-06b6d4?style=for-the-badge&logo=google-chrome&logoColor=white)](https://dreamerskymaster.github.io/half-marathon-pace-simulator/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)
[![Architecture: Zero--Build](https://img.shields.io/badge/Architecture-Zero--Build-10b981?style=for-the-badge)](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/What_is_JavaScript)

An interactive, responsive single-file training visualizer that models the mathematical and physiological feasibility of half marathon pacing goals. Built with **Vanilla JavaScript**, **Tailwind CSS (via CDN)**, and **Chart.js (via CDN)** with zero build tooling or Node.js runtime required.

---

## 🏃 Scenario Context

- **Runner Profile**: Fictional amateur runner training for a half marathon (13.1094 miles).
- **Current Long-Run Baseline**: `11:15 /mile` (675 seconds/mile).
- **Target Goal**: `2:10:00` finish time (~`09:55 /mile` / 595.4 seconds/mile).
- **Training Schedule**: 14 weeks, running 3 days per week.
- **Objective**: Visualize whether the weekly required pace improvement is achievable without exceeding safe physiological thresholds for musculoskeletal adaptation.

---

## 📊 Feasibility & Physiological Logic

The dashboard computes progression dynamics in real-time as input parameters change:

1. **Target Pace Calculation**:
   $$\text{Target Pace (sec/mi)} = \frac{\text{Target Time (minutes)} \times 60}{13.1094\text{ miles}}$$

2. **Weekly Improvement Rate**:
   $$\text{Weekly Drop (sec/wk)} = \frac{\text{Base Pace (sec)} - \text{Target Pace (sec)}}{\text{Weeks Until Race}}$$

3. **Injury Risk Assessment**:
   - **$\le 5.0\text{ sec/wk}$ (Safe Progression)**: Aerobic threshold adaptation comfortably sustained across 3 runs/week without overloading tendons.
   - **$5.1\text{ to }8.0\text{ sec/wk}$ (Aggressive - Monitor for Injury)**: Stretches neuromuscular adaptation limits; requires disciplined sleep, recovery, and volume spacing.
   - **$> 8.0\text{ sec/wk}$ (High Injury Risk - Extend Timeline)**: Exceeds mitochondrial and collagen remodeling capacity; timeline extension recommended.

---

## 🛠️ Key Features

- **Interactive Controls (Sliders)**:
  - **Weeks Until Race**: 5 to 20 weeks (Default: 14).
  - **Target Finish Time**: 110 to 160 minutes (Default: 130 min / 2:10:00).
  - **Current Base Pace**: 540s to 750s (Default: 675s / 11:15 min/mi).
- **Dynamic KPI Summary Cards**: Real-time updates for Target Race Pace, Baseline Pace, Total Delta Required, Weekly Pace Drop Rate, and Color-Coded Risk Assessment badge.
- **Interactive Chart.js Visualization**:
  - Linear progression trajectory from starting pace down to goal pace.
  - Custom Y-axis tick formatter translating seconds back into human-readable `MM:SS /mi`.
  - Detailed hover tooltips showing both pace and exact seconds.
- **Preset Quick-Selects**: One-click switching between Default (14 Wks / 2:10), Conservative Build (18 Wks / 2:15), and Aggressive Push (8 Wks / 2:00).
- **Zero-Build & Lightweight**: Pure HTML, CSS, and JS. Open directly in any modern browser without installing dependencies or running a server.

---

## 🚀 Getting Started

### Option 1: Live Demo
Open the live dashboard directly: [https://dreamerskymaster.github.io/half-marathon-pace-simulator/](https://dreamerskymaster.github.io/half-marathon-pace-simulator/)

### Option 2: Local Usage
Clone the repository and open `index.html` in your browser:
```bash
git clone https://github.com/dreamerskymaster/half-marathon-pace-simulator.git
cd half-marathon-pace-simulator
open index.html
```

---

## 📝 Submission & Portfolio Note

> *Note: The data and scenario modeled in this interactive visualization have been modified and fictionalized for public sharing purposes, as recommended by the project guidelines.*

---

## 📄 License
This project is licensed under the [MIT License](LICENSE).
