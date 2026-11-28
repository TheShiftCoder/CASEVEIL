# OBSCURA — MASTER BUILD PROMPT
## Complete Game Design, UI, Architecture, Logic & V1 Implementation

Build a complete, playable web-based detective investigation game called **OBSCURA**.

Tagline: **Nothing is what it seems.**

This is not a chatbot interface, not a static dashboard, and not just a text-based story. It should feel like a real detective investigation game where players actively investigate crime scenes, examine objects, interview suspects, discover clues, connect evidence, reconstruct events, develop theories and ultimately solve the case.

Build the complete V1 prototype now. Do not just provide plans, explanations, mockups, or code snippets. Create the actual project files and implement the game.

---

# 1. PRODUCT VISION

OBSCURA is an investigation game in which the player acts as an independent detective.

Each case is a contained mystery with:

- A crime.
- A crime scene.
- Multiple suspects.
- Individual suspect personalities.
- Motives.
- Secrets.
- Alibis.
- Evidence.
- Contradictions.
- Red herrings.
- A hidden truth.
- A chronological timeline.
- Multiple investigation paths.
- A final accusation and evaluation.

The game should feel like a combination of:

- Detective investigation.
- Interactive mystery.
- Psychological interrogation.
- Evidence analysis.
- Crime reconstruction.
- Narrative puzzle.
- Detective reasoning.

The player must not be guided through a rigid linear sequence. Multiple investigation approaches should be possible.

The player should not immediately know the culprit.

The game should reward logical investigation instead of simply clicking everything.

---

# 2. V1 SCOPE

This is V1.

Everything should work locally and use hardcoded game data.

Do NOT use:

- AI APIs.
- OpenAI API.
- Gemini API.
- Backend servers.
- Authentication.
- Firebase.
- Supabase.
- Database connections.
- Paid APIs.
- External AI services.

Use localStorage for saving game progress.

However, structure the project so that simulated game systems can later be replaced with real AI services without rebuilding the entire UI.

The game must be playable from beginning to end.

Do not create fake buttons.

Every visible interactive element must have a meaningful function.

---

# 3. TECHNOLOGY STACK

Use:

- React.
- Vite.
- JavaScript.
- CSS.
- React Router if routing is required.
- Lucide React for icons.
- LocalStorage for persistence.
- Native HTML drag and drop or a lightweight drag-and-drop library if necessary.

Do not use a giant single React component.

Use modular architecture.

Do not use TypeScript unless absolutely necessary.

Do not introduce unnecessary dependencies.

---

# 4. BRAND IDENTITY

Game name: OBSCURA

Tagline: Nothing is what it seems.

Brand personality:

- Dark.
- Psychological.
- Cinematic.
- Intelligent.
- Mature.
- Minimalist.
- Suspenseful.
- Investigative.
- Premium.

Avoid:

- Cartoon detective visuals.
- Generic dashboard UI.
- Bright colors.
- Excessive gradients.
- Gaming neon.
- Excessive rounded cards.
- Emoji-based interfaces.
- AI chatbot visual styles.
- Overly cluttered layouts.

---

# 5. DESIGN SYSTEM

Create a consistent design system.

## Colors

Background:
#0B0E13

Secondary background:
#10151D

Panel:
#141B25

Elevated panel:
#1A2230

Border:
#293344

Primary text:
#E8EDF5

Secondary text:
#8995A7

Muted text:
#586477

Accent:
#C69A5D

Accent hover:
#D9AD70

Danger:
#B85B5B

Success:
#799C84

Investigation blue:
#7289A6

## Typography

Use:

- Inter for UI.
- A restrained serif font for cinematic titles and case introductions, such as Cormorant Garamond or Playfair Display.

Maintain strong typographic hierarchy.

## UI characteristics

- Thin borders.
- Subtle shadows.
- Controlled spacing.
- Low contrast panel separation.
- Minimal motion.
- Cinematic transitions.
- Professional icons.
- Consistent spacing.
- Responsive layout.

