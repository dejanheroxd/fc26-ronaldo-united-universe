# FC26 Ronaldo United Universe

Persistent canon database for the Cristiano Ronaldo / Manchester United EA FC 26 Manager Career universe.

## Core rule

**The game creates the football facts. The database preserves them. The story layer explains what they mean.**

User screenshots/results override speculation. No inconvenient result is rewritten. No restart becomes canon unless the user explicitly says so.

## Two clocks

EA FC screenshots currently display a 2025/26 calendar, while the fictional story chronology is 2029/30. Both are stored:
- `ui_date` / `ui_season`: what the game screen shows.
- `story_canon_season`: the universe chronology used in the narrative.

## Source hierarchy

1. `game_ui` — visible in a screenshot.
2. `user_confirmed` — explicitly supplied/corrected by the user.
3. `story_metric` — invented world-reaction metric that persists once introduced.
4. `inference` — allowed only when clearly labeled; never silently promoted to fact.

## Match recommendation

Before each upcoming match, recommend exactly one:
- `PLAY`
- `TACTICAL_SIM`
- `FAST_SIM`

Use rivalry, stakes, opponent strength, narrative importance, development arcs, and the need to avoid manually controlling everything.

## Story tone

Approximate 70/20/10 balance:
- 70% normal football reality
- 20% substantial storylines
- 10% major cinema/drama

Not every match needs a viral event.

## Tracker rule

Whenever a tracker is shown:
- show every active metric for that entity;
- show `previous → current`;
- retain history;
- keep conflicts instead of silently overwriting them.

## Fast-loading rule

For normal updates, only load:
1. `current_state.json`
2. affected entity files
3. relevant active storyline file(s)

The full archive does not need to be reread every turn.
