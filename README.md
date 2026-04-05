# DECKIO Starter

A Dev Container template that spins up a [DECKIO](https://deckio.art/) presentation project in seconds — no local dependencies required.

## What is DECKIO?

[DECKIO](https://github.com/deckio-art/deck-engine) is a presentation framework powered by `@deckio/deck-engine`. It is designed to be driven by GitHub Copilot in Agent mode: you describe the slide you want, Copilot edits the deck files, and the browser preview hot-reloads instantly.

## What this repo does

When you open this repository in a Dev Container (locally or via GitHub Codespaces), the container:

1. Scaffolds a new DECKIO project with `create-deckio` into the working directory.
2. Installs all npm dependencies.
3. Creates an initial git commit.
4. Forwards port `5173` and opens a live preview in VS Code's Simple Browser.

The result is a fully working DECKIO presentation project, ready for you to start building slides with GitHub Copilot.

## Getting started

### Option 1 — GitHub Codespaces (recommended, zero setup)

Click **Code → Codespaces → Create codespace on main** in the GitHub UI. The container will build and the presentation preview will open automatically.

### Option 2 — Dev Container locally

Prerequisites: [Docker](https://www.docker.com/) and the [Dev Containers extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) for VS Code.

1. Clone this repository:

   ```bash
   git clone https://github.com/DevSecNinja/deckio-starter.git
   cd deckio-starter
   ```

2. Open in VS Code and, when prompted, click **Reopen in Container** — or run the **Dev Containers: Reopen in Container** command.
3. Wait for the container to build and the bootstrap script to finish. The presentation will open at `http://localhost:5173`.

## Building slides with GitHub Copilot

Once the container is running and the presentation is visible, use GitHub Copilot Chat in **Agent mode** to drive all deck changes. Use a frontier model such as Claude Sonnet or GPT-4o for best results.

Example prompts:

- `Add a slide that explains the rollout phases for strategic customers.`
- `Make this slide easier to scan and easier to present.`
- `Remove the speaker invite slide.`
- `Review this deck and fix anything that looks inconsistent or broken.`
- `Create a new slide based on my sketch.`

Copilot already knows which files to touch thanks to the built-in instructions and skills included by `create-deckio`.

## Pre-installed VS Code extensions

The Dev Container ships with:

| Extension | Purpose |
|---|---|
| GitHub Copilot + Copilot Chat | Drive deck changes with natural language |
| GitLens + Git Graph | GitOps workflow |
| Prettier | Format on save |
| ESLint | Code quality |

## Optional: download source assets

If your deck references offline PDF assets, run the included helper script once to download them into `assets/`:

```bash
chmod +x setup.sh && ./setup.sh
```

The `assets/` directory is git-ignored and is not committed to the repository.

## Links

- [DECKIO website](https://deckio.art/)
- [deck-engine repository](https://github.com/deckio-art/deck-engine)
- [Dev Containers documentation](https://containers.dev/)
- [GitHub Codespaces documentation](https://docs.github.com/en/codespaces)

## License

MIT — see [LICENSE](LICENSE).
