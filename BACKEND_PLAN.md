# Backend Plan

## Backend Services

Promptable Pet must not be frontend-only. Enable MeDo backend services before treating the app as build-ready.

## Data Storage

Tables/entities:

- `users`: id, displayName, createdAt.
- `pet_profiles`: id, userId, petName, species, currentMood, evolutionLevel, streak, currentImageKey, updatedAt.
- `daily_logs`: id, userId, date, sleepHours, mood, foodNote, careAction, generatedExplanation, createdAt.
- `evolution_events`: id, userId, dailyLogId, previousState, nextState, imageKey, reason, createdAt.
- `cached_pet_states`: imageKey, title, mood, color, posture, habitat, prompt, assetUrl.

## User Management

Use MeDo Login only if it is quick. If not, ship a demo-mode profile with a clear "Judge demo pet" state and persistent backend records.

## Backend Functions

- `computePetState(input, previousState)`: maps daily inputs to mood, color, posture, habitat, evolution level, streak, and image key.
- `saveDailyLog(input)`: stores the log and evolution event.
- `generateExplanation(input, transition)`: uses LLM plugin or deterministic fallback text.

## Secrets

- Store image/LLM plugin credentials in MeDo secrets if required by the platform.
- Do not hardcode API keys in the app or repo.

## Reliability

Use cached pet states for the critical judge path. Live image generation may be exposed as "Generate a new variant" after the core state update works.

## Current MeDo Evidence

MeDo generated `Requirement.md`, lists backend services as Supabase/backend storage in the requirements, and entered an implementation task saying it is setting up backend tables and functions. Final confirmation is pending until the generated app can be previewed and published.
