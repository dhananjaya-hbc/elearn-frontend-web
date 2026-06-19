# AGENT.md - Frontend Web (Next.js)

## Project Overview
This is the web frontend of our application built with Next.js 14, TypeScript, Tailwind CSS, and shadcn/ui.

## Tech Stack
- **Framework**: Next.js 14 (App Router)
- **Language**: TypeScript
- **Styling**: Tailwind CSS + shadcn/ui
- **State Management**: Zustand
- **Server State**: TanStack Query (React Query)
- **Forms**: React Hook Form + Zod
- **HTTP Client**: Axios
- **Authentication**: JWT (Access Token + Refresh Token)

## Project Setup

### 1. Create Project
```bash
npx create-next-app@latest frontend-web
```
Select these options:
- TypeScript: Yes
- ESLint: Yes
- Tailwind CSS: Yes
- src/ directory: Yes
- App Router: Yes
- Import alias: Yes (@/*)

### 2. Install shadcn/ui
```bash
cd frontend-web
npx shadcn@latest init
```
Select these options:
- Style: Default
- Base color: Slate
- CSS variables: Yes

### 3. Install Dependencies
```bash
npm install axios zustand @tanstack/react-query
npm install react-hook-form zod @hookform/resolvers
npm install clsx class-variance-authority lucide-react
npm install date-fns
npm install sonner
npm install --save-dev @types/node
npm install @tanstack/react-query-devtools
```

### 4. Install shadcn Components
```bash
npx shadcn@latest add button
npx shadcn@latest add input
npx shadcn@latest add form
npx shadcn@latest add card
npx shadcn@latest add toast
npx shadcn@latest add sonner
npx shadcn@latest add dialog
npx shadcn@latest add dropdown-menu
npx shadcn@latest add avatar
npx shadcn@latest add badge
npx shadcn@latest add table
npx shadcn@latest add sidebar
npx shadcn@latest add sheet
npx shadcn@latest add separator
npx shadcn@latest add skeleton
```

## Run Locally
```bash
npm install
npm run dev
```
App runs at: http://localhost:3000

## Build
```bash
npm run build
npm start
```

## Code Style Rules
- All components must be TypeScript
- Use "use client" directive only when needed
- Server components by default
- No any types - define proper interfaces
- All API calls go through src/lib/api/ folder
- All forms must have Zod validation
- All protected pages must be inside (dashboard) route group