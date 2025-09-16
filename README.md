# Personal Portfolio & Blog

A Next.js 15 project for my personal portfolio and blog. The goal is to showcase full-stack case studies, publish long-form writing, and provide clear contact paths for recruiters, clients, and peers.

## Project Overview
- **Mission:** Highlight technical depth and storytelling through featured projects and MDX-powered articles.
- **Audience:** Hiring managers, potential clients, and fellow developers who need quick evidence of impact with the option to dig deeper.
- **Status:** Planning artifacts complete; building the foundational layout and content pipeline is next.

## Planning Docs
- [Product Brief](docs/product-brief.md)
- [Information Architecture](docs/information-architecture.md)

These documents will evolve as the project grows; keep them in sync with implementation decisions.

## Tech Stack
- Next.js 15 App Router & TypeScript
- Tailwind CSS v4 tokens
- MDX for project case studies and blog posts
- Deployed on Vercel (planned)

## Local Development
Install dependencies once, then use the dev server:

```bash
npm install
npm run dev
```

Run linting as part of every change:

```bash
npm run lint
```

## Project Structure
- `src/app` – App Router routes, shared layout, and UI components
- `docs/` – Planning artifacts (brief, IA, future component inventory)
- `public/` – Static assets served via `next/image`

## Next Steps
1. Finalize visual direction (color palette, typography, imagery references).
2. Scaffold global layout, navigation, and Tailwind token configuration.
3. Implement content pipeline for MDX projects and posts.
4. Populate initial case studies and blog entries.

Track progress in README and docs to keep collaborators aligned.
