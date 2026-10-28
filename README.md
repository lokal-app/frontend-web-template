# Frontend Web Template

A minimal React + Vite + Tailwind CSS starter template with HMR and Oxlint, meant as a clean base for people starting out with web development.

## Tech Stack

- React 19 (JavaScript / JSX, functional components)
- Vite 8 with `@vitejs/plugin-react`
- Tailwind CSS v4 via `@tailwindcss/vite`
- Oxlint for linting
- `@/` import alias for `src/` (configured in `vite.config.js` and `jsconfig.json`)

## Getting Started

Scaffold a new project from this template using [degit](https://github.com/Rich-Harris/degit):

```sh
npx degit lokal-app/frontend-web-template my-web-app
cd my-web-app
npm install
npm run dev
```

To work on the template itself, clone it and run `npm install` instead.

This template ships with a `CLAUDE.md` defining the project's engineering guidelines (project structure, naming conventions, dependency policy, etc.). If you're using Claude Code, read and follow those rules when building on top of this template.

## Scripts

| Command           | What it does                              |
| ----------------- | ----------------------------------------- |
| `npm run dev`     | Start the Vite dev server with HMR        |
| `npm run build`   | Build for production into `dist/`         |
| `npm run preview` | Serve the production build locally        |
| `npm run lint`    | Lint the project with Oxlint              |

There is no test suite yet. CI (`.github/workflows/ci.yml`) runs `lint` and `build` on pushes and pull requests to `master`.

## Environment Variables

None are required. If you add any, prefix them with `VITE_` so Vite exposes them to the client, document them in `.env.example`, and keep your real values in an untracked `.env` file.

## React Compiler

The React Compiler is not enabled on this template because of its impact on dev & build performances. To add it, see [this documentation](https://react.dev/learn/react-compiler/installation).

## Expanding the Oxlint configuration

If you are developing a production application, we recommend using TypeScript with type-aware lint rules enabled. Check out the [TS template](https://github.com/vitejs/vite/tree/main/packages/create-vite/template-react-ts) for information on how to integrate TypeScript and Oxlint's TypeScript related rules in your project.
