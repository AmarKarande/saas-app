# 🧠 Companion AI — Build Your Own AI Friends

A modern, full-stack SaaS platform for creating, managing, and chatting with custom AI companions. Built with **Next.js 14 App Router**, **Clerk**, and **Supabase**.

---

## 🚀 Features

- 🔐 Secure Authentication via Clerk
- ✨ Custom Companion Creation (Name, Bio, Instructions)
- 🧠 Real-time Chat with AI Models
- 📜 Companion Session History
- ⭐ Bookmark & Save Your Favorites
- 📊 Feature-Flag Support (e.g., plan-based access)
- 🔁 Dynamic Pagination, Filtering, and Caching
- 🧾 Fully typed with modern server actions

---

## 🛠 Tech Stack

| Layer       | Tech                        |
|-------------|-----------------------------|
| Frontend    | Next.js 14 + Tailwind CSS   |
| Backend     | Supabase (Postgres + API)   |
| Auth        | Clerk.dev                   |
| Hosting     | Vercel                      |
| DB Client   | Supabase JS                 |
| State Mgmt  | Server Actions + Cache APIs |

---

## Add Environment Variables
 Create a .env.local file in the root:
 
 NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=your_key
CLERK_SECRET_KEY=your_secret
SUPABASE_URL=https://your-project.supabase.co
SUPABASE_ANON_KEY=your_anon_key
SUPABASE_SERVICE_ROLE_KEY=your_service_role

## Auth & Permissions
Clerk's auth() helper is used for:

User Authentication

Plan/Feature-Based Permissions via has()


## Core Server Actions
createCompanion() – Create new AI entity

getAllCompanions() – Paginated fetch with filters

addToSessionHistory() – Store chat history

addBookmark() / removeBookmark() – Manage favorites

newCompanionPermissions() – Feature gating by plan

## Supabase Tables
companions: AI profile info

session_history: User interaction logs

bookmarks: User favorites

## Deployment
Deploy easily to Vercel with your environment variables.
Other options: Netlify, Railway, or custom Node hosting.

