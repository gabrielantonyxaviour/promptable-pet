# Promptable Pet

Build with MeDo Hackathon solo submission by Gabriel.

Promptable Pet is a persistent digital companion that evolves from daily sleep, mood, meal, and care inputs. The hook is simple: a pet that grows because you slept well.

## MeDo App

- Owned MeDo project URL: https://medo.dev/projects/app-brfxm7x6hxxd
- Public app URL: pending publish
- Primary track: Surprise Us!
- Backup track: Lifestyle & Game

## Product Loop

1. Start with the seeded pet state `sleepy-sprout`.
2. Enter today's care signals: sleep hours, mood, meal signal, and care action.
3. Click Evolve.
4. The pet changes posture, color, and care card.
5. A weekly evolution strip shows five cached state snapshots.
6. A state receipt explains which stored inputs drove the transition.

## MeDo Capabilities Used

- Data Storage for pets, daily logs, evolution states, and prompt receipts.
- Backend function for deterministic state transitions.
- Managed image-generation plugin path for pet state art.
- Cached generated states so judging does not depend on live paid generation.
- Multi-turn prompt refinement documented in `EXECUTION_PACKET.md`.

## Submission Packet

- `TEAM.md`: submitter and identity lane.
- `PLUGIN_PLAN.md`: managed/custom plugin recon and local skill mapping.
- `BACKEND_PLAN.md`: storage, user, function, and secrets plan.
- `UI_TEMPLATE_PLAN.md`: template inspiration and visual rules.
- `BUILD_PLAN.md`: build scope and milestones.
- `SUBMISSION_PORTAL_PLAN.md`: Devpost requirements and current status.
- `EXECUTION_PACKET.md`: README copy, demo script, video script, judging map, and final checklist.