## Layout

Design for desktop first.

Support:

- Desktop.
- Laptop.
- Tablet.
- Mobile.

The desktop version should feel like an immersive detective workspace.

The mobile version should reorganize navigation, evidence board and scene interactions without breaking functionality.

---

# 6. GAME STRUCTURE

Create the following main screens:

1. Landing screen.
2. Case selection screen.
3. Case briefing screen.
4. Investigation workspace.
5. Crime scene.
6. Suspect directory.
7. Suspect interrogation.
8. Evidence archive.
9. Timeline.
10. Detective board.
11. Case notebook.
12. Final accusation.
13. Case results.
14. Settings.
15. Resume investigation.

All screens must be interconnected.

---

# 7. LANDING SCREEN

Create a cinematic introduction.

Include:

OBSCURA

Nothing is what it seems.

A subtle dark cinematic background with:

- A dimly lit investigation room.
- Faint paper textures.
- A restrained vignette.
- A subtle grain effect.
- Minimal motion.

Buttons:

- Start Investigation.
- Continue Case (only when saved progress exists).
- Case Files.
- Settings.

Include an understated footer:

OBSCURA / INTERACTIVE INVESTIGATION

Avoid making the screen look like a generic gaming landing page.

---

# 8. CASE SELECTION

Create a case selection interface.

Initially, only one case is playable.

Display:

CASE 001

THE LAST NIGHT AT BLACKWOOD

Status: Available.

Display case metadata:

- Case type: Homicide.
- Difficulty: Intermediate.
- Location: Blackwood Estate.
- Suspects: 5.
- Evidence: Unknown to the player.
- Status: Unsolved.

Create additional future cases as locked placeholders.

Locked cases must not pretend to be playable.

They may display:

- Case 002 — The Silent Witness.
- Case 003 — Room 17.
- Case 004 — The Missing Hour.

These are visual placeholders only.

---

# 9. CASE BRIEFING

Create an immersive briefing screen.

Case title:

THE LAST NIGHT AT BLACKWOOD

Brief:

At 10:47 PM, Adrian Blackwood, a wealthy art collector, was found dead in his private study at Blackwood Estate.

The estate was occupied by five people that evening.

A storm had disrupted communications and partially affected the property's security systems.

The death is believed to have occurred sometime between 9:30 PM and 10:20 PM.

The circumstances surrounding the death are suspicious.

The player has been assigned to investigate.

The briefing must not reveal the killer.

Include:

- Case summary.
- Victim profile.
- Location.
- Estimated crime window.
- Known initial facts.
- Start Investigation button.

The player should enter the investigation workspace after clicking Start.

---

# 10. INVESTIGATION WORKSPACE

This is the core game interface.

Create a persistent investigation layout.

## Left sidebar

Navigation:

- Investigation.
- Crime Scene.
- Suspects.
- Evidence.
- Timeline.
- Detective Board.
- Notebook.
- Case Files.

Display:

- Case name.
- Current investigation progress.
- Investigation status.
- Save indicator.

## Main area

The main area changes based on the selected investigation section.

## Right side panel

A collapsible panel containing:

- Recent discoveries.
- Investigation activity.
- Contextual information.
- Current selected object or suspect.

On mobile, convert panels into drawers.

---

# 11. INVESTIGATION HUB

Create the primary investigation screen.

Display:

- Case overview.
- Investigation summary.
- Latest discoveries.
- Suspect overview.
- Investigation activity.
- Current investigation progress.
- Recommended investigation actions.

Do not reveal recommendations that expose the solution.

Suggestions must be contextual and based on the current investigation state.

Examples:

- Examine the study more carefully.
- Review the victim's last known movements.
- Question Eleanor about the evening.
- Compare the broken glass with the recovered evidence.
- Reconstruct the timeline.

These recommendations must change based on discovered clues and completed actions.

---

