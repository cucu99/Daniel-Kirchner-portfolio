# Repository Guidelines

## Project Structure & Module Organization
This Next.js 15 project keeps all runtime code under `src/app`, using the App Router. Shared layout and metadata belong in `src/app/layout.tsx`, while page-level UI lives beside it in `page.tsx` or nested routes. Global styles and Tailwind 4 tokens load via `src/app/globals.css`. Static assets sit in `public/` and are served with `next/image`. Configuration files (`next.config.ts`, `tsconfig.json`, `eslint.config.mjs`) live at the root; update them in sync when introducing new tooling.

## Build, Test, and Development Commands
Run `npm install` once to hydrate dependencies. Use `npm run dev` for the Turbopack-powered local server with hot reload. Ship-ready bundles come from `npm run build`, and `npm run start` previews the compiled output. Maintain code health with `npm run lint`, which applies the Next.js core-web-vitals ESLint preset.

## Coding Style & Naming Conventions
Write TypeScript modules with default exports for route handlers and components. Favor React function components, two-space indentation, and arrow helpers for utilities. Compose UI through JSX and Tailwind utility classes; colocate component-specific styles via CSS-in-JS only when Tailwind is insufficient. Name files using lowercase kebab or nested folders to mirror route segments (e.g., `src/app/contact/page.tsx`). Keep shared helpers under future `src/lib/` or `src/components/` folders.

## Testing Guidelines
Automated tests are not yet wired up. Before adding features of substance, introduce tests with Jest or Vitest plus React Testing Library, and place them in `__tests__` directories mirroring the source. Name specs after the component under test (`page.spec.tsx`). Always run `npm run lint` alongside tests and aim for meaningful coverage of rendering and routing logic.

## Commit & Pull Request Guidelines
The existing history uses a concise, sentence-case message (“Initial commit from Create Next App”). Follow that style: a short imperative subject under 72 characters, optionally prefixed with a scope (`feat: hero section`). Open pull requests with a summary of intent, a checklist of validation (dev server, lint, tests), and screenshots for visual changes. Link relevant issues and call out migrations or config updates explicitly to ease review.

## Environment & Configuration
Copy environment secrets into `.env.local`; Turbopack reloads when variables change. Document any new keys in README updates and avoid committing `.env` files.
