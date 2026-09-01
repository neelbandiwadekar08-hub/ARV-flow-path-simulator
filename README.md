# ARV Flow Path Simulator

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/neel-nagesh-bandiwadekar/)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/neelbandiwadekar08-hub)
![Made with Google AI Studio](https://img.shields.io/badge/Made%20with-Google%20AI%20Studio-4285F4?style=for-the-badge&logo=google&logoColor=white)

An interactive simulator that visualizes how an Automatic Recirculation Valve (ARV) protects a centrifugal pump. It shows, in real time, how the valve's internal cone shifts position to switch flow between a minimum-flow bypass line and the main delivery line.

## Live Demo

🔗 [Try the simulator here](https://pump-valve-video-animator.ai.studio/)

## Why I Built This

Automatic Recirculation Valves are a core piece of centrifugal pump protection in mechanical and process engineering: they prevent overheating, cavitation, vibration, and pump damage by making sure a minimum safe flow always passes through the pump, even when downstream demand drops. Static diagrams make this hard to grasp at a glance, so I designed an interactive visualizer that shows the valve's two operating states, and what physically happens in each one, so the mechanism is easy to understand at a glance.

## How the Valve Works

**Minimum Flow Line (bypass)**
When the minimum flow line is open, the cone sits at its resting position. Water flows through the bypass line, and the main flow line stays closed.

**Main Delivery Line**
When the main delivery line is open, the cone lifts up. This closes the bypass line and opens the main flow path.

The minimum flow line returns water to the storage tank, while the main flow line supplies the intended application. In this simulator, both lines discharge back into the storage tank to demonstrate a closed-loop circulation system.

## Simulator Legend

| # | Component |
|---|---|
| 1 | Tank |
| 2 | Pump |
| 3 | Automatic Recirculating Valve |
| 4 | Minimum flow line |
| 5 | Main Delivery line |

## Flow Indicator System

The simulator uses color-coded LEDs to trace liquid movement through the system in real time:

| Indicator | Meaning |
|---|---|
| 🔴 Red LEDs | Bypass loop active. Water returns to tank. |
| 🟢 Green LEDs | Main line active. High-volume supply enabled. |
| 🔵 Blue pulse | Momentary indicator during actuator transition. |

It also displays live system telemetry, including operational status and exact cone position (e.g. 100% fully lifted), alongside manual ON/OFF toggles to switch between the minimum-flow and main-delivery feed lines.

## Design Choices, and Why

| Element | Choice | Reasoning |
|---|---|---|
| Dual-line visualization | Separate red (bypass) and green (main) flow paths | Makes the two operating states visually distinct at a glance |
| Cone position readout | Live percentage (e.g. 100% fully lifted) | Ties the abstract valve state to a concrete, measurable value |
| LED color coding | Red / Green / Blue pulse system | Mirrors how real industrial control panels signal system state |
| Closed-loop demo setup | Both lines return to the same tank | Keeps the simulation self-contained and easy to demonstrate without external plumbing context |

## How It Was Made

1. Broke down the ARV's real mechanical operation into its two core states (minimum flow vs. main delivery) based on engineering fundamentals.
2. Defined the visual language needed to represent each state clearly: cone position, flow color coding, telemetry readout.
3. Directed Google AI Studio to build the interactive simulator around this structure and logic.
4. Tested both operating states to confirm the visualization matched real ARV behavior.

## Tools Used

- Google AI Studio — used to build the interactive simulator from the described mechanism and visual logic

## Repository Contents

- `README.md` — this file
- *(add here once uploaded: screenshots, source files, or additional documentation)*

## Connect

- LinkedIn: [Neel Nagesh Bandiwadekar](https://www.linkedin.com/in/neel-nagesh-bandiwadekar/)
- GitHub: [neelbandiwadekar08-hub](https://github.com/neelbandiwadekar08-hub)
