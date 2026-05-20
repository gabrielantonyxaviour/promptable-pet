---
name: promptable-pet-care-signal-engine
description: Deterministic care-signal scoring and pet evolution engine for Promptable Pet. Converts sleep, mood, meal, care, and streak inputs into an explainable pet stage, state receipt, backend event payload, and art prompt.
---

# Promptable Pet Care Signal Engine

Use this skill inside Promptable Pet whenever the app needs to turn daily user care inputs into a deterministic pet evolution result. This is intentionally not a generic wellness scorer. It is a hackathon demo engine for a digital pet whose state changes from care signals while staying explainable, persistent, and safe for judges to test.

## Inputs

Accept a JSON object with:

```json
{
  "sleepHours": 8,
  "mood": "calm",
  "mealSignal": "cooked dinner",
  "careAction": "played",
  "streakDays": 4,
  "previousStage": "sprout"
}
```

Allowed mood values: `calm`, `hopeful`, `focused`, `tired`, `stressed`, `sad`.

Allowed meal signals: `cooked dinner`, `balanced`, `snack`, `skipped`, `takeout`.

Allowed care actions: `played`, `walked`, `checked in`, `breathed`, `rested`, `none`.

## Scoring

Score each input:

- Sleep: 0 to 4 hours = 0, 5 to 6 = 1, 7 to 8.5 = 3, 9 to 10 = 2, above 10 = 1.
- Mood: calm, hopeful, focused = 2; tired or sad = 1; stressed = 0.
- Meal: cooked dinner or balanced = 2; snack or takeout = 1; skipped = 0.
- Care: played, walked, checked in, breathed, rested = 2; none = 0.
- Streak bonus: 0 for no streak, 1 for 2 to 3 days, 2 for 4 or more days.

Total score range: 0 to 11.

## Evolution Stages

Map total score to a stage:

- 0 to 2: `dormant-egg`
- 3 to 4: `sleepy-sprout`
- 5 to 6: `steady-bloom`
- 7 to 8: `bright-companion`
- 9 to 10: `radiant-guardian`
- 11: `legendary-luma`

Do not jump more than two stages from the previous stage in a single day. If the score implies a larger jump, cap the result at two stages higher and set `cappedEvolution` to true.

## Output

Return JSON only:

```json
{
  "stage": "radiant-guardian",
  "score": 9,
  "scoreBreakdown": {
    "sleep": 3,
    "mood": 2,
    "meal": 2,
    "care": 2,
    "streak": 0
  },
  "cappedEvolution": false,
  "judgeExplanation": "Luma reached Radiant Guardian because strong sleep, calm mood, and cooked food created a high-care day.",
  "stateReceipt": [
    "Sleep contributed 3 points",
    "Mood contributed 2 points",
    "Meal contributed 2 points",
    "Care action contributed 2 points"
  ],
  "eventPayload": {
    "eventType": "pet_state_computed",
    "source": "custom_skill_promptable_pet_care_signal_engine",
    "stage": "radiant-guardian",
    "score": 9
  },
  "artPrompt": "A radiant small digital companion pet, warm mint and coral glow, cozy habitat, expressive but non-medical, premium playful app icon style"
}
```

## Explanation Rules

- Explain the pet change, not the user's health.
- Avoid medical, therapy, diagnostic, or treatment language.
- Keep judge explanations under 22 words.
- Mention the strongest positive driver first.
- If the score is low, make the copy gentle and actionable.

## Demo Path

For the judge demo input:

```json
{
  "sleepHours": 8,
  "mood": "calm",
  "mealSignal": "cooked dinner",
  "careAction": "played",
  "streakDays": 4,
  "previousStage": "steady-bloom"
}
```

Return `legendary-luma` only if the capped evolution rule allows it. Otherwise return `radiant-guardian` with `cappedEvolution: true`.

## Backend Integration

When the app uses this skill, store the returned object in:

- `daily_logs.skill_output`
- `evolution_events.event_payload`
- `pet_profiles.current_stage`
- `cached_pet_states.art_prompt`

Surface `source: custom_skill_promptable_pet_care_signal_engine` in the Build Witness drawer so judges can see the custom skill was part of the app architecture.