# 12. CRIME SCENE

Create an immersive crime scene interface.

Location:

Adrian Blackwood's study.

The scene should include a visually compelling illustration, generated image, available assets or custom CSS illustration.

Do not rely on a plain text-only scene.

Create an actual visual scene with clickable investigation hotspots.

Hotspots:

1. Desk.
2. Victim's body.
3. Window.
4. Wall clock.
5. Broken glass.
6. Bookshelf.
7. Study door.
8. Rug.
9. Fireplace.
10. Cabinet.

Each hotspot should have:

- Visual indication.
- Hover state.
- Click interaction.
- Contextual examination.
- Investigation result.
- Possible evidence discovery.
- Repeat examination behavior.

The player should not receive evidence automatically on every click.

Some objects should only reveal information after:

- A prerequisite clue.
- A different object examination.
- A contextual action.
- A specific investigative tool.

Create a contextual inspection panel.

When an object is selected, show:

- Object name.
- Visual.
- Description.
- Available actions.
- Previously discovered information.
- New observations.

Actions can include:

- Examine.
- Inspect closely.
- Photograph.
- Compare.
- Search.
- Collect, where appropriate.

Actions must be state-aware.

Avoid duplicate discoveries.

---

# 13. SUSPECT SYSTEM

Create five suspects.

Each suspect must have a detailed character profile.

Each profile should include:

- ID.
- Name.
- Age.
- Occupation.
- Relationship with the victim.
- Photograph or portrait.
- Personality.
- Public statement.
- Known motive.
- Hidden motive.
- Secret.
- Alibi.
- Actual movements.
- Knowledge of the crime.
- Behavioral traits.
- Contradictions.
- Suspicion score.
- Interview history.
- Dialogue state.
- Discovered information.

These fields should be stored in structured case data.

Never expose hidden fields directly in the UI.

## SUSPECT 1 — Eleanor Blackwood

Relationship: Wife.

Age: 48.

Occupation: Art patron.

Personality: Controlled, elegant, guarded.

Public statement:

She claims she was in the conservatory for most of the evening.

Secret:

She had recently discovered that Adrian was planning to change his will.

## SUSPECT 2 — Thomas Reed

Relationship: Personal secretary.

Age: 36.

Occupation: Secretary.

Personality: Nervous, precise, defensive.

Public statement:

He claims he was organizing correspondence in the office.

Secret:

He had altered a financial document and feared Adrian had discovered it.

## SUSPECT 3 — Clara Whitmore

Relationship: Family friend.

Age: 32.

Occupation: Art historian.

Personality: Intelligent, observant, evasive.

Public statement:

She claims she left the study before dinner and spent the evening in the gallery.

Secret:

She was involved in a dispute concerning a painting and its provenance.

## SUSPECT 4 — Daniel Blackwood

Relationship: Nephew.

Age: 27.

Occupation: Entrepreneur.

Personality: Impulsive, sarcastic, confrontational.

Public statement:

He claims he was in the billiard room.

Secret:

He was in debt and had recently asked Adrian for money.

## SUSPECT 5 — Margaret Shaw

Relationship: Housekeeper.

Age: 59.

Occupation: Housekeeper.

Personality: Calm, perceptive, observant.

Public statement:

She claims she was managing the household and preparing to retire for the night.

Secret:

She saw someone near the study shortly before the estimated crime window but did not initially disclose it.

---

# 14. INTERROGATION SYSTEM

Interrogation must be interactive.

Do not implement interrogation as a fixed dialogue sequence.

Create a suspect interview screen.

Display:

- Suspect portrait.
- Name.
- Relationship.
- Interview status.
- Known information.
- Interview transcript.
- Available dialogue actions.
- Evidence presentation controls.

Player interaction methods:

1. Free-text question.
2. Suggested questions.
3. Present evidence.
4. Challenge a statement.
5. Ask about a specific event.
6. End interview.

Examples of questions:

