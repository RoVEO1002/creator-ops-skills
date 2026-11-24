---
name: web-project-kickoff
description: Start a website or web app (fashion site, portfolio, festival site, small app) with a fixed sequence — brief, wireframe, design system, stack setup, build, mobile QA. Use when beginning a new web project or page.
---

# Web project kickoff

## 1. Brief (5 lines)
Goal, audience, must-have pages/features, 2–3 reference sites, deadline. Ask only for what's missing.
- Fashion: images lead, editorial layout, big photos, short lines.
- Portfolio: 3–6 works, who you are and what you do on the first screen, fast load.
- Festival: lineup, timetable, tickets, location within 3 clicks, mobile first.
- Small app: rank features by the one job users open it for.

## 2. Direction and wireframe
Pick one design direction, then wireframe (in Figma if connected, otherwise an HTML wireframe).

## 3. Design system first
≤5 colors, ≤2 typefaces, a 4/8px spacing unit, and base button/card/nav — saved as `DESIGN.md` or tokens before building.

## 4. Default stack
- Static site: Next.js (static export) or Astro.
- With login/data: Next.js + Supabase. Tailwind for layout. Deploy on Vercel.
- Secrets in `.env`, never committed.

## 5. Build
Plan → test → implement, one page or feature at a time. Reuse your component library before writing new UI.

## 6. QA, then report
Check 390px and 1440px in a real browser, zero console errors, optimized images, basic accessibility (contrast, alt text, keyboard). Report: link / what's left / decisions needed.
