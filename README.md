
# Evolutionary Agent Simulation — Research Lab X

A high-density browser-based evolutionary ecosystem simulation combining swarm behaviour, reinforcement-learning-style commander control, environmental pressure, emergent cooperation, resource competition, pathogen dynamics, and research-inspired quality-diversity tracking.

This project runs as a single HTML file using **Canvas**, **TensorFlow.js**, and **Chart.js**. It simulates thousands of autonomous agents living inside a changing world with weather, wind, day/night cycles, seasons, food, water, minerals, threats, obstacles, sanctuaries, pheromones, communication pulses, and adaptive tasks.

---

## Overview

**Evolutionary Agent Simulation — Research Lab X** is an experimental artificial-life sandbox where agent tribes evolve, cooperate, compete, survive, reproduce, and respond to a machine-learning-driven commander.

The simulation keeps the original large-scale ecosystem design while adding new research-inspired systems such as:

- Spatial hash acceleration
- Prioritized replay memory
- Double-DQN-style commander learning
- Curiosity and novelty reward
- MAP-Elites-inspired quality-diversity archive
- Population-based hyperparameter nudging
- Pheromone fields
- Communication pulses
- Pathogen clouds
- Sanctuaries
- Seasonal pressure
- Telemetry export
- Local save/load snapshots

The goal is not only to make agents survive, but to create a living research playground where cooperation, adaptation, diversity, and environmental strategy can emerge over time.

---

## Features

### Large-Scale Agent Ecosystem

The simulation preserves the original entity scale:

| Entity | Starting Count |
|---|---:|
| Agents | 1,620 |
| Threats | 135 |
| Food | 225 |
| Water | 135 |
| Tasks | 45 |
| Threat Nests | 90 |
| Obstacles | 135 |
| Minerals | 135 |

Agents belong to tribes and maintain individual state values such as:

- Energy
- Hydration
- Synergy
- Tribe ID
- Lineage
- Age
- Infection status
- Genome traits
- Cooperation tendency
- Curiosity tendency
- Speed and sensing traits

---

## Research Lab X Upgrades

### Spatial Hash Performance System

The original neighbour checks are upgraded with a spatial hash grid. This makes large swarm queries much faster by checking nearby cells instead of comparing every agent against every other agent.

Used for:

- Local neighbour detection
- Agent tooltips
- Agent selection
- Cooperation sharing
- Threat/resource seeking
- Pheromone and local-environment queries

---

### Commander Agent

The simulation includes a TensorFlow.js-powered commander model that observes global ecosystem state and selects high-level interventions.

Commander actions include:

- Spawn synergy tasks
- Lower task synergy requirements
- Increase threat pressure
- Refresh agent target behaviour
- Spawn tribe mega-tasks
- Buff tribe synergy
- Trigger resource blooms
- Spawn sanctuaries

The commander uses:

- Neural network prediction
- Target model updates
- Replay memory
- Exploration/exploitation through epsilon decay
- Learning-rate control
- Mutation-rate control
- Loss tracking with Chart.js

---

### Prioritized Replay

The commander does not treat every experience equally. More important or surprising experiences can be replayed more often, helping the model focus on transitions that matter.

This helps the commander learn from:

- Large reward swings
- Dangerous ecological events
- Resource collapses
- Tribe success patterns
- Novel world states

---

### Double-DQN-Style Targeting

The commander separates current Q-value estimation from target Q-value estimation. This reduces overconfident action values and makes learning more stable.

---

### Curiosity and Novelty

The simulation tracks how often areas of the world have been visited. Agents and the commander can receive novelty pressure when exploring less-used regions of the map.

This creates more interesting behaviour than simple food-seeking alone.

Novelty affects:

- Exploration
- Commander reward
- Research metrics
- Heatmap visualisation

---

### MAP-Elites-Inspired Archive

A quality-diversity archive records high-performing behavioural niches instead of only tracking one best score.

The archive rewards diversity across different behavioural patterns, allowing tribes to succeed in different ways.

The archive appears in the **Research Lab X** panel as a small grid of behavioural cells.

---

### Population-Based Hyperparameter Nudging

The simulation can gradually nudge learning parameters based on performance.

Tracked parameters include:

- Learning rate
- Mutation rate
- Epsilon decay
- Commander reward
- Novelty
- Population survival

This creates a more adaptive training system instead of relying on one fixed configuration forever.

---

## Environment Systems

### Weather

Weather changes dynamically over time.

Supported conditions:

- Sunny
- Rainy
- Stormy
- Foggy