- Where were you at 9:45 PM?
- What was your relationship with Adrian?
- Did you hear anything from the study?
- Why did you leave the gallery?
- What do you know about the missing painting?

Implement a simulated dialogue engine.

The dialogue engine must:

- Detect question categories.
- Detect names and locations.
- Detect time references.
- Detect relevant evidence.
- Detect accusation-related language.
- Detect contradictions.
- Generate responses based on the suspect's personality and hidden facts.
- Maintain conversation context.
- Avoid revealing everything in a single response.
- Respond differently when evidence is presented.
- Allow repeated questioning without repeating the exact same dialogue.

Implement a hardcoded intent-matching system.

Use keyword detection, rules, structured state and contextual responses.

The simulation should feel intelligent even without AI APIs.

Do not simply match a keyword and return a generic sentence.

Use a combination of:

- Intent classification.
- State validation.
- Suspect memory.
- Evidence context.
- Dialogue state.
- Reaction logic.

Include multiple possible response variants.

---

# 15. EVIDENCE SYSTEM

Create a fully functional evidence archive.

Evidence categories:

- Physical.
- Digital.
- Testimonial.
- Documentary.
- Forensic.
- Circumstantial.

Create at least 15 hardcoded evidence items.

Evidence should be distributed across:

- Crime scene.
- Suspect interviews.
- Timeline.
- Household locations.
- Contextual discoveries.

Each evidence item should contain:

- ID.
- Title.
- Description.
- Category.
- Discovery location.
- Discovery condition.
- Associated suspect IDs.
- Associated timeline events.
- Importance.
- Reliability.
- Status.
- Interpretation.
- Possible connections.
- Evidence type.
- Discovery timestamp.

Evidence types:

- Direct.
- Circumstantial.
- Contradictory.
- Red herring.
- Supporting.

These classifications should not always be immediately visible.

Create a detailed evidence inspection screen.

Allow:

- Search.
- Filtering.
- Sorting.
- Opening evidence.
- Reviewing discovery context.
- Linking evidence to suspects.
- Linking evidence to timeline events.
- Comparing evidence.
- Reviewing evidence history.

Evidence must not be duplicated.

Evidence discovery should be state-driven.

---

# 16. HIDDEN CASE LOGIC

Create a central case engine.

Store the complete truth of the case separately from the player interface.

The case engine must contain:

- Culprit.
- Motive.
- Method.
- Crime timeline.
- Actual events.
- Suspect movements.
- Hidden relationships.
- Evidence dependencies.
- False leads.
- Contradictions.
- Required conclusions.
- Case resolution conditions.

The game must never display this information directly before the player reaches the reveal.

Use a structured case definition.

Do not mix the solution into UI components.

---

# 17. HARDcoded CASE TRUTH

For V1, implement a complete and internally consistent mystery.

The actual culprit is Thomas Reed.

However, the player must not know this until they investigate.

Truth:

Thomas Reed discovered that Adrian intended to expose his financial fraud.

Thomas manipulated the evening's events to create a misleading timeline.

He entered the study during a period when he believed the hallway was unobserved.

The crime was committed using a poisoned drink.

He attempted to manipulate the crime scene to suggest an alternative sequence of events.

His movements, financial records, access to the study and inconsistencies in his statements eventually expose him.

The case must have a logically consistent explanation.

Create a detailed hidden chronology of the actual events.

Every clue must be consistent with the hidden truth.

Do not make the culprit obvious from the initial briefing.

---

# 18. EVIDENCE DEPENDENCY ENGINE

Implement a dependency-based discovery engine.

Examples:

- Examining the glass reveals a basic observation.
- A closer examination reveals an additional detail.
- Comparing the glass with a suspect's statement may reveal a contradiction.
- Discovering the financial document enables a new questioning option.
- A timeline contradiction unlocks a new interrogation response.
- A specific evidence combination unlocks an additional deduction.

Use structured conditions rather than hardcoded UI logic.

