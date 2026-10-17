<!-- BEGIN:nextjs-agent-rules -->

## This is NOT the Next.js you know

This version has breaking changes — APIs, conventions, and file structure may all differ from your training data. Read the relevant guide in `node_modules/next/dist/docs/` (resolved from this file's directory; in monorepos the `next` package may not be visible from the repo root) before writing any code. Heed deprecation notices.

This block is written and re-added by `next dev` — verify at `node_modules/next/dist/server/lib/generate-agent-files.js`. Removing it from a diff only re-creates the uncommitted change; committing it with your work keeps the tree clean.

<!-- END:nextjs-agent-rules -->

# ATH-THOOHIRIIN Landing Page

Landing page profil pondok pesantren ATH-THOOHIRIIN, ponpes pencetak penghafal Al-Qur'an dengan kepribadian Islam dan jiwa wirausaha. Target pengunjung: orang tua / calon santri yang ingin mendaftarkan anaknya. Tujuan: meyakinkan orang tua untuk mendaftarkan anak.

**Build approach:** Skateboard (MVP dulu, versi paling tipis yang sudah bisa dipakai, lalu berkembang).
**Workflow:** Prototype (langsung build, tanpa verifikasi tambahan).
**Bahasa komunikasi:** Bahasa Indonesia sederhana, hindari jargon tanpa penjelasan.

## Build commands

```bash
npm run dev      # development server, http://localhost:3000
npm run build    # production build
npm run start    # start production server
npm run lint     # ESLint
```

Verify: `npm run lint` dan `npm run build` harus lolos sebelum selesai.

## Tech stack

| Layer | Choice |
|---|---|
| Language | TypeScript 5 (strict mode) |
| Framework | Next.js 16.4.2 (App Router, Turbopack) |
| UI | React 19.3.0 |
| Styling | Tailwind CSS v4 |
| Linting | ESLint 9 |
| Formatting | Prettier |
| Git hooks | Husky |
| Deployment | Vercel |

## Coding conventions

- TypeScript strict mode, tidak ada `any` tanpa alasan jelas
- Tailwind CSS untuk styling, tidak pakai CSS modules atau styled-components
- Path alias `@/*` merujuk ke root project (`@/app`, `@/components`, dsb)
- Komponen React pakai function component dengan hooks
- Nama file komponen PascalCase (`HeroSection.tsx`)
- Nama file utilitas kebab-case (`format-date.ts`)

## Project structure

```
app/           # App Router (layout, page, route)
components/    # React components
public/        # Static assets (images, svg)
docs/          # Specs, scope, design docs
```

## Agent skills

Relevant skills for this project: `design-taste-frontend` (UI quality), `mengto-tailwindcss` (Tailwind conventions), `mengto-landing-page` (landing page patterns), `build-awwwards-quality-sites` (high-end frontend).

## Rules

- Next.js 16 has breaking changes. Read `node_modules/next/dist/docs/` before writing code. Heed deprecation notices.
- Always respond in Bahasa Indonesia, simple and relatable.
- Jangan commit, push, atau rewrite history tanpa persetujuan eksplisit.
- .env dan file credential tidak boleh dibaca, dicetak, atau di-commit.