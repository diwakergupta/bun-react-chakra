# Bun + React + Chakra UI Starter

A lightweight starter kit for building modern single-page applications with
[Bun](https://bun.sh/) for tooling, [React](https://react.dev/) for UI logic, and
[Chakra UI](https://chakra-ui.com/) for accessible, themeable components. This
template is configured to let you ship quickly with sensible defaults and a
clear project structure.

## Features

- ⚡️ **Bun-first toolchain** – fast installs, bundling, and dev server via Bun.
- ⚛️ **React with TypeScript** – strong typing and JSX out of the box.
- 🎨 **Chakra UI** – ready-to-use component library with dark mode support.
- 📦 **Zero-config setup** – scripts for local development and production
  builds already wired up.

## Getting Started

### Prerequisites

- [Bun](https://bun.sh/docs/installation) `v1.0.0` or later installed locally.

### Installation

Install project dependencies with Bun:

```bash
bun install
```

### Available Scripts

Run these commands from the project root:

| Command       | Description |
| ------------- | ----------- |
| `bun dev`     | Starts the development server with hot module reloading. |
| `bun start`   | Serves the production build. |
| `bun test`    | Executes unit tests (configure in `bunfig.toml` / `src`). |

> ℹ️ Bun automatically loads variables from `.env` files. No extra dotenv setup
> is required.

### Project Structure

```
.
├── src/
│   ├── App.tsx           # Root React component composed with Chakra UI
│   ├── components/       # Shared UI utilities (provider, color mode, etc.)
│   ├── frontend.tsx      # React entry file imported by index.html
│   ├── index.css         # Global styles
│   ├── index.html        # HTML shell bundled by Bun
│   └── index.tsx         # Bun server that serves the SPA
├── bunfig.toml           # Bun configuration
├── package.json          # Scripts and dependency manifest
├── tsconfig.json         # TypeScript compiler options
└── README.md
```

## Chakra UI Tips

- Adjust theming by updating `src/components/ui/provider.tsx` to pass a custom
  theme or system into `ChakraProvider`.
- Use the [Chakra UI docs](https://chakra-ui.com/docs) for component examples,
  recipes, and accessibility guidelines.

## Deployment

Create an optimized production bundle and serve it:

```bash
bun run build
bun start
```

The `bun run build` script should output static assets ready for static hosting
providers. Adjust your deployment pipeline to copy the generated files from the
`./dist` directory.

## Contributing

1. Fork the repository and create a feature branch.
2. Install dependencies with `bun install`.
3. Run `bun test` (and any other project-specific checks) before opening a PR.
4. Submit your pull request with a clear summary of the changes.

## License

This project is open source and available under the MIT License. Feel free to
use and adapt it for your own projects.
