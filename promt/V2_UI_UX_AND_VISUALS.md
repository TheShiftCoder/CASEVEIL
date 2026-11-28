# V2 — UI/UX Design & Visuals

## Purpose
Design the interface, layout, and interaction states for **OBSCURA**. This version establishes the visual language and user experience before implementing the full engine.

---

## 1. Global Visual System
- **Theme**: Dark, cinematic, mature.
- **Palette**:
    - Background: `#0B0E13`
    - Panels: `#141B25` (Elevated: `#1A2230`)
    - Border: `#293344`
    - Primary Text: `#E8EDF5`
    - Muted: `#586477`
    - Accent: `#C69A5D`
    - Investigation Blue: `#7289A6`
- **Typography**: Inter (UI), Cormorant Garamond (Titles).
- **Feel**: Minimalist, thin lines, subtle shadows. No "gaming" neon or cluttered dashboards.

---

## 2. Main Layout (Responsive)
- **Desktop**: Three-pane layout.
    - **Sidebar** (Left): Navigation (Investigation, Scene, Suspects, Evidence, Timeline, Board, Notebook, Files).
    - **Main Area** (Center): Dynamic component based on route.
    - **Info Panel** (Right): Contextual information (active object/suspect). Collapsible.
- **Mobile**: Panels become drawers. Navigation is an off-canvas drawer or hamburger menu.
- **Feedback**: Every click has a micro-transition. Active selection is highlighted with a border/glow in `--accent`.

---

## 3. Screen-by-Screen Map
### 1. Landing
- Cinematic backdrop. Title "OBSCURA".
- Buttons: Start (Accent), Continue (Secondary), Case Files, Settings.
### 2. Case Selection
- Case 001 card (Playable). Placeholder cards for future cases.
### 3. Case Briefing
- Serene, text-heavy, document style. Briefing summary.
### 4. Investigation Workspace
- Header with case name/save status.
- Central Workspace (Log + Actions).
### 5. Crime Scene
- Visual scene view. Hotspot markers (pulsing dots).
- Inspection overlay (modal).
### 6. Suspects
- Profile grid. Clicking opens detailed view with interrogation.
### 7. Evidence Archive
- Grid/List view with filtering (Category/Source/Relevance).
### 8. Timeline
- Interactive vertical/horizontal track.
### 9. Detective Board
- Infinite canvas. Draggable cards with connection lines.
### 10. Settings
- Toggle switches (not checkboxes).

---

## 4. Interaction States
- **Button**: Hover = lighter background, Click = brief glow.
- **Hotspot**: Pulse animation.
- **Evidence Card**: Hover = slight elevation, Click = modal view.
- **Drag-and-Drop**: Visual ghosting during drag.
- **Inputs**: Transparent borders, focus = accent outline.

---

## 5. UI/UX Checklist
- [ ] Implement Main Navigation Component (Sidebar)
- [ ] Implement Header/Sidebar/RightPanel Layout
- [ ] Implement Crime Scene hotspot visual system
- [ ] Implement Modal component for inspections
- [ ] Implement draggable Detective Board components
- [ ] Implement responsive behavior for all panels
- [ ] Finalize cinematic landing screen design
- [ ] Verify hover/active/disabled states for all buttons
- [ ] Finalize typography hierarchy
