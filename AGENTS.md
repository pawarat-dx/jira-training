# Repository Guidelines

## Project Structure & Module Organization
- Root hosts `index.html` (main page) and `style.css` (shared styles); keep new pages alongside for easy preview.
- `assets/logo.svg` holds shared artwork; prefer vector or compressed images, name assets kebab-case.
- `.github` reserved for automation/config; mirror any workflow changes in this guide.
- No package manager files; treat project as static site to simplify onboarding.

## Build, Test, and Development Commands
- `python -m http.server 8080` from repo root serves the site at http://localhost:8080 for quick manual QA.
- `Start-Process index.html` (Windows) opens the file directly; use when no server is needed.
- No build step today; if you add tooling (e.g., npm), document new commands here.

## Coding Style & Naming Conventions
- Prefer 4-space indentation in HTML/CSS; keep inline styles minimal and centralize in `style.css`.
- Use semantic HTML and descriptive classes (kebab-case: `.pony-img`, `#local-time`).
- Keep palettes and spacing as CSS custom properties; extend `:root` variables instead of hardcoding.
- Run a quick format pass before commits (e.g., VS Code formatter) to avoid noisy diffs.

## Testing Guidelines
- Automated tests are not set up; perform manual checks after changes: load the page, confirm the clock updates each second, and ensure no console errors.
- For visual tweaks, compare against previous screenshots on common viewports (mobile width ~375px and desktop ~1280px).

## Commit & Pull Request Guidelines
- Follow existing history: start messages with the Jira issue key and concise summary (e.g., `PGI-30 #comment refine clock colors`).
- Reference the issue in PRs, describe user-impacting changes, and attach before/after screenshots for UI updates.
- Keep PRs small and focused; call out any new assets or external dependencies.
