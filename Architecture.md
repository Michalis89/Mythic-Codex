# Mythic Codex - System Architecture & Database Structure

## 🏛️ System Design Overview
Mythic Codex follows a **modern full-stack architecture** optimized for performance, scalability, and maintainability. The system is structured to handle **character creation, party management, and combat tracking**, ensuring real-time synchronization where necessary.

### **🔹 Core Components:**
- **Frontend** → Next.js (React-based, SSR for fast rendering)
- **Backend** → Supabase (PostgreSQL, Authentication, API)
- **State Management** → Zustand (or Redux if needed)
- **Real-time Sync** → Supabase Realtime (for future live updates)
- **Deployment** → Vercel (frontend) & Supabase (backend)

---

## 🖥️ Frontend Architecture
### **Client-Side Rendering (CSR) + Server-Side Rendering (SSR) Hybrid**
- **SSR for character sheets & dynamic pages** → Faster loading, SEO-friendly.
- **CSR for real-time interactions** → Faster updates in UI.

### **📌 Key Frontend Components:**
1. **Character Sheet UI** → Editable & auto-calculating stats.
2. **Party Management Dashboard** → Overview for DMs.
3. **Combat Tracker** → Initiative, conditions, and health tracking.
4. **State Management** → Zustand for character data, React Query for API calls.

---

## 🗄️ Backend Architecture
### **Supabase as the Backend**
- **PostgreSQL** → Relational database for structured character data.
- **Auth & Role Management** → Supabase Authentication for users & DMs.
- **Edge Functions (Optional)** → For complex backend logic (e.g., auto-calculating stats).
- **Realtime API (Phase 3)** → Combat & Party sync using Supabase Realtime.

### **📌 API Endpoints (Planned)**
| Endpoint           | Method | Purpose                     |
|-------------------|--------|-----------------------------|
| `/api/character`  | `GET`  | Fetch character data        |
| `/api/character`  | `POST` | Create a new character      |
| `/api/character`  | `PUT`  | Update character details    |
| `/api/party`      | `GET`  | Fetch party details         |
| `/api/party`      | `POST` | Create a new party          |
| `/api/combat`     | `POST` | Track combat session        |

---

## 🗃️ Database Schema
### **Character Table (characters)**
```sql
CREATE TABLE characters (
    id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
    user_id UUID REFERENCES users(id) ON DELETE CASCADE,
    name TEXT NOT NULL,
    class TEXT NOT NULL,
    race TEXT NOT NULL,
    background TEXT,
    level INT DEFAULT 1,
    strength INT,
    dexterity INT,
    constitution INT,
    intelligence INT,
    wisdom INT,
    charisma INT,
    created_at TIMESTAMP DEFAULT NOW()
);
```

### **Party Table (parties)**
```sql
CREATE TABLE parties (
    id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
    name TEXT NOT NULL,
    created_by UUID REFERENCES users(id) ON DELETE CASCADE,
    created_at TIMESTAMP DEFAULT NOW()
);
```

### **Party Members Table (party_members)**
```sql
CREATE TABLE party_members (
    party_id UUID REFERENCES parties(id) ON DELETE CASCADE,
    character_id UUID REFERENCES characters(id) ON DELETE CASCADE,
    PRIMARY KEY (party_id, character_id)
);
```

### **Combat Table (combats) - Future Implementation**
```sql
CREATE TABLE combats (
    id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
    party_id UUID REFERENCES parties(id),
    encounter_name TEXT,
    started_at TIMESTAMP DEFAULT NOW()
);
```

---

## 🌍 Data Flow & User Interactions
### **1️⃣ Character Creation Process**
1. User selects class, race, and ability scores.
2. Character data is saved in Supabase.
3. The UI updates state using Zustand.

### **2️⃣ Party & DM Management**
1. A DM creates a party & invites players.
2. Players accept the invite, joining the party.
3. The party dashboard updates in real-time.

### **3️⃣ Combat Tracking (Phase 3)**
1. Players roll initiative.
2. DM starts combat tracking in the UI.
3. Conditions, HP changes, and initiative order update in real time.

---

## 🎯 Next Steps
✅ Finalize character sheet implementation.  
✅ Build API endpoints & integrate with frontend.  
🚀 Expand database structure for party & combat tracking.

---

🔗 **Related Documentation:**
- [Roadmap.md](roadmap.md) - Development phases & features.
- [Tech_Stack.md](tech_stack.md) - Technology choices & reasoning.