Example architecture:

Evidence A + Evidence B + Suspect statement C = Contradiction unlocked.

Evidence D + Evidence E = New theory available.

Suspect interview + discovered document = New dialogue branch.

The system must allow future cases to use the same engine.

---

# 19. TIMELINE SYSTEM

Create a functional timeline.

Display:

- Known events.
- Approximate times.
- Suspect movements.
- Crime window.
- Evidence-related events.
- Contradictions.
- Player-added events.

Timeline events should be discovered progressively.

The timeline must not reveal the complete truth at the start.

Allow:

- Filtering by suspect.
- Filtering by evidence.
- Chronological ordering.
- Event details.
- Suspect movement comparison.
- Contradiction highlighting.
- Player-added notes.

Create a visual chronological timeline.

Use interactive event markers.

---

# 20. DETECTIVE BOARD

Create an interactive detective board.

This must not be a static mockup.

Allow the player to:

- Add evidence cards.
- Add suspect cards.
- Add timeline cards.
- Move cards.
- Create connections between cards.
- Remove connections.
- Add notes.
- Save theories.

Use a visual board with:

- Cards.
- Connections.
- Labels.
- Connection types.

Connection types:

- Related.
- Contradiction.
- Motive.
- Opportunity.
- Supports.
- Suspected.

Use drag-and-drop.

Save board state in localStorage.

Allow the board to be zoomed and repositioned if practical.

Make the board responsive.

Do not force the player to connect clues in a predefined manner.

---

# 21. CASE NOTEBOOK

Create a detective notebook.

The notebook should contain:

- Case notes.
- Suspect notes.
- Evidence notes.
- Timeline notes.
- Theories.
- Investigation history.

Allow the player to:

- Write notes.
- Edit notes.
- Delete notes.
- Save notes.
- Create theory entries.
- Mark a theory as unresolved.
- Mark a theory as supported.
- Mark a theory as rejected.

Notes must persist.

---

# 22. INVESTIGATION ACTION ENGINE

Create a central action engine.

The player should be able to enter actions such as:

- Search the desk.
- Examine the window.
- Question Thomas about the financial records.
- Ask Eleanor about her movements.
- Compare the clock with the timeline.
- Investigate the drink.
- Review the secretary's statement.

The game should interpret these actions.

The action engine should:

1. Receive the player's action.
2. Normalize the text.
3. Detect the action type.
4. Detect relevant objects.
5. Detect suspects.
6. Detect evidence.
7. Check investigation state.
8. Validate prerequisites.
9. Execute the action.
10. Update game state.
11. Discover evidence if appropriate.
12. Update the investigation log.
13. Generate a contextual response.
14. Update relevant UI.
15. Persist state.

Create a rule-based action interpreter.

Use multiple patterns and contextual rules.

Avoid making the system entirely dependent on a few keywords.

Create reusable functions.

---

# 23. SIMULATED AI DIRECTOR

Create a central DirectorEngine.

In future versions, this will be connected to an actual AI model.

For V1, implement a simulated director.

Responsibilities:

- Contextual responses.
- Investigation guidance.
- Investigation pacing.
- Suspect reactions.
- Hint generation.
- Discovery narration.
- Investigation feedback.
- State-aware suggestions.
- Unlocking investigative opportunities.
- Avoiding duplicate discoveries.

The Director should never reveal the culprit prematurely.

The Director must never randomly contradict the hidden truth.

Create multiple response templates with contextual logic.

The Director should use the current investigation state.

Do not create a random-response chatbot.

---

# 24. HINT SYSTEM

Implement a progressive hint system.

Three levels:

Hint 1:

Subtle direction.

Hint 2:

More specific investigative direction.

Hint 3:

Strong hint identifying the relevant evidence or contradiction.

Hints should:

- Be state-aware.
- Avoid immediately revealing the killer.
- Avoid revealing the complete solution.
- Be linked to the actual case logic.
- Be available only when relevant.

