# Game Architecture

## 1. Core Engine
- **State Management**: A reactive state object (`gameState`) holding current location, evidence list, suspect status, logs, and progression flags.
- **Action Interpreter**: A central function `handleAction(input)` that maps natural language tokens to game functions.
- **Scene Controller**: Manages transitions between screens (Investigation, Crime Scene, Suspects, etc.).

## 2. Component Structure
- `App`: Main controller.
- `Dashboard`: HUD/Navigation/Case Info.
- `InvestigationArea`: Interaction input & log.
- `CrimeSceneViewer`: Interactive overlay component.
- `ModalSystem`: For evidence examination and suspect interrogation.

## 3. Data Structure
- `suspects`: Array of objects (profiles, motives, secrets).
- `evidence`: Array of objects (discovered flag, detailed descriptions).
- `locations`: Object mapping names to interactive scenes.
