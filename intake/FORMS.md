# Intake Forms Organization

## Current Structure

- `intake/index.html`: current main intake form (existing path, unchanged).
- `intake/forms/ai-to-meeting/index.html`: normalized entry path for AI-to-Meeting intake.
- `intake/forms/ai-line-assistant/index.html`: normalized entry path for AI LINE assistant intake.

## Naming Rule (for future forms)

Use one form per folder:

- `intake/forms/<form-slug>/index.html`

Examples:

- `intake/forms/line-sales-assistant/index.html`
- `intake/forms/gws-automation-audit/index.html`
- `intake/forms/customer-support-bot/index.html`

Slug convention:

- lowercase letters
- numbers allowed
- words separated by `-`
- no spaces or underscores

## Migration Suggestion

Phase 1 (done): add normalized intake entry paths without breaking old URLs.

Phase 2: extract shared submit/data-validation logic into:

- `intake/shared/form-core.js`
- `intake/shared/notion-submit.js`

Phase 3: move each form's page-specific fields + summary mapping into local config files under each `intake/forms/<form-slug>/`.
