Execute this hackathon idea.

Hackathon: build-with-medo-hackathon
Idea: Promptable Pet
Execution workspace: /Users/gabrielantonyxaviour/Documents/hackathons/build-with-medo-hackathon/execution/2026-05-20T03-56-39Z-promptable-pet
Report output: /Users/gabrielantonyxaviour/Documents/hackathons/build-with-medo-hackathon/execution/2026-05-20T03-56-39Z-promptable-pet/outputs/builder-report.md

## Assigned Solo Submitter

This is a solo Build with MeDo submission. Use exactly this identity unless Gabriel explicitly overrides it:

- Project: Promptable Pet
- Primary submitter / repo owner: Gabriel
- chromeDir: "Default"
- chromeProfile: "Gabriel"
- email: gabrielantony56@gmail.com
- agent-browser session stem: "medo-gabriel-promptable-pet"

Submission portal target:
- Devpost: https://medo.devpost.com/

Required browser preflights:
agent-browser --session medo-gabriel-promptable-pet-app --profile "Default" --allowed-domains "medo.dev,www.medo.dev,*.medo.dev,miaoda-resource-static.s3cdn.medo.dev,miaoda-font.cdn.bcebos.com,fonts.googleapis.com,fonts.gstatic.com" open "https://medo.dev/"
agent-browser --session medo-gabriel-promptable-pet-plugins --profile "Default" --allowed-domains "medo.dev,www.medo.dev,*.medo.dev,miaoda-resource-static.s3cdn.medo.dev,miaoda-font.cdn.bcebos.com" open "https://medo.dev/plugin?source=managed"
agent-browser --session medo-gabriel-promptable-pet-devpost --profile "Default" --allowed-domains "medo.devpost.com,devpost.com,www.devpost.com,github.com,www.github.com,mail.google.com,accounts.google.com,google.com" open "https://medo.devpost.com/"

Hard isolation rules:
- Never use another persona's Chrome profile, MeDo app, Devpost draft, GitHub repo, or browser session.
- Never run agent-browser close --all. Close only your own named sessions.
- If agent-browser reports that --profile was ignored, stop and relaunch with a fresh session name before doing anything else.
- If the current URL is another run's known app URL, for example app-amaxapjx24g0 or app-brcr7qqqmadd, stop and create/open this run's own MeDo app instead of editing it.
- Record the first owned MeDo project URL and public app URL in STATE.json, BUILD_PLAN.md, and EXECUTION_PACKET.md as soon as they exist.


Required source files:
- /Users/gabrielantonyxaviour/Documents/agents/docs/hackathons/browser-execution-runbook.md
- /Users/gabrielantonyxaviour/Documents/agents/docs/hackathons/medo-execution-runbook.md
- /Users/gabrielantonyxaviour/Documents/hackathons/submission-profile-registry.json
- /Users/gabrielantonyxaviour/Documents/templates/INDEX.md
- /Users/gabrielantonyxaviour/Documents/hackathons/build-with-medo-hackathon/council/LATEST

Execution contract:
0. Execution/code-building authority is GPT-5.5 or Claude Opus 4.7 only. Do not use Kimi to build project code. If Kimi artifacts exist, treat them as planning notes that must be verified before implementation.
1. Read the browser execution runbook, the MeDo execution runbook, and profile registry before any GitHub, MeDo, Contra, Devpost, Gmail, or submission-portal work.
2. Read the latest council run for this hackathon: TOP_10.json, EXECUTION_QUEUE.json, IDEAS.md, and the most relevant outputs/*.md files.
3. Before app generation, perform MeDo platform reconnaissance and write PLUGIN_PLAN.md:
   - Open https://medo.dev/plugin?source=managed with the assigned profile and list managed plugins/skills relevant to this idea.
   - Open https://medo.dev/plugin?source=custom with the assigned profile and decide whether a custom plugin/skill is useful and feasible.
   - Browse local skills under /Users/gabrielantonyxaviour/.agents/skills and /Users/gabrielantonyxaviour/.codex/skills for reusable capability ideas. Use a skill only when it strengthens the product, not as decoration.
   - Pick at least one concrete plugin/skill integration path, or write a defensible reason why a plugin would be fake/weak for this idea.
4. Before app generation, enable or explicitly request MeDo backend services and write BACKEND_PLAN.md:
   - Data Storage: tables/entities and relationships.
   - User Management: whether login/users are needed for the demo.
   - Backend Functions: server-side logic, scheduled/event logic, or transformation logic.
   - Secrets: any API key placeholder or secure integration plan.
   - If the UI says backend services are not enabled, use the MeDo chat/action to add backend services before treating the app as build-ready.
5. Before app generation, inspect /Users/gabrielantonyxaviour/Documents/templates/INDEX.md and the most relevant template prompt/source. Write UI_TEMPLATE_PLAN.md with the chosen inspiration, visual system, first-screen judge moment, and what should be copied as a design pattern. High-end UI is required; a plain CRUD dashboard is not acceptable.
6. Write these files in the execution workspace:
   - TEAM.md: exact person, Chrome profile directory, email, and ownership role for this solo submission.
   - BUILD_PLAN.md: concrete build plan, stack, app scope, demo path, plugin/backend choices, UI direction, and timeboxed milestones.
   - PLUGIN_PLAN.md: managed/custom MeDo plugin reconnaissance plus local skill mapping.
   - BACKEND_PLAN.md: MeDo backend services and data/function/secrets plan.
   - UI_TEMPLATE_PLAN.md: selected template inspiration and visual implementation rules.
   - REPO_PLAN.md: public repo name, owner, creation method, visibility proof, and push/deploy steps.
   - SUBMISSION_PORTAL_PLAN.md: portal URL, account/profile used, required fields, assets still missing, and current prefill status.
   - EXECUTION_PACKET.md: single source of truth for README, demo script, video script, judging criteria mapping, links, and final checklist.
7. Create or verify a proper public GitHub repo for the selected primary owner only after confirming the active GitHub account matches the assigned chromeDir/profile. Use agent-browser for persona-owned repo creation when the repo must belong to a specific persona. Do not create private repos for hackathon submissions unless the rules explicitly require it.
8. Start submission portal preparation in parallel with build work: open the relevant portal with agent-browser, confirm login/profile, identify required fields, and record evidence in SUBMISSION_PORTAL_PLAN.md. Prefill only reversible fields if the portal safely supports drafts. Stop before legal attestations, eligibility checkboxes, irreversible registration, or final submission unless Gabriel explicitly authorizes that exact action.
9. Begin reversible setup and implementation immediately after the plans are written. Reversible setup includes scaffolding the app/repo, writing README/demos/scripts, preparing seed data, opening the owned MeDo app, enabling backend services, and starting app implementation. Do not stop at a plan if build work can begin.
10. Keep a live progress log at PROGRESS.md with timestamped notes every phase, including blockers, exact files changed, active browser session name, owned MeDo app URL, and public app URL when known.
11. Write the final builder report to /Users/gabrielantonyxaviour/Documents/hackathons/build-with-medo-hackathon/execution/2026-05-20T03-56-39Z-promptable-pet/outputs/builder-report.md. The report must include repo status, submission portal status, plugin/backend status, UI/template status, build status, blockers, and next actions.

Start now.