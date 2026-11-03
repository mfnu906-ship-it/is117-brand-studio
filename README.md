# IS117 Brand Studio

**PUREFORM's Modernist brand direction centers on a promise of simple, affordable everyday T-shirts.** This project applies its audience hypotheses, Everyman character, friendly voice, original geometric P logo, neutral palette with rust-red accents, and two optional styling features to a working storefront and live style guide.

BRAND-001 is still in progress; its pull request has not yet been created or merged. The audience and product claims remain hypotheses or unsubstantiated learner-proposed language; the page uses fictional demo product data. The demo bag does not take payments or place orders.

**A short record, visible to you:** your AI coach updates [LEARNING.md](LEARNING.md) with brief task-related explanations, observations and help received. It is AI-drafted, not a full transcript, and may be public with your repository. Review it and correct or remove excerpts before they are committed or pushed. Your instructor uses it alongside the project with this [simple three-part rubric](docs/assessment.md); the AI does not assign your grade.

## Start here

1. Open [this template on GitHub](https://github.com/kaw393939/is117-brand-studio), select **Use this template → Create a new repository**, and create a **public** repository in your own account. Wait until the new repository shows its README before cloning. A template copy does not copy the instructor's issues.
2. In your terminal, replace both placeholders with your account and new repository name:

   ```sh
   git clone git@github.com:USERNAME/REPOSITORY.git
   cd REPOSITORY
   ```

3. Select this cloned folder as the chat's local project in ChatGPT desktop/Codex, or another AI agent that can **read and edit local files and run terminal commands**. Have the agent report its current folder and Git remote before installing anything. A browser-only conversation cannot do the whole exercise. VS Code is optional; an editor extension or separate agent CLI is not required. Start one chat with:

   > Read AGENTS.md and SPEC.md. Help me get this running, then guide me through the brand studio one decision at a time.

4. Let the agent check Node.js **22.16+ on the 22 LTS line (recommended), or 24+**, and npm, run `npm ci` and `npm run check`, and help with any setup errors before making further project changes.
5. Return to the terminal you used to clone, still inside your repository, and run:

   ```sh
   npm run dev
   ```

   Open the address printed by the server in your browser (normally `http://127.0.0.1:5173`). Leave this terminal running while you work. The agent can edit files and run checks in its separate project terminal.

Save an HTML, CSS, JavaScript, or asset file under `public/` to refresh the local browser automatically; unsaved edits do not appear. A refresh resets the temporary demo bag. `npm start` is an alias for this same development mode. Press **Ctrl+C** in the terminal running the server to stop it. To switch to a plain preview, stop the server first, then use `npm run preview` and reopen its printed address. Refresh the browser yourself after saving. These commands serve your local files; publishing to GitHub Pages is a later step.

**First success checkpoint:** open the PUREFORM storefront, choose a size, and add the shirt to the demo bag. Tell the agent what you actually see. The bag is a demonstration; it does not take payments, persist between visits, or place orders.

If a command fails, paste the real error into the same chat. If the port is in use, let the agent help you stop your earlier preview or use `PORT=5175 npm run dev`, then open its printed address. You can ask for a hint, an example, or a small recommendation at any time. You do not need to know the branding vocabulary first.

**Returning later:** reopen the same local clone and chat. Have the agent read SPEC.md and LEARNING.md to resume the next step. Check the server terminal first; if it is still running, use its printed address. Otherwise run `npm run dev` from your repository again, reusing any chosen `PORT` prefix. You normally do not need to clone or install dependencies again.

## Work one decision at a time

PUREFORM's decisions and implementation evidence are recorded in [SPEC.md](SPEC.md); the short learner contribution and review record is in [LEARNING.md](LEARNING.md). The audience descriptions are hypotheses, not customer research. The Modernist direction, original logo, live style guide, free styling tip, and optional style-goal suggestions are part of the current storefront.

`BRAND-001` is in progress on `feature/brand-001`, with issue #1 in the student repository. The current LEARNING.md excerpts have been reviewed for accuracy. The pull request and merge decision remain for the learner; keep the feature in progress until the pull request is merged. There is no checkout, payment, account, or persistent bag.

Saved changes under `public/` refresh the local site; the demo bag resets when the page reloads. Use the prepared checks described below when making further changes, and record only observations that were actually made. No customer evidence or unsupported product facts should be added.

## What is here

| File                                   | Purpose                                                                                                    |
| -------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| `public/index.html`                    | PUREFORM storefront with optional style goals, styling suggestions, size selector, and demo bag            |
| `public/styleguide.html`               | Live identity board using the storefront's shared styles and assets                                        |
| `public/studio.html`                   | Short studio overview, also [available online](https://kaw393939.github.io/is117-brand-studio/studio.html) |
| [SPEC.md](SPEC.md)                     | The concise record of your chosen decisions and evidence                                                   |
| [AGENTS.md](AGENTS.md)                 | Instructions for your AI coach                                                                             |
| [LEARNING.md](LEARNING.md)             | Brief AI-drafted conversation evidence for you to review; no full transcript or automatic grade            |
| [docs/reference.md](docs/reference.md) | Short explanations and source links to use when needed                                                     |

The README is the authoritative startup path. The online overview introduces the exercise; it does not replace your local project or chat.

## Prepared checks

`npm run check` runs formatting, HTML/CSS/JavaScript lint, server tests, and a real Chromium browser journey with Playwright and axe accessibility checks. Use `npm run format` to fix formatting, then check again. Fix lint problems in the source; keep the prepared rules. If Chromium is missing, the agent can explain and run `npm run setup:browser`, then retry. That command installs the browser dependency; it is not an additional tool choice.

Positive cases check intended behavior, such as adding a selected size. Negative cases check unsuitable input, such as trying to add without a size. These are different from test **levels**: unit checks focus on a small function, integration checks join parts, and end-to-end checks drive a user journey in a real browser.

Checks can find defects and some accessibility barriers. They do not verify that the page and guide express the same identity; compare their logo, typography, components, and voice in the browser. They cannot prove that your audience will value the brand, that a claim is true, or that every person can use the site. Your own browser observation adds evidence; it does not stand in for customer research.

After `BRAND-001`, choose **one** next cycle with less guidance: perhaps a useful brand story, a fit guide with supported information, or a richer demo bag. A real checkout would be a separate project decision.

## Publish when you keep the site

After you approve keeping the checked change and it is merged into `main`, you can publish it. Let the agent guide you through your repository's **Settings → Pages → Source → GitHub Actions**, then **Actions → Check and publish → Run workflow** on `main`. Open the deployment URL reported by that run. Later pushes to `main` publish automatically after checks pass. Until Pages is configured, the workflow checks the project and skips publishing successfully; first setup does not require deployment.

If Settings is missing or shows a 404, sign into the owning GitHub account in that browser. Terminal SSH authentication does not sign the browser in.
