# Contributing Guide

Every piece of code generated for this project must follow these rules.

---

# General Principles

Write code as if it will be maintained by a large engineering team.

Prioritize:

- Readability

- Maintainability

- Reusability

- Scalability

Avoid shortcuts.

---

# Before Writing Code

Understand:

- The feature

- Existing architecture

- Existing folder structure

- Existing types

Do not duplicate code.

---

# Components

Components should:

- Have a single responsibility

- Be reusable

- Be small

If a component exceeds approximately 250 lines, split it.

---

# Hooks

Extract business logic into hooks.

Avoid large useEffect blocks.

Prefer custom hooks.

---

# Services

Every API request belongs inside services.

Components never perform HTTP requests.

---

# State

Server State

TanStack Query

Client State

Zustand

Never mix responsibilities.

---

# Forms

Always use:

React Hook Form

Zod

---

# Types

Every request and response should have dedicated interfaces.

Never use any.

---

# Error Handling

Centralize error handling.

Never duplicate logic.

Return typed errors whenever possible.

---

# Naming

Variables

camelCase

Functions

camelCase

Components

PascalCase

Interfaces

PascalCase

Enums

PascalCase

Hooks

useSomething

---

# Functions

Keep functions small.

Avoid functions longer than approximately 50 lines.

Split responsibilities.

---

# Components

Prefer composition.

Avoid prop drilling.

Extract reusable parts.

---

# Comments

Avoid unnecessary comments.

Code should be self-explanatory.

Comment only:

- Complex algorithms

- Business rules

- Temporary workarounds

---

# Imports

Order imports consistently.

1. React

2. External libraries

3. Internal modules

4. Relative imports

---

# Performance

Avoid unnecessary re-renders.

Use memoization only when needed.

Lazy load heavy modules.

Use dynamic imports where appropriate.

---

# Accessibility

Always consider accessibility.

Buttons

Labels

Keyboard navigation

ARIA attributes

Focus management

---

# Responsiveness

Every page should work on:

Desktop

Tablet

Mobile

---

# Security

Never expose secrets.

Never hardcode API keys.

Validate user input.

Escape unsafe content.

Sanitize HTML if needed.

---

# Pull Request Checklist

Before considering a feature complete:

✓ TypeScript passes

✓ ESLint passes

✓ No duplicated code

✓ Uses existing architecture

✓ No business logic inside components

✓ No API calls inside components

✓ Types created

✓ Error handling implemented

✓ Responsive

✓ Accessible

---

# AI Assistant Rules

When generating code:

1. Respect the project architecture.

2. Never introduce new libraries unless requested.

3. Reuse existing components before creating new ones.

4. Keep code modular.

5. Prefer simplicity over cleverness.

6. Explain architectural decisions when relevant.

7. Generate production-ready code.

8. Assume this project will continue growing.

9. If a request conflicts with these guidelines, explain the conflict and propose an alternative instead of violating the architecture.

These rules are mandatory for every code generation task.
