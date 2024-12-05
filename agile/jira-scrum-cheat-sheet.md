# Jira/Scrum Beginners Cheat Sheet

## Description

This is my personal notes learning Jira through this video [Ultimate Jira Tutorial for Beginners (2024)](https://www.youtube.com/watch?v=8jWKwiIcWPI).

I also went ahead and asked ChatGPT to solidify my understand which you can find the chat here: [Jira/Scrum Clarification](https://chatgpt.com/share/67517eb5-5f1c-8001-9ba2-c799a1e683fc).

## Contents

- [Concepts](#concepts)
  - [Roadmap](#roadmap)
  - [Backlog](#backlog)
  - [Issue](#issue)
  - [Epic](#epic)
  - [Story](#story)
  - [Story Points](#story-points)
  - [Task](#task)
  - [Sprint](#sprint)
  - [Timeline View](#timeline-view)
  - [Board View](#board-view)
  - [Project Pages](#project-pages)
  - [Retrospective](#retrospective)
  - [Keys](#keys)
  - [Workflow](#workflow)
  - [Dashboards](#dashboards)
- [FAQs](#faqs)
  - [What's "is blocked by"?](#whats-is-blocked-by)
  - [What's Confluence?](#whats-confluence)
  - [Can tasks be broken into stories?](#can-tasks-be-broken-into-stories)
  - [Do keys change?](#do-keys-change)

## Concepts

### Roadmap

- Outlines high-level project goals.
- Focuses on what to achieve with the project.
- Contains the **Product Backlog**.

### Backlog

- A prioritized list of work items (**issues**) to complete.
- Includes epics, stories, tasks, and bugs.
- Organized by importance, with the most critical issues at the top.
- Divided into:
  - **Product Backlog**: All work items for the project.
  - **Sprint Backlog**: Work items selected for a specific sprint.

### Issue

- A generic term for any work item in Jira.
- Types of issues:
  - **Epic**: A large feature or goal broken into stories.
  - **Story**: A user-facing functionality broken into tasks.
  - **Task**: The smallest unit of work, often assigned to one person.
  - **Bug**: A defect or issue in the system.

### Epic

- Represents a large body of work spanning multiple sprints.
- Broken down into **stories** for better manageability.
- Created and managed by the **Product Owner**.

### Story

- Simply put, it's a user-centric functionality.
- Broken into **tasks** for implementation.
- Effort to complete is measured in **story points**.

### Story Points

- A relative measure of effort, complexity, and uncertainty.
- Tied to **stories**, not tasks.

### Task

- A granular, actionable step to achieve part of a story or a standalone work item.
- Typically assigned to one team member.
- Cannot be broken into smaller items in Jira.

### Sprint

- A fixed time frame (1 month or less) for completing selected backlog items.
- **Goal:** Deliver a potentially shippable product increment.
- Ends with a **sprint review** and **retrospective**.

### Timeline View

- Visualizes issue dependencies and schedules.
- **Dependencies**: Show relationships between issues (e.g., "Issue A is blocked by Issue B").
  - Example: "Frontend A depends on Backend B being ready."

### Board View

- Visual representation of issues based on workflow status (e.g., To Do, In Progress, Done).
- Used during sprints to track progress.

### Project Pages

- Collaborative documents for the team (e.g., sprint retrospectives, meeting notes).
- Example: **Confluence** pages for shared documentation and collaboration.

### Retrospective

- A page or meeting to reflect on a sprint:
  - What went well?
  - What went wrong?
  - How can the process improve?

### Keys

- Unique identifiers for issues in a project.
- Format: `[ProjectKey]-[IssueNumber]` (e.g., `PROJ-1`).
- Remains consistent unless the project key changes.

### Workflow

- Defines the lifecycle of an issue through different statuses.
- Example: `To Do` -> `In Progress` -> `Code Review` -> `Done`.

### Dashboards

- Visual summaries of project metrics and progress.
- Example: Shows sprint progress, burndown charts, or a list of open issues.

## FAQs

### What's "is blocked by"?

- It indicates that one issue cannot proceed until another is completed.
- Example: Feature A *is blocked by* Backend B.

### What's Confluence?

- A team collaboration tool for creating and sharing pages like documentation, meeting notes, or retrospectives.

### Can tasks be broken into stories?

- No. Tasks are the smallest unit of work and always belong to a story or an epic.

### Do keys change?

- Keys are unique and consistent within a project. They only change if the project key is updated.
