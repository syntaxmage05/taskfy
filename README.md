# Taskfy

Taskfy is a full-stack task management application built with **Ruby on Rails 8** and **React**. It provides a JSON API for core resources (tasks, users, sessions, comments) and serves a SPA-style frontend shell from Rails.

## Contents
- [Overview](#overview)
- [Architecture](#architecture)
- [Tech Stack](#tech-stack)
- [API](#api)
- [Repository Layout](#repository-layout)
- [Local Development](#local-development)
- [Testing & Code Quality](#testing--code-quality)
- [Deployment](#deployment)
- [Troubleshooting](#troubleshooting)

## Overview

Taskfy is designed for a Rails-first backend workflow with a modern frontend toolchain.

- Rails handles domain logic, persistence, and JSON responses.
- React handles interactive UI components in the frontend shell.
- Vite/esbuild provide fast frontend development and bundling.
- SQLite keeps local setup lightweight.

## Architecture

- **Backend framework:** Rails 8 (`config.load_defaults 8.0`)
- **API rendering:** Jbuilder templates under `app/views/**/.json.jbuilder`
- **Auth/session flow:** session resource (`POST /session`, `DELETE /session`)
- **Authorization:** Pundit policy layer (e.g., `app/policies/task_policy.rb`)
- **Frontend entrypoint:** `app/javascript/src/App.jsx` served through Rails routing fallback

## Tech Stack

### Backend
- Ruby on Rails `~> 8.0.4`
- SQLite3
- Pundit
- Jbuilder
- Solid Queue / Solid Cache / Solid Cable

### Frontend
- React 18
- Vite
- esbuild
- Sass
- Tailwind CSS

### Tooling
- RuboCop
- ESLint + Prettier
- Brakeman
- Husky + lint-staged

## API

JSON routes are defined with a `format: :json` constraint in `config/routes.rb`.

| Method | Path | Purpose |
|---|---|---|
| GET | `/tasks` | List tasks |
| POST | `/tasks` | Create task |
| GET | `/tasks/:slug` | Get task by slug |
| PATCH / PUT | `/tasks/:slug` | Update task |
| DELETE | `/tasks/:slug` | Delete task |
| GET | `/users` | List users |
| POST | `/users` | Create user |
| POST | `/session` | Sign in / create session |
| DELETE | `/session` | Sign out / destroy session |
| POST | `/comments` | Create comment |

## Repository Layout

```text
taskfy/
├── app/
│   ├── controllers/       # Request handling and API actions
│   ├── javascript/        # React source, entrypoints, stylesheets
│   ├── models/            # ActiveRecord models
│   ├── policies/          # Pundit authorization policies
│   └── views/             # ERB and Jbuilder templates
├── config/                # Rails config, routes, env settings
├── db/                    # Schema and migration/data files
├── bin/                   # Dev and maintenance scripts
├── Procfile.dev           # Foreman process definitions
├── Gemfile                # Ruby gems
└── package.json           # JavaScript dependencies/scripts
```

## Local Development

### Prerequisites

Install:
- Ruby (version compatible with `.ruby-version`)
- Bundler
- Node.js + Yarn
- SQLite3

### Setup

```bash
git clone <repo-url>
cd taskfy
bundle install
yarn install
bin/rails db:prepare
```

Alternative bootstrap flow:

```bash
bin/setup
```

### Run

```bash
bin/dev
```

`bin/dev` uses `Procfile.dev` and starts:
- Rails server
- JS build watcher
- Vite dev server

Default URL: `http://localhost:3000`

## Testing & Code Quality

### Tests

```bash
bin/rails test
```

### Ruby linting

```bash
bin/rubocop
```

### Security scan

```bash
bin/brakeman
```

### JavaScript lint/format (examples)

```bash
yarn eslint app/javascript --ext .js,.jsx
yarn prettier --check "app/javascript/**/*.{js,jsx}"
```

## Deployment

The repository includes Docker and Kamal configuration.

Build a local image:

```bash
docker build -t taskfy:latest .
```

Before deploying, review:
- `config/deploy.yml`
- `.kamal/secrets`

## Troubleshooting

- **Port conflict:** `PORT=3001 bin/dev`
- **Dependency mismatch:** rerun `bundle install` and `yarn install`
- **Database reset:** `bin/rails db:drop db:create db:migrate`
