# Autonomous navigation in Webots

## Overview

This project implements an autonomous navigation pipeline for a mobile robot in a Webots simulation.

### Project goal

For all 5 given maps, the robot must:

- Navigate between the **blue** and **yellow** columns (landmarks)
- Avoid the **green area** (hazard/obstacle region)
- Find and follow an optimal path from blue to yellow

### Key approaches

- **Environment Mapping**: Builds an occupancy grid map from **LiDAR** data
- **Perception**: Detects landmarks and hazards with **camera-based color segmentation**
- **Path Planning**: Plans routes using global **A\*** algorithm with local **DWA path following**

## Installation requirements

- Python 3.x
- Webots
- Python packages listed in [requirements.txt](requirements.txt)

Install the Python dependencies :

```bash
pip install -r requirements.txt
```

## Webots setup (selecting the controller)

1. Open your world in Webots.
2. In the robot node properties, set **controller** to `main`.
3. Ensure the controller directory points to [src/controllers/main](src/controllers/main) and the entry file is [src/controllers/main/main.py](src/controllers/main/main.py).
4. Start the simulation.
