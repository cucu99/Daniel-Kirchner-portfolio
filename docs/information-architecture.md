# Information Architecture

## Global Framework
- **Layout shell:** Persistent header with site logo/name, navigation (Home, Projects, Blog, About, Contact) and theme toggle; footer with social links, availability status, RSS link, copyright.
- **Metadata:** Define base metadata in `src/app/layout.tsx`; per-route `generateMetadata` for titles, descriptions, OG images, and canonical URLs.
- **Design tokens:** Tailwind v4 configuration for typography scale, spacing, color palette (light/dark), and component primitives (buttons, cards).

## Route Map (App Router)
- `/` – Landing page with hero, concise bio, featured projects carousel, recent posts, testimonial strip, and contact CTA.
- `/about` – Extended biography, skills grouped by category, values, speaking/publications, resume download.
- `/projects` – Grid/list of project summaries with tag-based filters and outcome highlights.
- `/projects/[slug]` – MDX-driven case study with contextual metadata, sections for challenge, solution, impact, gallery of visuals, and call-to-action.
- `/blog` – Paginated blog index with MDX post previews, categories/tags, subscribe CTA, optional search (phase two).
- `/blog/[slug]` – MDX article layout including reading time, table of contents, code syntax highlighting, share buttons, related posts.
- `/contact` – Email/contact form (Resend or similar API), alternative contact channels (email, LinkedIn, GitHub), availability/response time note.
- `/rss.xml` – Generated RSS feed for blog posts.
- `/sitemap.xml` – Auto-generated sitemap reflective of dynamic routes.
- `/robots.txt` – Search engine crawling directives.
- `/404` – Custom not-found page with navigation back to key sections.

## Content Organization
- `src/content/projects/*.mdx` – Case studies with frontmatter: `title`, `description`, `date`, `role`, `stack`, `tags`, `image`, `links`, `featured`.
- `src/content/posts/*.mdx` – Blog posts with frontmatter: `title`, `description`, `date`, `tags`, `readingTime`, `image`, `canonical`, optional `series`.
- `src/content/snippets/` (future) – Short-form tips or code snippets.
- Shared MDX components (Callout, CodeBlock, Quote, Image) defined under `src/components/mdx/` for consistent styling.

## Component Inventory (Initial)
- Layout primitives: `Header`, `Footer`, `Container`, `ThemeToggle`
- Home sections: `Hero`, `ProjectSpotlight`, `PostTeaserList`, `TestimonialStrip`, `ContactBanner`
- Listing & cards: `ProjectCard`, `PostCard`, `Tag`, `Badge`
- Content: `MDXContent`, `TableOfContents`, `ShareBar`
- Forms: `ContactForm`, `Input`, `Textarea`, `Button`
- Utilities: `SectionHeading`, `Pagination`, `BackToTop`

## User Flows
1. **Recruiter evaluating fit** → Land on `/` → skim hero & featured projects → drill into a project case study → use contact CTA.
2. **Client vetting capability** → Navigate to `/projects` → filter by domain → read several case studies → submit inquiry via `/contact`.
3. **Developer seeking insights** → Access `/blog` → read specific post → subscribe to RSS or share article.
4. **Returning visitor** → Use sticky nav to jump directly to blog or specific project; theme toggle persists preference.

## Accessibility & Performance Considerations
- Semantic HTML structure with aria landmarks and skip-links in layout.
- High-contrast color palette, focus indicators, keyboard navigable components.
- Image optimization via `next/image` with responsive sizes; prefetch critical routes.
- Limit layout shift by reserving space for images and using font loading strategies.

## Future Extensions (Reserved Routes)
- `/uses` – Equipment and software stack
- `/speaking` – Talks and conference appearances
- `/newsletter` – Subscription landing page
- `/search` – Federated search across projects and posts

Maintaining this IA ensures the App Router structure remains scalable, content stays organized, and future features can land without refactoring the core navigation.