Include a hint button.

Allow the player to choose whether to use a hint.

Record hint usage.

Hints should influence the final investigation score.

---

# 25. FINAL ACCUSATION

Create a complete accusation screen.

The player must choose:

- Suspect.
- Motive.
- Method.
- Supporting evidence.
- Explanation.

Do not allow an empty accusation.

Allow the player to select multiple supporting evidence items.

Allow a written explanation.

Provide a final submit button.

The game should evaluate the accusation.

---

# 26. CASE EVALUATION ENGINE

Create a structured scoring system.

Score the investigation based on:

- Correct culprit.
- Correct motive.
- Correct method.
- Relevant evidence.
- Contradictions discovered.
- Timeline reconstruction.
- Investigation completeness.
- False accusations.
- Hint usage.
- Evidence quality.

Use a score out of 100.

Example scoring:

Culprit: 35 points.

Motive: 15 points.

Method: 15 points.

Supporting evidence: 20 points.

Timeline reconstruction: 10 points.

Investigation completeness: 5 points.

Hints can reduce the bonus score.

Do not make the score entirely dependent on collecting every clue.

Evidence reasoning should matter.

Implement different outcomes.

Outcome categories:

- Master Detective.
- Excellent Investigation.
- Case Solved.
- Partial Truth.
- Wrong Accusation.

The final evaluation must be deterministic and based on case data.

---

# 27. CASE REVEAL

After submission, display a cinematic case reveal.

Reveal:

- Actual culprit.
- Motive.
- Method.
- Actual chronology.
- Key clues.
- False leads.
- Suspect contradictions.
- Why the culprit was exposed.
- What the player missed.
- Investigation score.
- Final rank.

Show a detailed explanation.

The player must be able to understand the complete mystery after finishing.

Allow:

- Replay Case.
- Return to Case Files.
- Review Evidence.
- Review Timeline.

---

# 28. GAME STATE MANAGEMENT

Create a central game state.

It must include:

- Active case ID.
- Current screen.
- Investigation status.
- Discovered evidence.
- Suspect interview states.
- Suspect suspicion levels.
- Investigation history.
- Timeline state.
- Notebook entries.
- Detective board state.
- Player theories.
- Hints used.
- Investigation score.
- Current accusation.
- Case completion state.
- Game settings.

Create a clean state management approach.

Use React Context, reducer-based architecture or an appropriate lightweight state management system.

Avoid uncontrolled state scattered throughout components.

---

# 29. SAVE SYSTEM

Use localStorage.

Implement:

- Automatic saving.
- Resume investigation.
- Save indicator.
- Save timestamp.
- Case progress.
- Interview progress.
- Evidence.
- Notes.
- Timeline.
- Board layout.
- Settings.
- Investigation history.

Handle:

- Missing saves.
- Corrupted saves.
- Reset.
- New case.
- Replay.
- Multiple cases in future.

Use a save version.

Implement a basic migration structure for future versions.

---

# 30. SETTINGS

Create a functional settings screen.

Settings:

- Sound toggle.
- Music toggle.
- Animation toggle.
- Reduced motion.
- Text size.
- UI brightness if practical.
- Reset investigation.
- Reset all game data.

Settings must persist.

If audio is not implemented, do not pretend audio works.

---

# 31. ACTIVITY LOG

Create an investigation history log.

Record:

- Object examinations.
- Evidence discoveries.
- Suspect interviews.
- Statements.
- Contradictions.
- Timeline discoveries.
- Hints.
- Accusations.
- Important game events.

Display chronological history.

Allow filtering.

Activity logs should persist.

---

# 32. PROJECT ARCHITECTURE

Use a modular project structure similar to:

src/

  app/

    App.jsx

    routes.jsx

  components/

    layout/

      GameLayout.jsx

      Sidebar.jsx

      Header.jsx

      RightPanel.jsx

    common/

      Button.jsx

      Modal.jsx

      Tooltip.jsx

      ProgressBar.jsx

      EmptyState.jsx

      LoadingState.jsx

    investigation/

      InvestigationHub.jsx

      ActionInput.jsx

      ActivityLog.jsx

      SuggestedActions.jsx

    crimeScene/

      CrimeScene.jsx

      SceneHotspot.jsx

      InspectionPanel.jsx

    suspects/

      SuspectList.jsx

      SuspectProfile.jsx

      InterrogationPanel.jsx

      DialogueHistory.jsx

      EvidencePresentation.jsx

    evidence/

      EvidenceArchive.jsx

      EvidenceCard.jsx

      EvidenceDetails.jsx

      EvidenceFilters.jsx

    timeline/

      Timeline.jsx

      TimelineEvent.jsx

      TimelineFilters.jsx

    board/

      DetectiveBoard.jsx

      BoardCard.jsx

      BoardConnection.jsx

      BoardNotes.jsx

    notebook/

      Notebook.jsx

      NotesEditor.jsx

    accusation/

      AccusationForm.jsx

      CaseResults.jsx

      CaseReveal.jsx

    settings/

      Settings.jsx

  engine/

    GameEngine.js

    CaseEngine.js

    InvestigationEngine.js

    DirectorEngine.js

    ActionInterpreter.js

    SuspectEngine.js

    DialogueEngine.js

    EvidenceEngine.js

    DependencyEngine.js

    TimelineEngine.js

    BoardEngine.js

    HintEngine.js

    CaseEvaluator.js

    SaveEngine.js

  data/

    cases/

      blackwoodCase.js

    suspects.js

    evidence.js

    timeline.js

    dialogueTemplates.js

    actionRules.js

  hooks/

    useGameState.js

    useLocalStorage.js

  context/

    GameContext.jsx

  utils/

    textMatching.js

    helpers.js

    constants.js

  styles/

    global.css

    theme.css

    components.css

    layout.css

    animations.css

  main.jsx

You may adjust this structure if a better modular design is needed.

However:

- Keep components modular.
- Keep game logic out of UI components.
- Keep case data separate.
- Keep the truth separate from player-visible data.
- Keep engines reusable.
- Avoid giant files.
- Avoid circular dependencies.
- Avoid excessive abstractions.

---

# 33. ARCHITECTURE PRINCIPLES

Follow these principles:

## Separation of concerns

UI is responsible for displaying state.

Engines are responsible for game logic.

Data files are responsible for case definitions.

Save engine is responsible for persistence.

## Reusability

A future case should be added mainly by creating a case data file.

The UI and engines should not require major modifications.

## State-driven gameplay

Every discovery and interaction must update the actual game state.

Do not rely on screen-only variables for major game progress.

## Deterministic logic

The hidden case truth should be consistent.

Randomness may be used for dialogue variations only where it does not contradict case logic.

## Extensibility

The architecture should later support:

- AI-generated dialogue.
- AI-generated cases.
- Dynamic evidence.
- Real AI Director.
- Backend.
- Database.
- Multiplayer investigation.
- Voice interaction.
- Audio narration.
- More cases.
- Procedural mysteries.

---

# 34. FUTURE AI INTEGRATION DESIGN

Do not integrate AI APIs in V1.

But create a clear future integration boundary.

Create an interface or service abstraction that future AI implementations can replace.

Potential future services:

- AI Director.
- AI Suspect.
- Case Generator.
- Dialogue Generator.
- Investigation Analyzer.
- Hint Generator.
- Case Evaluator.

The current implementations should use hardcoded logic.

Future implementation should be able to replace the hardcoded engines without replacing the UI.

Avoid directly calling APIs from React components.

---

# 35. VISUAL ASSETS

Use appropriate visual assets.

The game should not look like a text-heavy admin dashboard.

Use:

- Crime scene illustrations.
- Suspect portraits.
- Evidence illustrations.
- Estate imagery.
- Background imagery.
- Subtle textures.
- Scene overlays.