Weather affects movement and ecosystem pressure.

---

### Wind

Wind has both speed and direction. It influences:

- Threat drift
- Agent movement
- Weather feel
- Environmental variation

---

### Day/Night Cycle

The world has a continuous time-of-day system.

The canvas background shifts between daytime and nighttime colours, and a dynamic sun moves through the sky.

---

### Seasons

The simulation includes seasonal modifiers:

| Season | Effect |
|---|---|
| Spring | More resources, lower disease pressure |
| Summer | Stable resources, higher disease pressure |
| Autumn | Reduced resources, moderate disease pressure |
| Winter | Scarcer resources, stronger threat pressure |

---

### Terrain Zones

The world is divided into terrain zones:

- Forest
- Desert
- Urban
- Mountain
- Plains

Each terrain type has different resource and movement characteristics.

---

## Agent Behaviour

Agents use local steering rules combined with evolving traits.

They can:

- Seek food when energy is low
- Seek water when hydration is low
- Seek minerals for synergy
- Avoid threats
- Avoid obstacles
- Follow nearby allies
- Separate from overcrowded allies
- Deposit pheromones
- Follow pheromone gradients
- Respond to signal pulses
- Reproduce when healthy and energetic
- Mutate genome traits
- Become infected by pathogen clouds
- Recover in sanctuary zones

---

## Resources

### Food

Restores energy.

### Water

Restores hydration.

### Minerals

Increase synergy and support group task completion.

### Sanctuaries

Temporary safe zones that help agents recover from disease and survive difficult conditions.

---

## Threat Systems

### Threats

Hostile entities that move through the ecosystem and pressure agents.

### Threat Nests

Spawn additional threats when global synergy rises high enough, creating a balancing force against over-successful populations.

### Pathogen Clouds

Disease zones that infect agents and create health pressure across the population.

---

## Synergy and Cooperation

Agents gain synergy by staying near members of their own tribe.

Synergy is used to complete:

- Standard synergy tasks
- Tribe-specific mega-tasks
- Global cooperative objectives

Nearby agents can also share cooperation values, creating smoother group-level behaviour.

---

## Visual Layers

The simulation includes optional visual overlays:

| Layer | Description |
|---|---|
| Pheromones | Shows pheromone trails left by agents |
| Heatmap | Shows explored and frequently visited regions |
| Labels | Shows lineage/identity labels above selected agents |

---

## Controls

| Control | Description |
|---|---|
| Train Commander | Runs extra commander training steps |
| Reset | Restarts the simulation |
| Pause / Resume | Freezes or resumes the ecosystem |
| Save | Saves a snapshot to `localStorage` |
| Load | Restores the saved snapshot |
| CSV | Exports telemetry data as a CSV file |
| Pheromones | Toggles pheromone visualisation |
| Heatmap | Toggles exploration heatmap |
| Labels | Toggles lineage labels |
| Disrupt | Adds a disruptive ecological event |
| Sim Speed | Adjusts simulation speed |
| LR | Adjusts commander learning rate |
| Mutation | Adjusts mutation rate |
| Epsilon Decay | Adjusts exploration decay |
| Curiosity | Adjusts novelty reward weight |
| Curriculum | Adjusts adaptive pressure |

---

## Telemetry

The simulation tracks live metrics including:

- FPS
- Generation
- Time of day
- Weather
- Season
- Wind
- Agent count
- Threat count
- Resource count
- Mean energy
- Mean hydration
- Mean synergy
- Diversity
- Novelty
- Commander reward
- Commander epsilon
- Learning rate
- Mutation rate
- Tasks completed
- Mega-tasks completed
- Births
- Deaths
- Infections
- Resources consumed

Telemetry can be exported as CSV for later analysis.

---

## Save and Load

The simulation supports browser-local snapshots through `localStorage`.

Saved data includes:

- Generation
- Time of day
- Weather
- Wind
- Agent states
- Genome traits
- Threats
- Resources
- Tasks
- Pathogen clouds
- Sanctuaries
- Recent telemetry

This makes it possible to pause long-running experiments and resume them later.

---

## Installation

No build step is required.

Clone or download the project, then open the HTML file through a local server.

```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
````

Start a simple local server:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000/
```

---

## Why Use a Local Server?

The project loads external browser libraries from CDNs:

* TensorFlow.js
* Chart.js

Running through a local server avoids browser restrictions that can happen when opening files directly with `file://`.

---

## Dependencies

Loaded through CDN:

```html
<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
<script src="https://cdn.jsdelivr.net/npm/@tensorflow/tfjs@latest"></script>
```

No package manager is required.

---

## Suggested File Structure

```text
project-root/
├── index.html
├── README.md
└── screenshots/
    └── preview.png
```

---

## How It Works

The simulation runs inside a requestAnimationFrame loop.

Each frame:

1. Updates time, weather, season, and wind.
2. Rebuilds spatial hashes for fast lookup.
3. Lets the commander observe the global state.
4. Applies commander actions.
5. Updates agents, threats, resources, pathogens, sanctuaries, and tasks.
6. Calculates synergy and cooperation.
7. Handles resource consumption and reproduction.
8. Updates telemetry and archive metrics.
9. Draws the ecosystem and UI overlays.
10. Updates the training loss chart.

---

## Main Systems

### `Agent`

Base autonomous entity with energy, hydration, synergy, tribe, genome, infection state, and local movement behaviour.

### `AdvancedAgent`

Extended agent type used for the full simulation.

### `CommanderAgent`

Machine-learning controller that observes the ecosystem and performs strategic interventions.

### `SpatialHash`

Acceleration structure for nearby-object lookup.

### `Task`

Cooperation objective that requires global or tribe-specific synergy.

### `Threat`

Hostile entity that pressures agent survival.

### `ThreatNest`

Spawner that creates new threats under certain ecosystem conditions.

### `PathogenCloud`

Disease hazard that can infect agents.

### `Sanctuary`

Temporary recovery zone.

### `SignalPulse`

Short-lived communication pulse used to visualise agent/tribe signalling.

---

## Experiment Ideas

Try running different experiments:

* Increase mutation rate and observe whether tribes diverge faster.
* Increase curiosity and watch agents explore more of the map.
* Lower synergy requirements and see whether task completion accelerates.
* Increase threat aggressiveness and test whether cooperation becomes more important.
* Toggle the heatmap to study exploration patterns.
* Export CSV after a long run and chart survival, novelty, and reward over time.
* Save a stable ecosystem, then trigger disruption and compare recovery.

---

## Performance Notes

This simulation is intentionally large and visually active.

For best performance:

* Use a modern Chromium-based browser.
* Close other heavy browser tabs.
* Reduce simulation speed if FPS drops.
* Turn off heatmap or pheromone overlays if needed.
* Avoid setting extremely high population limits on low-power devices.

The spatial hash system helps significantly, but thousands of agents plus TensorFlow.js training can still be demanding.

---

## Browser Compatibility

Recommended:

* Chrome
* Edge
* Brave
* Other modern Chromium-based browsers

Firefox may work, but TensorFlow.js performance and canvas behaviour can vary by system.

---

## Limitations

This is an experimental artificial-life simulation, not a scientifically validated ecology model.

The commander is a browser-based learning system designed for exploration and visual experimentation. Results should be treated as emergent simulation behaviour rather than formal biological or reinforcement-learning proof.

---

## Roadmap

Possible future improvements:

* Web Worker simulation thread
* OffscreenCanvas rendering
* WebGPU TensorFlow.js backend support
* Replay inspector
* Agent family tree viewer
* Tribe diplomacy system
* Predator/prey specialization
* More terrain-specific behaviours
* Import/export full experiment presets
* Multi-run experiment comparison dashboard
* Graph-based social network visualisation
* Evolutionary species clustering
* More advanced neural policies for individual agents

---

## Contributing

Contributions are welcome.

Good areas to improve:

* Simulation performance
* Agent intelligence
* Visual overlays
* Experiment tools
* Data export
* UI layout
* Documentation
* Accessibility
* Mobile support

---

## License

Choose the license that best fits your project.

Recommended open-source options:

* MIT License
* Apache 2.0
* GPLv3

Example:

```text
MIT License
Copyright (c) 2026 Your Name
```

---

## Credits

Built with:

* HTML5 Canvas
* JavaScript
* TensorFlow.js
* Chart.js

Inspired by concepts from:

* Artificial life
* Swarm intelligence
* Evolutionary computation
* Reinforcement learning
* Quality-diversity search
* Curiosity-driven exploration
* Population-based training
* Multi-agent systems

---

## Summary

**Evolutionary Agent Simulation — Research Lab X** is a browser-native artificial-life laboratory for exploring how simple local behaviours, environmental pressure, machine-learning guidance, and evolutionary variation can produce complex ecosystem dynamics.

It is designed to be visual, interactive, experimental, and expandable.

```
```
