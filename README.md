# 21 Days — Habit Challenge App

**Small actions. 21 days. A different you.**

A calm, motivating web app to build good habits or leave bad ones over a 21-day journey.

## Design

- **Warm Cream** `#FFF8F0` background  
- **Sage Green** `#7A9E7E` for growth & progress  
- **Coral** `#E9785B` for action & CTAs  
- **Forest Green** `#3F6044` for strong progress  
- Soft cards, rounded UI, mobile-first  

## Features

- User registration & login (local demo auth)
- Onboarding flow to create first challenge
- Build a Habit 🌱 or Leave a Habit 🚫
- Daily check-in with mood & optional journal
- 21-day visual timeline with milestones (Day 7, 14, 21)
- Streak tracking (gentle — no harsh failure messaging)
- Progress & history
- Profile & logout
- Responsive: sidebar on desktop, bottom nav + prominent Add on mobile
- Confetti celebration on completion

## Tech Stack

- React 19 + TypeScript
- Vite
- Tailwind CSS v4
- React Router
- Framer Motion (subtle animations)
- date-fns
- lucide-react
- canvas-confetti

**Persistence:** localStorage (works offline / no backend required).  
Structure is ready to swap in Supabase Auth + tables when you add your project keys.

## Quick Start

```bash
cd 21-days
npm install
npm run dev
```

Open the URL shown (usually `http://localhost:5173`).

### Demo flow

1. Click **Start My 21 Days** → Create account  
2. Complete onboarding (choose build/leave, habit, start date, goal, optional reminder)  
3. Dashboard → Mark Done / I Resisted Today  
4. View Journey for the 21-day timeline  
5. Progress, History, Profile from the nav  

Data stays in the browser. Clear site data to reset.

## Project structure

```
src/
├── components/     # UI + HabitCard, CheckInModal
├── pages/          # Landing, Auth, Dashboard, Journey, …
├── layouts/        # AppLayout (sidebar + mobile nav)
├── hooks/          # useAuth, useHabits
├── services/       # auth + habits (localStorage)
├── lib/            # storage helpers
├── types/          # shared TypeScript types
├── utils/          # dates, id
└── styles via index.css (Tailwind + theme)
```

## Supabase (optional)

1. Create a Supabase project  
2. Enable Email auth  
3. Create tables matching the data model in `src/types` (users, habits, daily_check_ins)  
4. Replace `src/services/auth.ts` and `src/services/habits.ts` with Supabase client calls  
5. Add `.env`:

```
VITE_SUPABASE_URL=...
VITE_SUPABASE_ANON_KEY=...
```

## Philosophy

> One missed day doesn’t erase your progress.  
> Consistency over perfection.

Built to feel personal, calm, and rewarding — not like a corporate tracker.
