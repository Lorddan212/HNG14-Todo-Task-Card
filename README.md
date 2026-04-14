# Todo Task Card

A clean, modern Todo / Task Card built with plain HTML, CSS, and JavaScript.

## Features

- Responsive todo card layout
- Required `data-testid` hooks for automated checks
- Priority badges:
  - `High` in red
  - `Medium` in blue
  - `Low` in orange
- Status badges:
  - `Pending` in yellow
  - `In Progress` in blue
  - `Done` in green
- Live time-remaining update
- Real task actions:
  - Add task
  - Edit task
  - Delete task
- Modal task editor
- Local task persistence with `localStorage`

## Project Files

- `index.html` - Main app UI, styling, and behavior
- `READ.md` - Project overview and usage notes

## How To Run

1. Open `index.html` in your browser or with VS Code Live Server.
2. Use the task card buttons to add, edit, or delete tasks.
3. Select tasks from the task list to load them into the main card.

## Accessibility Notes

- Uses semantic elements like `article`, `section`, `time`, `button`, and a real checkbox input
- Visible focus styles are included
- Action buttons have accessible names
- Time remaining uses `aria-live="polite"`

## Testing Hooks

The main task card includes the required test IDs:

- `test-todo-card`
- `test-todo-title`
- `test-todo-description`
- `test-todo-priority`
- `test-todo-due-date`
- `test-todo-time-remaining`
- `test-todo-status`
- `test-todo-complete-toggle`
- `test-todo-tags`
- `test-todo-edit-button`
- `test-todo-delete-button`

Optional tag hooks:

- `test-todo-tag-work`
- `test-todo-tag-urgent`

## Notes

- Tasks are saved in the browser with `localStorage`
- Clearing browser storage will remove saved tasks
