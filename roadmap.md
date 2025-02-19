# Mythic Codex - Development Roadmap

## 🚀 Phase 1: MVP - Character Builder (Initial Release)

**Goal:** Develop and deploy a fully functional D&D Character Builder.

### ✅ Core Features for First Release

- 🎭 **Character Sheet UI** - Editable fields, structured like a D&D sheet.
- 🎲 **Ability Scores Management** - Point Buy, Standard Array, Rolling.
- ⚔️ **Skills & Proficiencies** - Auto-calculated modifiers.
- 🛡 **Combat Stats** - AC, HP, Initiative, Death Saves.
- 🎒 **Inventory & Equipment** - Basic item tracking.
- 🔮 **Spell Management** - Spell slots & known spells.
- 💾 **Save & Load Characters** - Store character data in a database.

### 🛠 Technologies for Phase 1

- **Frontend:** Next.js, Zustand, Tailwind CSS
- **Backend:** Supabase, PostgreSQL
- **State Management:** React Query / SWR
- **\*\*\*\*Auth & User Accounts:** Supabase Auth

### 🎯 Deployment Plan

- 🔧 Final testing & bug fixing.
- 🚀 Deploy first version.
- 📣 Announce & gather feedback.

---

## 🏹 Phase 2: Party & Campaign Management

**Goal:** Add Dungeon Master tools & multi-character management.

### 📌 Planned Features

- 🏹 **Party Overview** - Display all player characters.
- 🗺 **Quest Log** - Track quests and story progress.
- 🎩 **NPC Manager** - Create and manage NPCs.
- 💰 **Shared Loot System** - Manage distributed gold & items.

### 🛠 Technologies for Phase 2

- **Database Expansion:** More relational tables for party & quest tracking.
- **API Development:** Custom API endpoints for campaign management.

---

## ⚔️ Phase 3: Battle & Combat Tracking

**Goal:** Implement combat tools for real-time encounters.

### 📌 Planned Features

- 🎲 **Initiative Tracker** - Automatically order combat turns.
- 💀 **Conditions & Status Effects** - Track buffs, debuffs & injuries.
- 🏹 **Damage Calculator** - Log attack rolls and damage.

### 🛠 Technologies for Phase 3

- **Real-time Updates:** WebSockets or Supabase Realtime for battle tracking.
- **UI Enhancements:** Interactive battle maps & condition tracking.

---

## 🌍 Future Expansions

**Goal:** Extend Mythic Codex with advanced customization & online features.

### 📌 Ideas for Future Updates

- 🏆 **Multiclassing & Homebrew Features.**
- 📜 **Dynamic Worldbuilding** - City, region, and event management.
- 🏴‍☠️ **Faction & Reputation System.**
- 🔗 **Live Session Sync** - Real-time collaboration between players and DM.
- 🎤 **Voice & Chat Integration** for online play.

### 🛠 Future Technologies

- **Cloud Storage:** Object storage for player uploads (e.g., character images, homebrew content).
- **AI-Powered Tools:** Automated NPC generation, quest suggestions.

---

## 🛠 Development Workflow

📌 GitHub Branch Strategy

- `main` - Stable production-ready branch.
- `dev` - Active development branch.
- Feature-specific branches for individual updates.

📌 Contribution Guidelines

- Feature requests & issues tracked on GitHub.
- Pull requests reviewed before merging into `main`.

---

## 🎯 Next Steps

- ✅ Finalize Character Builder (Phase 1).
- 🚀 Prepare for first deployment.
- 📅 Plan for Phase 2 development.

---

🔗 **Related Documentation:**

- [Features.md](features.md) - Core features breakdown.
- [Architecture.md](architecture.md) - System design & database structure.

