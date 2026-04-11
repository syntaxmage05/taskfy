<div id="top">

<!-- HEADER STYLE: CLASSIC -->
<div align="center">


# TASKFY

<em>Transforming Tasks Into Seamless Success</em>

<!-- BADGES -->
<img src="https://img.shields.io/github/last-commit/syntaxmage05/taskfy?style=flat&logo=git&logoColor=white&color=0080ff" alt="last-commit">
<img src="https://img.shields.io/github/languages/top/syntaxmage05/taskfy?style=flat&color=0080ff" alt="repo-top-language">
<img src="https://img.shields.io/github/languages/count/syntaxmage05/taskfy?style=flat&color=0080ff" alt="repo-language-count">

<em>Built with the tools and technologies:</em>

<img src="https://img.shields.io/badge/JSON-000000.svg?style=flat&logo=JSON&logoColor=white" alt="JSON">
<img src="https://img.shields.io/badge/Markdown-000000.svg?style=flat&logo=Markdown&logoColor=white" alt="Markdown">
<img src="https://img.shields.io/badge/npm-CB3837.svg?style=flat&logo=npm&logoColor=white" alt="npm">
<img src="https://img.shields.io/badge/Ruby-CC342D.svg?style=flat&logo=Ruby&logoColor=white" alt="Ruby">
<img src="https://img.shields.io/badge/PostCSS-DD3A0A.svg?style=flat&logo=PostCSS&logoColor=white" alt="PostCSS">
<img src="https://img.shields.io/badge/Prettier-F7B93E.svg?style=flat&logo=Prettier&logoColor=black" alt="Prettier">
<img src="https://img.shields.io/badge/esbuild-FFCF00.svg?style=flat&logo=esbuild&logoColor=black" alt="esbuild">
<img src="https://img.shields.io/badge/JavaScript-F7DF1E.svg?style=flat&logo=JavaScript&logoColor=black" alt="JavaScript">
<img src="https://img.shields.io/badge/i18next-26A69A.svg?style=flat&logo=i18next&logoColor=white" alt="i18next">
<br>
<img src="https://img.shields.io/badge/React-61DAFB.svg?style=flat&logo=React&logoColor=black" alt="React">
<img src="https://img.shields.io/badge/Yarn-2C8EBB.svg?style=flat&logo=Yarn&logoColor=white" alt="Yarn">
<img src="https://img.shields.io/badge/Docker-2496ED.svg?style=flat&logo=Docker&logoColor=white" alt="Docker">
<img src="https://img.shields.io/badge/GitHub%20Actions-2088FF.svg?style=flat&logo=GitHub-Actions&logoColor=white" alt="GitHub%20Actions">
<img src="https://img.shields.io/badge/Vite-646CFF.svg?style=flat&logo=Vite&logoColor=white" alt="Vite">
<img src="https://img.shields.io/badge/ESLint-4B32C3.svg?style=flat&logo=ESLint&logoColor=white" alt="ESLint">
<img src="https://img.shields.io/badge/Axios-5A29E4.svg?style=flat&logo=Axios&logoColor=white" alt="Axios">
<img src="https://img.shields.io/badge/Sass-CC6699.svg?style=flat&logo=Sass&logoColor=white" alt="Sass">
<img src="https://img.shields.io/badge/Buffer-231F20.svg?style=flat&logo=Buffer&logoColor=white" alt="Buffer">

</div>
<br>

---

## Table of Contents

