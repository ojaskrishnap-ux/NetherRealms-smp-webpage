# Chills Panel — NetherRealms Edition

A modern, Realms-style Minecraft server control panel built as a **single-file HTML frontend**.  
Chills is designed to look and feel like a professional hosting panel while remaining **frontend-only**, using **webhooks** for all real actions.

---

## ✨ Features

### 🔐 Authentication
- Sign In / Sign Up UI
- Owner account support
- Session persistence (localStorage)
- Sidebar hidden on login, unlocked on dashboard

### 🧭 Dashboard
- Realms-style **Server Cards**
- Up to **3 server slots**
- Create server instantly (frontend)
- Clean navigation with working Dashboard button

### 🖥️ Server Panel
- Aternos-style sidebar layout
- Animated **Start Server** button
- Server states:
  - Offline
  - Queue (awaiting approval / manual start)
- NetherRealms server address with copy button

### 🧾 Console
- Command input (no fake logs)
- Commands sent directly to webhook
- Clean, realistic console design

### 👥 Player Actions
- OP / Ban / Heal / Kill buttons
- UI actions → webhook payloads
- No fake inventory or player data

### 🎨 Design
- NetherRealms purple theme
- Glowing logo & smooth animations
- Mobile-friendly layout
- Works on **HTTP** (no HTTPS required)

---

## 🔗 Webhook Integration

All real actions are handled externally.

The panel sends JSON payloads including:
- Action type
- Username
- Server data
- Command text (if applicable)
- Timestamp

Example payload:
```json
{
  "type": "COMMAND",
  "user": "superdude",
  "data": {
    "command": "/op Steve"
  },
  "time": "2026-02-13T12:00:00Z"
}
