# Glassmorphism Website

A demo digital-agency website ("GlassStudio") built entirely with a **glassmorphism** design
language — frosted-glass cards, translucent nav, glowing gradients — powered by Next.js,
Framer Motion animations, and Tailwind CSS.

## What it does

A single-page-style marketing site for a fictional digital agency. It showcases services,
a stats band, team members, a company timeline, a filterable project portfolio, and a
contact section — all wrapped in glassmorphic panels with scroll-driven motion effects.

## Features

- **Glassmorphism design system** — backdrop-blur cards, translucent sticky nav, gradient
  borders and glows throughout
- **Services section** — Web Development, Mobile Apps, UI/UX Design, Digital Strategy
- **Stats band** — 150+ projects, team size, years, client counters
- **Team section** — member cards with roles
- **Company timeline** — milestones (Founded → Growth → Innovation)
- **Filterable portfolio** — projects (E-Commerce Platform, Fitness Mobile App, SaaS
  Dashboard, etc.) filtered by category
- **Contact section** — name/email/message form UI (front-end only demo) plus contact info
- **Scroll animations** — Framer Motion `useScroll`/`useTransform` parallax and reveal effects
- **Dark / light theme toggle** — via `next-themes`
- **Responsive layout** — mobile hamburger menu, adaptive grids

## Tech stack

- **Next.js 14** (App Router) + **React 18** + **TypeScript**
- **Framer Motion** (scroll animations, parallax, reveals)
- **Tailwind CSS v3** + `tailwindcss-animate`
- **Radix UI** (`@radix-ui/react-slot`) via shadcn/ui-style `components/ui`
- **next-themes** for theme switching
- **lucide-react** icons
- `@emotion/is-prop-valid` utility

## Quick start

```bash
# Install dependencies (npm or pnpm)
npm install

# Run the dev server
npm run dev

# Open http://localhost:3000
```

## Build

```bash
npm run build
npm start
```

## Project structure

```
glassmorphism-website/
├── app/
│   ├── layout.tsx          # Root layout, Inter font, metadata, ThemeProvider
│   ├── page.tsx            # Entire site: hero, services, stats, team, timeline,
│   │                       #   portfolio, contact (client component)
│   └── globals.css         # Tailwind + glassmorphism tokens
├── components/
│   ├── theme-provider.tsx   # next-themes wrapper
│   └── ui/                  # badge, button, input, textarea
├── lib/
│   └── utils.ts             # cn() class helper
├── public/                  # Images / static assets
├── next.config.mjs
├── components.json          # shadcn/ui config
└── tailwind.config.ts
```

## Environment variables

None — the site is fully client-side; the contact form is a front-end demo and submits
nowhere. Wire it to your own API or form service to make it functional.

## Deployment

The site has no API routes, server actions, or server-side data fetching, so it can be
**statically exported** and hosted anywhere static files work (GitHub Pages, Cloudflare
Pages, Netlify, Vercel).

Static export is enabled in `next.config.mjs` via `output: "export"` with
`basePath: "/glassmorphism-website"` for the GitHub Pages subpath.

Live demo: https://girishlade111.github.io/glassmorphism-website/

> Note: `basePath` is only needed for the GitHub Pages subpath. If you deploy to a root
> domain (e.g. on Vercel or Cloudflare Pages), remove the `basePath` line from
> `next.config.mjs` and rebuild.

---

Built by Girish Lade · https://ladestack.in
