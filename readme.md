# COVID-19 3D Spatial Simulation with SEIR Dynamics

## Overview
This project implements a 3D spatial simulation of COVID-19 transmission using the **SEIR epidemiological model**, visualized through a multi-panel animated dashboard. The simulation models disease propagation in a 3D environment where agents move and interact, with different scenarios including lockdown effects.

## Features
- **3D Spatial Visualization**: Real-time 3D representation of agent movement and state changes
- **SEIR Model Implementation**: 
  - **S**: Susceptible
  - **E**: Exposed
  - **I**: Infectious
  - **R**: Recovered
- **Multi-scenario Support**: Baseline transmission vs. lockdown scenarios
- **Comprehensive Dashboard**:
  - 3D propagation view with rotating camera
  - SEIR evolution curves over time
  - Daily new infections with 7-day moving average
  - Real-time population distribution pie chart
  - Live statistics panel with effective R₀ calculation

## Key Components

### 1. Simulation Core
- **Agent-based modeling**: 120 agents in 100×100×100 3D space
- **Transmission mechanics**: Distance-based infection probability
- **Dynamic parameters**: 
  - Initial R₀: 3.50
  - 8 initial infections
  - 40-day simulation period
  - Adjustable transmission rates

### 2. Visualization System
- **Interactive 3D scatter plot**: Color-coded agent states with distinct markers
- **Multi-panel layout**: 6 synchronized visualization components
- **Real-time updates**: Frame-by-frame progression of the epidemic
- **Lockdown visualization**: Gray shaded regions indicating intervention periods

### 3. Animation Engine
- **Custom frame generation**: 400 frames for 40-day simulation
- **Dynamic data synchronization**: All visualization components update simultaneously
- **GIF export capability**: High-quality animation saving with configurable FPS
- **Performance optimization**: Frame limiting and efficient data handling

## Technical Implementation

### Libraries Used
- `numpy`: Numerical computations and array operations
- `matplotlib`: 2D and 3D visualization with animation support
- `scipy.spatial`: Distance calculations for infection spread
- `Pillow`: GIF image creation and saving

### Key Functions
- `create_complete_animation()`: Main animation controller
- **Subplots**:
  - 3D spatial propagation
  - SEIR evolution curves
  - Daily infection bar charts
  - Population distribution pie chart
  - Live statistics text panel

### Simulation Parameters
- Population: 120 agents
- Simulation days: 40
- Initial infected: 8
- Initial R₀: 3.50
- Frames per second: 10
- Lockdown scenario: Days 15-35

## Output
- **Interactive display**: Real-time animation during execution
- **GIF export**: `covid_confinement_complete.gif` (400 frames)
- **Statistics tracking**: 
  - Daily counts for S, E, I, R compartments
  - Percentage calculations
  - Effective reproduction number (R₀)

## Applications
- **Educational tool**: Visualizing disease spread dynamics
- **Policy analysis**: Comparing intervention strategies
- **Research visualization**: Communicating epidemiological concepts
- **Public health planning**: Understanding spatial transmission patterns

## Usage Notes
- The simulation automatically extends to ensure sufficient frames for animation
- Memory-efficient data handling for large agent populations
- Configurable parameters for different epidemic scenarios
- Robust error handling for animation saving and display

This implementation provides a comprehensive, visually engaging tool for understanding COVID-19 transmission dynamics in both spatial and temporal dimensions, with particular emphasis on how interventions like lockdowns affect disease progression.