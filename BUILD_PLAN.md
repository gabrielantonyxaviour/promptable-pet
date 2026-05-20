# Build Plan

## Goal

Build Promptable Pet: a persistent digital pet that evolves from daily human inputs and explains its emotional state.

## Track

Primary: Surprise Us
Backup: Lifestyle & Game

## Critical Judge Moment

Within 5 seconds:

1. User enters sleep/mood/care input.
2. Pet visibly changes.
3. Week strip updates.
4. Explanation card appears.

## Build Steps

1. Enable MeDo backend services.
2. Create storage for pet profile, daily logs, evolution events, and cached pet states.
3. Add state-transition backend function.
4. Add image generation plugin or cached image-state fallback.
5. Add LLM explanation plugin or deterministic explanation fallback.
6. Build high-end single-screen app with pet scene, input controls, week strip, and Build Witness drawer.
7. Publish public MeDo URL.
8. Smoke test public URL and capture screenshots.

## Owned URLs

- MeDo project URL: https://medo.dev/projects/app-brfxm7x6hxxd
- Public app URL: pending

## Kill Conditions

- If backend cannot be enabled quickly, keep demo-mode persistence but document blocker.
- If image generation fails or credits are too expensive, use cached pet states and expose live generation as optional.
- If custom skill creation blocks progress, implement state machine as backend function.
