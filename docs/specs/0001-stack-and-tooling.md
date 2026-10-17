# 0001. Stack and tooling

**Date**: 2026-10-17
**Status**: Proposed

## Summary

Proyek ini pakai Next.js 16 dengan React 19, TypeScript, dan Tailwind CSS v4. Tooling: ESLint 9, Prettier, Husky. Deploy ke Vercel. Testing belum ada, ditambah nanti kalau sudah perlu.

## Context

Landing page profil pondok pesantren ATH-THOOHIRIIN. Target: orang tua / calon santri. Tujuan: meyakinkan orang tua untuk mendaftarkan anak. Build approach: Skateboard. Workflow tier: Prototype.

Proyek sudah di-scaffold dengan create-next-app. Stack utama sudah ada: Next.js 16.4.2, React 19.3.0, TypeScript 5, Tailwind CSS v4. Build dan lint sudah lolos.

## Options considered

### Option 1: Next.js + React + TypeScript + Tailwind (current)

Stack yang sudah ada di proyek.

**Pros:**
- Sudah terpasang dan teruji
- Turbopack untuk build cepat
- Tailwind v4 untuk styling cepat
- TypeScript untuk type safety

**Cons:**
- Next.js 16 masih relatif baru
- Tailwind v4 masih baru

### Option 2: Next.js + React + JavaScript + Tailwind

Sama tapi tanpa TypeScript.

**Pros:**
- Lebih simpel
- Lebih sedikit boilerplate

**Cons:**
- Tidak ada type safety
- Lebih error prone

### Option 3: Astro + React + TypeScript

Astro untuk static site, React untuk komponen.

**Pros:**
- Lebih ringan untuk static site
- Island architecture

**Cons:**
- Lebih kompleks untuk setup
- Overkill untuk landing page

## Decision

**Chosen option**: Option 1: Next.js + React + TypeScript + Tailwind

Stack yang sudah ada di proyek. Next.js 16 dengan Turbopack, React 19, TypeScript 5, Tailwind CSS v4.

## Proposed stack

| Layer | Choice | Reason |
|---|---|---|
| Language | TypeScript 5 | Type safety, better IDE support |
| Framework | Next.js 16.4.2 | App Router, Turbopack, SSR/SSG |
| Styling | Tailwind CSS v4 | Utility first, fast development |
| Linting | ESLint 9 | Already configured |
| Formatting | Prettier | Auto format code |
| Git hooks | Husky | Precommit hooks for code quality |
| Testing | None (yet) | Add later when needed |
| Deployment | Vercel | Easiest for Next.js |
| Hosting | Vercel | Same as deployment |

## Rationale

Stack yang dipakai adalah stack yang sudah ada di proyek. Next.js 16 dengan Turbopack memberikan build yang cepat. React 19 adalah versi terbaru. TypeScript memberikan type safety. Tailwind CSS v4 memberikan styling yang cepat dan konsisten.

Tooling yang ditambahkan: Prettier untuk auto format, Husky untuk precommit hooks. Testing ditambah nanti kalau sudah perlu.

Deployment ke Vercel karena paling mudah untuk Next.js. Vercel adalah creator Next.js, jadi integrasinya paling mulus.

## Consequences

**Positive:**
- Build dan lint sudah lolos
- Stack modern dan teruji
- Tooling lengkap untuk development

**Negative / tradeoffs:**
- Next.js 16 masih relatif baru
- Tailwind v4 masih baru
- Prettier dan Husky perlu di setup

**Neutral:**
- Testing belum ada
- Deploy ke Vercel perlu di setup

## Follow-up

- [ ] Setup Prettier + Husky
- [ ] Setup deploy ke Vercel
- [ ] Tambah testing framework nanti kalau sudah perlu
