# Frontend Architecture

## Overview

This project is the frontend of an Enterprise Generative AI Platform.

The backend is implemented using FastAPI and follows a Clean Architecture.

The frontend must maintain the same philosophy:

- Modular
- Scalable
- Maintainable
- Easy to test
- Easy to extend
- Independent features
- Clear separation of responsibilities

The frontend should be able to evolve for years without requiring architectural changes.

---

# Architectural Principles

The project follows these principles:

- Clean Architecture
- Feature-Based Architecture
- Separation of Concerns
- SOLID
- DRY
- KISS
- Composition over Inheritance

---

# High Level Architecture

Application

├── App Router

├── Features

├── Shared Components

├── Services

├── Providers

├── Stores

├── Hooks

├── Utilities

└── API Client

The UI never communicates directly with the backend.

All communication must go through the Services layer.

---

# Folder Structure

src/

    app/

    features/

    components/

    services/

    hooks/

    stores/

    providers/

    lib/

    types/

    utils/

    styles/

---

# Feature Architecture

Every feature should be isolated.

Example:

features/

    chat/

        components/

        hooks/

        services/

        types/

        utils/

    documents/

    connectors/

    users/

    evaluation/

Each feature owns its own business logic.

Avoid dependencies between features whenever possible.

---

# Shared Components

Reusable UI components belong in:

components/

Examples:

- Button

- Modal

- Dialog

- Table

- Card

- Loader

- Badge

- Avatar

Never duplicate reusable UI.

---

# Services

Every HTTP request must be implemented inside services.

Components must never perform API calls.

Bad

Component

↓

fetch()

Good

Component

↓

Hook

↓

Service

↓

API Client

↓

FastAPI

---

# Hooks

Business logic should be extracted into custom hooks.

Hooks coordinate:

- Queries
- Mutations
- Loading state
- Error state
- Pagination
- Infinite scrolling
- Streaming

Components should remain focused on rendering.

---

# State Management

There are only two types of state.

Server State

Managed exclusively with TanStack Query.

Examples:

- Chats

- Documents

- Users

- Search results

Client State

Managed with Zustand.

Examples:

- Sidebar open

- Theme

- Selected conversation

- User preferences

Do not duplicate server state inside Zustand.

---

# API Layer

Every request must go through a centralized API Client.

Responsibilities:

- Authentication

- Authorization

- Token refresh

- Interceptors

- Error handling

- Timeouts

- Base URL

---

# Types

Every DTO must have its own interface.

Avoid anonymous objects.

Requests

Responses

Enums

Models

Errors

Pagination

Streaming events

---

# Error Handling

Errors must be centralized.

Never duplicate try/catch logic.

UI components only display errors.

Business logic handles them elsewhere.

---

# Streaming

Streaming must be abstracted.

Components should never manage EventSource or WebSockets directly.

Instead:

Component

↓

Hook

↓

Streaming Service

↓

FastAPI

---

# Dependency Rules

Features must not import each other directly.

Shared code belongs in:

components/

hooks/

lib/

services/

types/

utils/

---

# Scalability

The application must support future modules without changing the architecture.

Examples:

- AI Chat

- RAG

- Document Management

- Connectors

- Evaluation

- Prompt Playground

- Admin Dashboard

- Users

- Agents

- Memory

- Analytics

The architecture should remain stable regardless of project size.
