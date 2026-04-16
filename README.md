# Daniel J Todo Task Card

A single, interactive Todo / Task Card built with plain HTML, CSS, and JavaScript.

## What Changed

The previous design behaved more like a small task app with a task list and modal editor. This update keeps the experience focused on one Todo Card and moves the richer behavior directly into the card.

New behavior includes:

- In-card edit mode
- Editable title, description, priority, and due date
- Status dropdown control
- Synchronized checkbox and status state
- Priority indicator that changes color
- Collapsible long description
- Overdue indicator
- More granular time remaining text
- Focus trap while editing

## Features

- Real checkbox for completion
- Status values: `Pending`, `In Progress`, and `Done`
- Priority values: `Low`, `Medium`, and `High`
- Priority colors:
  - `Low`: orange
  - `Medium`: blue
  - `High`: red
- Status colors:
  - `Pending`: yellow
  - `In Progress`: blue
  - `Done`: green
- Time remaining examples:
  - `Due in 2 days`
  - `Due in 3 hours`
  - `Due in 45 minutes`
  - `Overdue by 1 hour`
  - `Completed`

## Design Decisions

- The component remains a single Todo Card instead of a full app.
- Editing happens inside the card so users do not leave the task context.
- The status dropdown appears before the expand and action buttons to support the requested keyboard flow.
- Long descriptions collapse by default and can be expanded with an accessible button.
- If the task is marked `Done`, the time remaining text becomes `Completed` and the countdown no longer updates.

## Accessibility Notes

- All edit fields use visible `<label for="">` labels.
- The status dropdown has an accessible name.
- The expand button uses `aria-expanded` and `aria-controls`.
- The collapsible section has a matching `id`.
- Time remaining uses `aria-live="polite"`.
- Edit mode traps focus inside the form.
- Closing edit mode returns focus to the Edit button.
- Focus styles are visible for keyboard users.

## Testing Hooks

Previous test IDs are still present:

- `test-todo-card`
- `test-todo-title`
- `test-todo-description`
- `test-todo-priority`
- `test-todo-due-date`
- `test-todo-time-remaining`
- `test-todo-status`
- `test-todo-complete-toggle`
- `test-todo-tags`
- `test-todo-tag-work`
- `test-todo-tag-urgent`
- `test-todo-edit-button`
- `test-todo-delete-button`

New test IDs:

- `test-todo-edit-form`
- `test-todo-edit-title-input`
- `test-todo-edit-description-input`
- `test-todo-edit-priority-select`
- `test-todo-edit-due-date-input`
- `test-todo-save-button`
- `test-todo-cancel-button`
- `test-todo-status-control`
- `test-todo-priority-indicator`
- `test-todo-expand-toggle`
- `test-todo-collapsible-section`
- `test-todo-overdue-indicator`

## How To Run

Open `index.html` directly in a browser or use VS Code Live Server.

## Known Limitations

- The card stores state in memory only. Refreshing the page resets it to the default task.
- Delete resets the card to a simple empty-task state rather than removing the card from the page.
- There is no backend or task database because this is intentionally a single-card component.
