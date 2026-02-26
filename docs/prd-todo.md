# Product Requirements Document (PRD) - Todo App Upgrade (Due Dates, Priority, and Filters)

## 1. Overview

Upgrade the current basic Todo app (title + completed) to a simple, teachable MVP that improves task planning and visibility without adding backend complexity. The MVP introduces optional due dates, priority levels, and date-based filters so users can quickly identify what needs attention. Scope is intentionally constrained to local-only storage and core workflow improvements.

---

## 2. MVP Scope

- Add `dueDate` to tasks as an optional field using ISO format `YYYY-MM-DD`.
- Add `priority` to tasks with enum values `P1 | P2 | P3`.
- Default `priority` to `P3` when not provided.
- Add filters/tabs: **All**, **Today**, **Overdue**.
- Filter behavior:
  - **All** includes completed and incomplete tasks.
  - **Today** and **Overdue** include only incomplete tasks.
- Keep storage local only (no backend changes, no external storage).
- Data model validation:
  - `title` is required.
  - `priority` must be one of `P1 | P2 | P3` (default `P3`).
  - `dueDate` is optional and must be valid ISO `YYYY-MM-DD`; invalid values are ignored (treated as absent).

---

## 3. Post-MVP Scope

- Visually highlight overdue tasks.
- Add task sorting rules:
  - overdue first
  - then by priority (`P1` → `P3`)
  - then by due date ascending
  - tasks without due dates last

---

## 4. Out of Scope

- Notifications
- Recurring tasks
- Multi-user support
- Keyboard navigation enhancements
- External storage / backend persistence
