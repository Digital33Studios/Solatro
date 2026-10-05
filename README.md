<img width="960" height="544" alt="image" align="center" src="https://github.com/user-attachments/assets/6dace07a-b42b-430f-bbf2-e4cbbd7329d2" />

# SOLATRO
**Solitaire, with a score-chasing problem.**
Solatro is a fast, arcade-style take on Klondike Solitaire inspired by the presentation, momentum, and ridiculous-number energy of *Balatro*. (I love Balatro!)
At its core, it is still real Solitaire: build descending alternating-color tableau stacks, reveal hidden cards, manage the stock and waste, and complete all four foundations.
But Solatro adds another question:
> **Can you win cleanly enough to make the numbers explode?**

---
## About
Solatro takes classic (Klondike) Solitaire and layers a scoring system over every meaningful decision.
Progress earns **Pips**. Maintaining momentum builds **Flow**. Chaining productive plays builds **Cascade**.
Together:

```text
PIPS × FLOW × CASCADE = SCORE
```

A normal play might earn a few hundred points.
A well-planned sequence can suddenly turn into:

```text
250 PIPS
× 1.84 FLOW
× 14 CASCADE

= 6,440 SCORE
```

And once a run catches fire, the HUD catches fire with it.
The goal isn't simply to solve Solitaire.
The goal is to solve it **beautifully**.

---
## Gameplay

Solatro follows standard (Klondike) fundamentals:
- Seven tableau columns with alternating-color descending stacks
- Four ascending suit foundations
- Stock and waste piles
- Foundation rollback
- Quick-send to Foundation
- Automatic endgame completion
- Undo support
- Stalemate / no-progress detection
- Controller-first navigation
- True animated Klondike opening deal
- Persistent statistics and personal records
But every move also affects the scoring engine.

---
### Pips
Pips represent real Solitaire progress.
Examples include:

```text
Reveal a hidden card
Send a new card to Foundation
Open a tableau column
Complete a suit
Win the deal
```

Pips are intentionally protected against simple score farming. Progress awards are tracked so repeatedly moving the same cards around cannot endlessly generate points.

---
### Flow
Flow is your long-term momentum.
Productive play pushes it upward.
Messy play pulls it down.

```text
Clean progress       ↑ Flow
Ordinary shuffling   ↓ Flow
Stock recycling      ↓ Flow
Foundation rollback  ↓ Flow
```

Flow builds from roughly:

```text
×1.00 → ×3.00
```

and represents how efficiently the entire deal is being played.

---
### Cascade
Cascade is the volatile part.
Consecutive productive actions build a chain:

```text
CAS ×1
CAS ×2
CAS ×3
CAS ×4
...
```

Special actions can accelerate it even faster.
Stock browsing can preserve the chain, but unnecessary tableau movement, recycling, and backtracking can break it.
This creates a scoring decision that doesn't exist in ordinary Solitaire:
> Do you make the obvious move immediately, or prepare the board for a much larger sequence?
Flow × Cascade becomes the live **MULT** shown in the HUD.
And yes, sufficiently large multipliers set the scoring display on fire.

---
## Presentation
Solatro is heavily focused on tactile feedback.
Cards have spring-based movement, hover, tilt, rotation, flip animation, drag response, snapping, jiggle, and juice effects.
Moving cards are automatically promoted above the board while travelling, whether they are:

```text
Dragged
Returned after an invalid move
Drawn from Stock
Moved from Waste
Sent to Foundation
Pulled back from Foundation
Quick-sent
Auto-sent
Auto-completed
Dealt at the start of a round
```

The right-side scoring HUD tracks:

```text
SCORE
PIPS × MULT
FLOW
MOVES
TIME
STREAK
ROUND
```

Higher multipliers escalate the visuals rather than simply displaying a larger number.
The intention is for a huge scoring sequence to **look, sound, and feel huge**.

---
## Stalemates
(Klondike) is not guaranteed to be solvable. Trust me my vigorous testing if proof, many games of Solitaire, oh so many.
Solatro uses both board-state analysis and repeated no-progress stock cycles to identify deals that appear stuck.
When no useful progression remains, the player can:

```text
Start a new deal
Return to the main menu
```

---
## Collection
Solatro includes a Collection system for cosmetic customization.
The long-term plan is to provide unlockable:

```text
Card backs
Card faces
Deck cosmetics
Run achievements
Progression rewards
```

The standard red card back is available from the beginning.
Additional cosmetics are intended to be earned through accomplishments such as high Cascade streaks, score milestones, fast wins, low-move victories, completed suits, and total wins.
The Collection is **currently under active development**. I repeat, the Collection is **currently under active development**.

---
## Audio

Solatro includes separate volume control for music and sound effects.
Music continues seamlessly between the menu and gameplay rather than restarting between rooms.
Gameplay audio includes dedicated feedback for:

```text
Card movement
Card flips
Flow / multiplier increases
Cascade / X-Mult increases
Stalemates
Victories
```

As the scoring engine escalates, the audio is intended to escalate with it.

---
## Controls
Solatro is designed primarily around the PSVita and of course, a gamepad for Dev work on the PC.

```text
D-Pad / Left Stick  Navigate cards and piles
Cross               Select / move / draw
Triangle            Quick-send to Foundation
Circle              Cancel
Square              Undo
```

During the opening deal:

```text
Cross               Fast-forward the remaining deal
```

Keyboard controls are also available during development.

---

## Saving
Solatro maintains persistent profiles with statistics including:

```text
Games played
Games won
Best score
Best Flow
Best time
Fewest moves
Selected card back
Collection progress
```

An active Solitaire deal can also be saved and resumed.

---
## Technology

Solatro is built in:
**GameMaker Studio 1.4.9999**
A major development target is the **PlayStation Vita**, so performance and memory usage are treated as first-class constraints.
The game and UI, shaders, animation, save behavior, and asset usage are designed with Vita hardware in mind. So the background 
shader had to take a hit on resolution, while I still haven't done the CRT shader don't worry, all in due time.

---
## Current Status
**Work in progress.**
The core Solitaire game is fully playable and currently includes:

```text
Klondike gameplay
Controller navigation
Animated cards
True opening deal
Undo
Save / Continue
Auto Complete
Stalemate detection
Pips
Flow
Cascade
Score tracking
Personal records
Dynamic scoring HUD
Shader-driven background
Music and SFX settings
Profile support
Early Collection system
```

Current development is focused on polish, scoring feel, cosmetics, Collection progression, and pushing the audiovisual feedback further.

---
## Design Goal
Solatro is not trying to turn Solitaire into poker.
It is trying to answer a different question:
> **What if winning Solitaire felt like building a ridiculous scoring engine?**
The cards are still Solitaire cards.
The decisions are still Solitaire decisions.
But when everything lines up, the numbers should become completely unreasonable.
And that's the point.

---
## Project Name

**SOLATRO**
A Solitaire sister-game built around momentum, chaining, score optimization, and the deeply irresponsible pursuit of larger numbers.
