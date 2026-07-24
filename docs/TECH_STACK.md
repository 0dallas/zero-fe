# Technology Stack

This project uses the following technologies.

Only these technologies should be used unless explicitly approved.

---

# Framework

Next.js (App Router)

---

# UI Library

React

---

# Language

TypeScript

JavaScript is not allowed.

Everything must be fully typed.

Avoid using any.

---

# Styling

Tailwind CSS

---

# UI Components

shadcn/ui

Build custom components using shadcn primitives.

Do not install additional UI frameworks.

---

# Icons

lucide-react

---

# HTTP Client

Axios

Create one reusable API Client.

Never duplicate configuration.

---

# Server State

TanStack Query

Responsibilities:

- Fetching

- Caching

- Pagination

- Mutations

- Synchronization

---

# Global State

Zustand

Use only for:

- UI state

- Theme

- Preferences

- Selected entities

Never store API data in Zustand.

---

# Forms

React Hook Form

---

# Validation

Zod

Every form should use Zod schemas.

---

# Date Handling

date-fns

---

# Utility Libraries

clsx

tailwind-merge

---

# Authentication

JWT

Authentication must be implemented through the centralized API Client.

Never manually attach tokens inside components.

---

# Environment Variables

Only expose variables prefixed according to Next.js conventions.

Never hardcode URLs.

---

# API Communication

REST

Streaming

Server-Sent Events (SSE)

WebSockets (future support)

---

# Folder Naming

Folders

lowercase

Files

PascalCase for components

camelCase for hooks and utilities

---

# Component Naming

Button.tsx

ChatMessage.tsx

ConversationList.tsx

DocumentCard.tsx

---

# Hook Naming

useChat.ts

useDocuments.ts

useStreaming.ts

---

# Service Naming

chat.service.ts

document.service.ts

user.service.ts

---

# Types Naming

Chat.ts

Document.ts

User.ts

Api.ts

---

# Imports

Prefer absolute imports.

Avoid deep relative paths.

Good

@/components

@/features

@/services

Bad

../../../../components

---

# Code Formatting

Prettier

ESLint

Strict TypeScript

No warnings.

No unused imports.

No unused variables.

---

# Testing (Future)

Vitest

React Testing Library

Playwright

Unit tests

Integration tests

End-to-end tests

---

# Forbidden Technologies

JavaScript

Redux

MobX

Bootstrap

Material UI

jQuery

Moment.js

CSS Modules

Styled Components

