# Product Brief

## Mission
Launch a personal portfolio and blog that positions me as a versatile full-stack engineer. The experience should reinforce credibility through storytelling, highlight tangible results, and provide a clear path for contact or collaboration.

## Target Audience
- Hiring managers evaluating candidates for senior/full-stack roles
- Potential freelance/consulting clients vetting capabilities
- Fellow developers and peers interested in technical insights

These personas are often busy, so the site must surface key takeaways quickly while offering deeper dives when time allows.

## Value Proposition
- Authentic narratives around real projects, structured by problem → solution → impact
- Demonstrated technical depth through detailed case studies and long-form blog posts
- Thoughtful design system and performance-first implementation that reflects my standards for shipping production software

## Voice & Tone
Confident, approachable, and transparent. Stories should be honest about trade-offs and lessons learned while maintaining technical rigor and clarity.

## Core Pages & Experiences
- **Home:** Hero with elevator pitch, featured projects, recent blog posts, testimonials, primary contact CTA
- **About:** Long-form bio, skills matrix, timeline, work philosophy, resume download
- **Projects:** Filterable index of case studies with outcomes and tech stack
- **Project Detail (`/projects/[slug]`):** MDX case studies covering context, approach, results, visuals
- **Blog:** Index with latest posts, categories/tags, subscribe CTA
- **Blog Post (`/blog/[slug]`):** MDX article layout with TOC, reading time, code highlighting, related posts
- **Contact:** Email form or direct link, social handles, availability indicator
- **Utility:** RSS feed, sitemap, robots, custom 404

## Differentiators
- Structured storytelling template for projects (problem, constraints, solution, impact)
- Tailwind-driven design system with dark/light toggle to showcase frontend polish
- Lightweight MDX authoring workflow for fast publishing and version control within the repo

## Success Metrics
- ≥3 qualified inbound opportunities per month (recruiter outreach or client inquiries)
- Average session duration ≥ 2:30 minutes
- Hero CTA click-through rate ≥ 20%
- Newsletter sign-ups (if implemented) trending upward month-over-month
- Lighthouse performance, accessibility, best practices, SEO scores ≥ 90

## Constraints & Assumptions
- Content stored as MDX within the repository (no external CMS initially)
- Deployment on Vercel with automatic previews
- Four-week part-time timeline: Week 1 planning, Weeks 2–3 build + content production, Week 4 polish and QA
- Limited visual assets; plan to curate or generate imagery early to maintain consistency

## Risks & Mitigations
- **Content backlog:** Schedule writing milestones alongside development
- **Scope creep:** Lock MVP routes/components; defer extras to roadmap
- **Accessibility debt:** Include accessibility checks (axe, keyboard testing) in each milestone
- **Inconsistent visuals:** Establish color/typography tokens and asset guidelines before high-fidelity build

## Dependencies & Tooling
- Next.js 15 with App Router, Tailwind CSS v4, MDX integration, TypeScript
- Optional integrations: analytics (Plausible or Vercel Analytics), email API for contact form (Resend), Open Graph image generation
- Version control via GitHub with PR workflow; future CI/CD for lint/build on push

## Roadmap Overview
1. Planning artifacts (brief, IA, component inventory)
2. Foundation setup: Tailwind tokens, layout shell, navigation/footer
3. Core sections on the home page with placeholder content
4. MDX content pipeline for projects/posts with static generation
5. Detailed case study and blog templates, including metadata
6. Contact form integration and analytics wiring
7. Polish: responsiveness, accessibility, performance audits, SEO enhancements