If external assets are used:

- Prefer free assets.
- Avoid broken links.
- Avoid inaccessible remote images.
- Provide fallback visuals.
- Do not use assets that require paid licenses without permission.

If suitable assets cannot be found, use CSS-based illustrations or custom SVG illustrations.

The game must remain visually usable even if an image fails to load.

---

# 36. INTERACTION QUALITY

Every action must provide feedback.

Examples:

- Clicking an evidence card opens it.
- Examining an object generates an inspection result.
- Discovering evidence updates the archive.
- Interviewing suspects updates dialogue history.
- Presenting evidence changes suspect responses.
- Adding a connection changes the board.
- Saving notes persists notes.
- Accusing a suspect evaluates the case.
- Resetting a case actually resets it.

Avoid:

- Dead buttons.
- Placeholder interactions.
- Fake navigation.
- Static evidence.
- Repeated generic responses.
- Random unsupported discoveries.
- Empty screens.
- Broken mobile layouts.

---

# 37. GAMEPLAY FLOW

The complete gameplay flow must be:

Landing Screen

↓

Start Investigation

↓

Case Selection

↓

Case Briefing

↓

Investigation Workspace

↓

Crime Scene Investigation

↓

Evidence Discovery

↓

Suspect Interviews

↓

Timeline Reconstruction

↓

Detective Board

↓

Notebook & Theory Development

↓

Final Accusation

↓

Case Evaluation

↓

Cinematic Reveal

↓

Replay or Return to Cases

The player may navigate between investigative sections freely.

Do not force a rigid sequence except where the case logic requires prerequisites.

---

# 38. DEVELOPMENT REQUIREMENTS

Do not just generate a plan.

Create all project files.

Implement all screens.

Implement all core logic.

Implement all interactions.

Implement the complete case.

Implement localStorage.

Implement the game state.

Implement the action interpreter.

Implement interrogation.

Implement evidence dependencies.

Implement the timeline.

Implement the detective board.

Implement final evaluation.

Implement case reveal.

Implement responsive styling.

---

# 39. QUALITY ASSURANCE

Before declaring the project complete:

- Run the project.
- Check the build.
- Fix compilation errors.
- Fix import errors.
- Fix broken navigation.
- Fix state issues.
- Fix save issues.
- Fix broken buttons.
- Fix responsive layout.
- Check the complete case flow.
- Check the accusation flow.
- Check the reset flow.

Test the following scenarios:

1. Start a new case.
2. Examine the crime scene.
3. Discover evidence.
4. Interview a suspect.
5. Present evidence to a suspect.
6. Discover a contradiction.
7. Add evidence to the board.
8. Connect evidence.
9. Write a notebook entry.
10. Review timeline.
11. Save and reload.
12. Resume investigation.
13. Submit a correct accusation.
14. Submit a wrong accusation.
15. Review the case reveal.
16. Replay the case.
17. Reset the investigation.

Do not leave critical functionality broken.

---

# 40. FINAL DELIVERABLE

Deliver a complete, working V1 prototype of OBSCURA.

The project must:

- Run locally.
- Have a complete folder structure.
- Have clean code.
- Have functional UI.
- Have a fully playable case.
- Have hardcoded game logic.
- Have no backend requirement.
- Have no API requirement.
- Save locally.
- Be responsive.
- Be visually polished.
- Be extensible.
- Have a complete investigation loop.

Create the actual codebase now.

Do not stop at architecture planning.

Do not ask me to implement missing parts manually.

Do not output only code snippets.

Build the complete project, run it, debug it and finish the V1 prototype.

If you are operating in a coding workspace, create the files directly in the project folder.

If you cannot execute commands in the environment, output the complete project file structure and full source code for all required files without omitting essential files.

The goal is a playable, polished, immersive detective game prototype — not a concept presentation.

**OBSCURA — Nothing is what it seems.**
