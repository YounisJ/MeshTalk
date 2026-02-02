# MeshTalk — Hybrid Offline & Online Secure Messaging (FYP)

MeshTalk is an Android messaging application designed to keep communication working even when the internet is unavailable. It supports **offline messaging using Bluetooth Low Energy (BLE) mesh networking** and **online synchronization using Firebase**, with a focus on **end-to-end encryption (E2EE)** for message privacy.

> Final Year Project (BSCS) — Sukkur IBA University

---





## ✨ Key Features
- **Hybrid Communication**
  - Offline mode: BLE mesh (peer-to-peer + multi-hop forwarding)
  - Online mode: Firebase sync and delivery
- **Security**
  - End-to-end encryption (AES-256 for message content)
  - Secure key exchange (ECC)
- **Reliable Messaging**
  - Local message queue when offline
  - Auto sync when connectivity is restored
- **User Experience**
  - Clean chat interface
  - Online/offline indicators
  - Delivery status tracking (basic)

---

## 🧰 Tech Stack
- **Android:** Android Studio (Java / Kotlin)
- **Offline Networking:** Bluetooth Low Energy (BLE) + mesh-style forwarding
- **Online Backend:** Firebase Realtime Database / Firebase Cloud Messaging (FCM)
- **Local Storage:** SQLite / Room DB
- **Security:** AES-256 + ECC (key exchange)

---

## 📌 System Overview (High Level)
1. User composes a message
2. App encrypts message locally (E2EE)
3. If **offline**, message is transmitted via BLE to nearby nodes (multi-hop forwarding)
4. If **online**, message is sent via Firebase
5. Messages are stored locally and synced when internet is available

---

## 🚀 Getting Started (Developer Setup)
### Prerequisites
- Android Studio (latest stable)
- Android device with Bluetooth 5.0+ recommended
- Firebase project (Realtime DB + optional FCM)

### Setup Steps
1. Clone the repo:
   ```bash
   git clone https://github.com/YounisJ/meshtalk.git
   cd meshtalk
