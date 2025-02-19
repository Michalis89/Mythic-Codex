# Mythic Codex - Technology Stack Overview

## 🏗️ Why These Technologies?
Mythic Codex is designed to be a **scalable, performant, and easy-to-maintain** application for managing D&D characters, parties, and campaigns. Each technology was chosen based on its **performance, ease of use, and compatibility** with our project goals.

---

## 🖥️ Frontend: Next.js
### ✅ Why Next.js?
- **Server-side Rendering (SSR) & Static Generation (SSG)** → Faster performance, better SEO.
- **API Routes** → Easy backend logic handling within the same framework.
- **Image Optimization & Lazy Loading** → Improves performance for large character sheets.
- **Built-in Routing** → Simplifies navigation.

---

## 🎨 Styling: Tailwind CSS
### ✅ Why Tailwind?
- **Utility-first approach** → Faster UI development.
- **Responsive by design** → Adapts easily across devices.
- **Highly customizable** → Can match the aesthetic of D&D character sheets.
- **Better performance** → Reduces unused CSS with tree-shaking.

---

## 📦 State Management: Zustand (Initially) & Redux (If Needed)
### ✅ Why Zustand for MVP?
- **Lightweight (~1KB)** → Minimal overhead.
- **No boilerplate** → Simpler than Redux.
- **Works without context providers** → Direct store usage in components.
- **Persistable state** → Can store character data in `localStorage`.

### 🔄 When to Consider Redux?
- **If state management becomes too complex** (e.g., sharing data across multiple features like Party Management, Combat Tracking).
- **For strict immutability & debugging** (Redux DevTools).

---

## 🗄️ Backend: Supabase (PostgreSQL)
### ✅ Why Supabase?
- **PostgreSQL-based** → Strong relational database structure.
- **Built-in Authentication** → Secure user accounts.
- **Realtime capabilities** → Can be used for battle tracking.
- **Scalable & managed** → Less backend maintenance required.
- **Open-source alternative to Firebase**.

---

## 🔄 API & Data Fetching: React Query / SWR
### ✅ Why React Query or SWR?
- **Efficient caching & background updates**.
- **Automatic data synchronization**.
- **Reduces API call overhead**.

---

## ⚡ Realtime & WebSockets (Planned for Phase 3)
### ✅ Why WebSockets (Supabase Realtime)?
- **Live combat tracking** → Players & DMs can see changes instantly.
- **Party Management Sync** → Updates reflect across all connected users.

---

## 🔐 Authentication: Supabase Auth
### ✅ Why Supabase Auth?
- **Built-in user management**.
- **OAuth & social login support**.
- **JWT-based authentication**.
- **Seamless integration with Supabase Database**.

---

## 📡 Hosting & Deployment
### ✅ Vercel (for frontend) & Supabase (for backend)
- **Vercel** → Best for Next.js, automatic deployments.
- **Supabase** → Scalable backend, integrated authentication.

---

## 🌍 Future Technologies (For Expansions)
- **Cloud Storage** → Upload character images & homebrew content.
- **AI-powered NPC Generation** → Procedural NPC & quest suggestions.
- **Voice & Chat Integration** → Built-in communication for online sessions.

---

## 🎯 Summary
| Technology       | Purpose                       | Why? |
|-----------------|-----------------------------|------|
| **Next.js** | Frontend framework | Fast, SSR, API handling |
| **Tailwind CSS** | Styling | Lightweight, responsive UI |
| **Zustand (Initially)** | State management | Simple, minimal setup |
| **Redux (If needed)** | Complex state management | Scalable global store |
| **Supabase** | Backend (PostgreSQL) | Scalable, real-time features |
| **React Query / SWR** | API data fetching | Efficient, automatic caching |
| **WebSockets (Future)** | Real-time updates | Sync combat & party data |
| **Supabase Auth** | User authentication | Secure login & JWT-based auth |
| **Vercel + Supabase** | Hosting & deployment | Optimized for Next.js |

---

🔗 **Related Documentation:**
- [Roadmap.md](roadmap.md) - Feature development plan.
- [Architecture.md](architecture.md) - System structure & database schema.

