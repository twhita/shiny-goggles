# Product Requirements Document (PRD) - Todo App Upgrade (Due Dates, Priority, and Filters)

## 1. Overview

Upgrade the current basic Todo app (currently title + completed) into a simple, teachable MVP that improves day-to-day task planning without adding backend complexity. The MVP adds optional due dates, priority levels, and date-based filters, while keeping all persistence local. Scope reflects the requirements meeting and the follow-up Slack scope lock.

---

## 2. MVP Scope

- Add `dueDate` to each task as an optional field using ISO format `YYYY-MM-DD`.
- Add `priority` to each task using enum values `P1 | P2 | P3`.
- Default `priority` to `P3` when a value is not provided.
- Add filters/tabs: **All**, **Today**, **Overdue**.
- Filter behavior:
  - **All** shows both complete and incomplete tasks.
  - **Today** and **Overdue** show incomplete tasks only.
- Keep storage local only (no backend changes and no external storage).
- Apply MVP data validation rules:
  - `title` is required.
  - `priority` must be one of `P1 | P2 | P3` (default `P3`).
  - `dueDate` is optional and must be valid ISO `YYYY-MM-DD`; invalid values are ignored and treated as absent.

---

## 3. Post-MVP Scope

- Visually highlight overdue tasks.
- Add sorting order for task lists:
  - overdue tasks first
  - then priority (`P1` → `P3`)
  - then due date ascending
  - then undated tasks last

---

## 4. Out of Scope

- Notifications
- Recurring tasks
- Multi-user support
- Keyboard navigation enhancements
- External storage / backend persistence
