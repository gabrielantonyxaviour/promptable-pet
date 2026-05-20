# Plugin Plan

## Product Thesis

Promptable Pet should prove MeDo can combine persistent app state, backend logic, and generative media into a charming product. The plugin story must be honest: persistent state plus image generation plus explanatory LLM text, not fake "plugin chaining."

## Managed Plugins To Use

- `Image Generation (Nano Banana Pro)` or the lower-cost image generation plugin:
  - Generate or pre-generate pet evolution states.
  - Use cached deterministic states for judging reliability if live generation is slow or credit-heavy.
- `Large language Model`:
  - Generate the "why your pet changed" explanation from sleep, mood, food, and care streak inputs.
  - Keep explanations short and deterministic enough for a repeatable demo.
- Optional `Text-to-Speech`:
  - Only use if MeDo can add it quickly as a pet voice line.
  - Skip if it slows the core 5-second hero moment.

## Custom Skill Decision

Create a custom skill only if MeDo supports it quickly:

- Name: `Pet State Transition Engine`
- Input: mood, sleep hours, meal/care notes, streak, previous state.
- Output: pet mood, body color, posture, habitat, evolution level, explanation, and cached image key.

If custom skill creation is slow, implement the same state-machine logic in backend functions and describe it as the custom-skill path in the submission.

## Local Skill Inspiration

- `product-judgment`: keep the app useful, not only cute.
- `ui-design` / `frontend-design`: use high-end visual interaction patterns.
- `imagegen` / `openai-image-gen`: inspiration for cached pet-state image prompts.

## Demo Moment

The judge enters "8h sleep, calm mood, cooked dinner" and the pet changes immediately. The app shows the plugin-backed/cached pet image, backend state update, and a one-sentence explanation.

