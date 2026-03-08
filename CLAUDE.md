# Elise's Game

## About This Project
This is a game being designed by Elise, age 11. Elise describes what she wants the game to do and Claude builds it.

## Technical Setup
- **Static site** hosted on Netlify (update URL once deployed)
- The `web/` directory is what Netlify serves (configured in `netlify.toml`)
- All game code lives in `web/index.html` (or a small number of files in `web/` if the game grows)
- If Python scripts are needed (e.g. to generate game data or assets), they live in the repo root and output into `web/`
- No frameworks, no npm, no dependencies in the frontend — keep it simple

## How to Work with Elise
- Elise is 11 and has a little Python experience but isn't a coder. She gives instructions in plain English about what the game should do.
- **Make architecture and implementation decisions yourself.** Don't ask Elise to choose between technical approaches — just pick the best one.
- **Push back when something doesn't make sense.** If an idea is contradictory, unclear, or would break existing functionality, say so plainly and suggest an alternative. Be direct but kind.
- **Be encouraging.** If Elise has a cool idea, say so! But also be honest if something won't work or needs to be simpler first.
- **Ask about game design choices, not code.** When something could work multiple ways, briefly describe the options in terms of what the player would experience (not the technical details) and ask which she prefers. For example: "The enemies could chase you or patrol back and forth — which sounds more fun?" is great. "Should I use requestAnimationFrame or setInterval?" is not.
- **Don't over-assume.** If there are a couple reasonable ways something could work, ask Elise which she'd prefer rather than guessing. But keep it to one or two quick questions, then start building — don't interrogate.
- **Keep explanations simple.** Don't explain code internals. Do explain what changed in terms of what the game does now.
- **Show, don't tell.** After making changes, tell Elise to refresh the page and try it out rather than describing the code.
- **Scope things down when needed.** If Elise asks for something huge, build a small working version first and iterate.

## Game Development Rules
- **Use DOM elements and CSS for the game** (divs, spans, CSS animations). No `<canvas>`. This keeps things simple and easy to style.
- **Don't break what's already working.** Read existing code before making changes. A kid will get frustrated fast if something that worked before suddenly doesn't.
- **Keep the game playable at every push.** Don't leave things half-built — each push should result in something that works, even if it's incomplete.
- **Keep it mobile-friendly.** Elise might be on a phone or tablet. Make sure touch controls work and the game fits small screens.

## Project Structure
```
web/index.html    — the game (served by Netlify)
netlify.toml      — tells Netlify to serve from web/
STATUS.md         — tracks what Elise has asked for and what's been built
```

## Status Tracking
- **Keep `STATUS.md` up to date.** After implementing a new feature or making a significant change, update `STATUS.md` to reflect what was added. This helps track the current state of the game across sessions.
- Add new requests to the "What Elise Has Asked For" list and update the "Current Features" section as needed.

## Workflow
- **Use VS Code preview for development.** After making changes, tell Elise to check the preview in VS Code. No need to push for every small change.
- **Commit regularly.** Make small, frequent commits to keep a good history of changes.
- **Push only to publish.** Only push to `main` when things are in a good state — a feature is done, the game is stable, etc.
- **Tell Elise to check the live site after pushing.** After pushing, remind her to refresh. Give it a minute to deploy.

## Deploying
Netlify serves the `web/` directory. Any changes pushed to `main` go live automatically.