- [Overview](#overview)
- [Getting Started](#getting-started)
    - [Prerequisites](#prerequisites)
    - [Installation](#installation)
    - [Usage](#usage)
    - [Testing](#testing)
- [Features](#features)
- [Project Structure](#project-structure)

---

## Overview

Taskfy is a powerful developer toolkit designed to streamline the development, deployment, and maintenance of modern Rails applications integrated with React. It combines robust dependency management, frontend asset optimization, and containerized workflows to enhance productivity and scalability.

**Why Taskfy?**

This project simplifies complex workflows by providing:

- 🧩 **Dependency & Environment Management:** Ensures a consistent, scalable Rails setup with Gemfile, credentials, and environment configs.
- 🚀 **Frontend Asset Optimization:** Uses esbuild, Tailwind CSS, and Vite for fast, modern frontend builds.
- 🐳 **Containerized Deployment:** Dockerfile and Procfile.dev facilitate reliable, repeatable environments.
- 🎯 **Testing & Quality Assurance:** Factory setups, parallel test execution, and system tests improve code reliability.
- 🔒 **Secure & Maintainable:** Encrypted credentials, security policies, and clear separation of concerns support long-term stability.

---

## Features

|      | Component            | Details                                                                                     |
| :--- | :------------------- | :------------------------------------------------------------------------------------------ |
| ⚙️  | **Architecture**     | <ul><li>Ruby on Rails backend with React on the frontend</li><li>Ruby API and React on the frontend structure</li></ul> |
| 🔩 | **Code Quality**     | <ul><li>Uses RuboCop for linting</li><li>Consistent code style with Prettier & ESLint for frontend</li><li>Includes Rake tasks for automation</li></ul> |
| 📄 | **Documentation**    | <ul><li>Dockerfile for containerization</li><li>README.md with project overview</li><li>Config files (.yml, .json) for setup</li></ul> |
| 🔌 | **Integrations**      | <ul><li>GitHub Actions for CI/CD pipeline</li><li>Docker for containerization</li><li>Bundler, npm, yarn for dependency management</li></ul> |
| 🧩 | **Modularity**        | <ul><li>Frontend components built with React, modularized via Vite</li><li>CSS handled with TailwindCSS, utility-first approach</li><li>Backend separated into controllers, models, services</li></ul> |
| 🧪 | **Testing**           | <ul><li>RSpec for backend tests</li><li>Jest and React Testing Library for frontend</li><li>CI pipeline runs tests on push</li></ul> |
| ⚡️  | **Performance**       | <ul><li>Vite used for fast frontend builds</li><li>Asset optimization with esbuild and TailwindCSS</li><li>Caching strategies via Rails cache.yml</li></ul> |
| 🛡️ | **Security**          | <ul><li>Encrypted credentials via credentials.yml.enc</li><li>Secure environment variables in CI/CD</li><li>Dependabot for dependency updates</li></ul> |
| 📦 | **Dependencies**      | <ul><li>Backend: Ruby gems managed via Gemfile & Gemfile.lock</li><li>Frontend: npm/yarn with package.json & yarn.lock</li><li>CI/CD: docker, github_actions, rake</li></ul> |

---

## Project Structure

```sh
└── taskfy/
    ├── .github
    │   ├── dependabot.yml
    │   └── workflows
    ├── Dockerfile
    ├── Gemfile
    ├── Gemfile.lock
    ├── Procfile.dev
    ├── README.md
    ├── Rakefile
    ├── app
    │   ├── assets
    │   ├── controllers
    │   ├── helpers
    │   ├── javascript
    │   ├── jobs
    │   ├── mailers
    │   ├── models
    │   ├── policies
    │   └── views
    ├── config
    │   ├── application.rb
    │   ├── boot.rb
    │   ├── build
    │   ├── cable.yml
    │   ├── cache.yml
    │   ├── credentials.yml.enc
    │   ├── database.yml.ci
    │   ├── deploy.yml
    │   ├── environment.rb
    │   ├── environments
    │   ├── initializers
    │   ├── locales
    │   ├── puma.rb
    │   ├── queue.yml
    │   ├── recurring.yml
    │   ├── routes.rb
    │   └── storage.yml
    ├── config.ru
    ├── db
    │   ├── cable_schema.rb
    │   ├── cache_schema.rb
    │   ├── data
    │   ├── data_schema.rb
    │   ├── migrate
    │   ├── queue_schema.rb
    │   ├── schema.rb
    │   └── seeds.rb
    ├── esbuild.config.js
    ├── lib
    │   └── tasks
    ├── package.json
    ├── postcss.config.js
    ├── script
    │   └── .keep
    ├── tailwind.config.js
    ├── test
    │   ├── application_system_test_case.rb
    │   ├── controllers
    │   ├── factories
    │   ├── helpers
    │   ├── integration
    │   ├── mailers
    │   ├── models
    │   ├── support
    │   ├── system
    │   └── test_helper.rb
    ├── vite.config.js
    ├── vite.config.mts
    └── yarn.lock
```

---

## Getting Started

### Prerequisites

This project requires the following dependencies:

- **Programming Language:** Ruby
- **Package Manager:** Bundler, Rake, Npm, Yarn
- **Container Runtime:** Docker

### Installation

Build taskfy from the source and install dependencies:

1. **Clone the repository:**

    ```sh
    ❯ git clone https://github.com/syntaxmage05/taskfy
    ```

2. **Navigate to the project directory:**

    ```sh
    ❯ cd taskfy
    ```

3. **Install the dependencies:**

**Using [docker](https://www.docker.com/):**

```sh
❯ docker build -t syntaxmage05/taskfy .
```
**Using [bundler](https://www.ruby-lang.org/):**

```sh
❯ bundle install
```
**Using [npm](https://www.npmjs.com/):**

```sh
❯ npm install
```
**Using [yarn](https://yarnpkg.com/):**

```sh
❯ yarn install
```

### Usage

Run the project with:

**Using [docker](https://www.docker.com/):**

```sh
docker run -it {image_name}
```
**Using [bundler](https://www.ruby-lang.org/):**

```sh
bundle exec ruby {entrypoint}
```
**Using [npm](https://www.npmjs.com/):**

```sh
npm start
```
**Using [yarn](https://yarnpkg.com/):**

```sh
yarn start
```

### Testing

Taskfy uses the {ruby__test_framework} test framework. Run the test suite with:

```sh
rails test
```
**Using [npm](https://www.npmjs.com/):**

```sh
npm test
```
**Using [yarn](https://yarnpkg.com/):**

```sh
yarn test
```

---

<div align="left"><a href="#top">⬆ Return</a></div>

---
