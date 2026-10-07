# 🚀 AeroVerse

<div align="center">

<img src="docs/assets/banner.png" alt="AeroVerse banner" width="100%" />

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Unity](https://img.shields.io/badge/Unity-2021.3_LTS-black?logo=unity)](https://unity.com)
[![Python](https://img.shields.io/badge/Python-3.9+-blue?logo=python)](https://python.org)
[![Flask](https://img.shields.io/badge/Flask-2.x-lightgrey?logo=flask)](https://flask.palletsprojects.com)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-14+-blue?logo=postgresql)](https://postgresql.org)

AeroVerse is a VR-based aerospace education platform that combines 3D exploration, AI tutoring, and computer vision to make learning about space and aircraft more interactive, visual, and practical.

[Overview](#-project-overview) • [Architecture](#-system-architecture) • [Repository Structure](#-repository-structure) • [Getting Started](#-getting-started) • [Team](#-team)

</div>

---

## 📋 Project Overview

AeroVerse transforms theoretical aerospace knowledge into practical, immersive experiences through:

- 🏛️ Virtual Aerospace Museum with interactive 3D environments
- 🤖 AI-powered educational tutor in English and French
- 🔬 Computer vision module for component recognition
- 🚀 Rocket assembly simulation with guided tasks and feedback
- 📚 Structured learning modules covering rockets, satellites, and space missions

### Key Details

- Institution: National School of Computer Science (ENSI)
- Academic Year: 2025 / 2026
- Project ID: 232 — Version 01
- Goal: create a modern educational platform for aerospace outreach and learning

---

## 🧩 System Architecture

```text
┌─────────────────────────────────────────────┐
│                Unity Client                 │
│  3D Museum • Assembly Simulation • UI     │
└──────────────────────┬──────────────────────┘
                       │
                       ▼
             ┌────────────────────┐
             │  Flask API Layer    │
             │  Auth • Modules     │
             │  Progress • Tutor   │
             └─────────┬──────────┘
                       │
        ┌──────────────┼──────────────┐
        ▼              ▼              ▼
 ┌──────────────┐ ┌──────────────┐ ┌────────────────┐
 │ PostgreSQL   │ │ OpenAI API   │ │ Computer Vision│
 │ user data    │ │ AI tutor     │ │ object recog.  │
 └──────────────┘ └──────────────┘ └────────────────┘
```

---

## 🗂️ Repository Structure

```text
AeroVerse/
├── app/                        # Web application (frontend + backend)
│   ├── frontend/               # React interface
│   │   └── src/
│   └── backend/                # Flask REST API
│       ├── routes/
│       ├── models/
│       ├── services/
│       └── config/
├── unity/                      # Unity 3D project
│   └── Assets/
│       ├── Scripts/
│       ├── Scenes/
│       ├── Prefabs/
│       ├── Materials/
│       └── Models/
├── computer-vision/            # CV + AI pipeline
│   ├── models/
│   ├── pipeline/
│   ├── api/
│   ├── training/
│   └── tests/
├── docs/                       # Documentation and assets
├── public/                     # Public web assets
├── src/                        # Frontend source files
├── .github/                    # Issue templates and workflows
├── README.md                   # Project overview
├── package.json                # Frontend configuration
├── vite.config.ts              # Vite configuration
├── tailwind.config.ts          # Tailwind configuration
├── LICENSE                     # MIT license
├── .gitignore                  # Git ignore rules
├── CI.yml                      # CI workflow
├── index.html                  # App entry
└── package-lock.json           # Lockfile
```

---

## ⚙️ Getting Started

### Prerequisites

- Unity 2021.3 LTS
- Python 3.9+
- Node.js 18+
- PostgreSQL 14+
- Git

### 1) Clone the repository

```bash
git clone https://github.com/wiem-benelhajsalahbouhdid/AeroVerse.git
cd AeroVerse
```

### 2) Backend setup

```bash
cd app/backend
python -m venv venv
source venv/bin/activate    # Windows: venv\Scripts\activate
pip install -r requirements.txt
cp .env.example .env
flask db upgrade
flask run
```

### 3) Frontend setup

```bash
cd app/frontend
npm install
cp .env.example .env
npm start
```

### 4) Computer vision setup

```bash
cd computer-vision
pip install -r requirements.txt
python api/server.py
```

### 5) Unity setup

1. Open Unity Hub
2. Add project from the `unity/` directory
3. Use Unity 2021.3 LTS
4. Open `Assets/Scenes/MainMuseum.unity`

---

## 🧪 Features

### Educational Experience
- Immersive museum navigation in 3D
- Content based on aerospace modules and missions
- Interactive learning flow with quizzes and feedback

### AI Tutor
- Ask questions in French or English
- Personalized explanations and knowledge support
- Integration with OpenAI-based services

### Computer Vision
- Real-world component recognition
- AI-assisted identification workflow
- Support for educational object analysis

### Simulation
- Rocket assembly interaction
- Guided tasks with validation
- Immediate user feedback and learning reinforcement

---

## 📅 Sprint Tracker

| Sprint | Focus | Status |
|--------|-------|--------|
| Sprint 1 | Core navigation + user management | ✅ Done |
| Sprint 2 | Hotspots + educational modules | ✅ Done |
| Sprint 3 | AI tutor integration + quizzes | 🔄 In Progress |
| Sprint 4 | Rocket assembly simulation | 📋 Planned |
| Sprint 5 | Computer vision integration | 📋 Planned |
| Sprint 6 | Testing + security + performance | 📋 Planned |
| Sprint 7 | Finalization + deployment | 📋 Planned |

---

## 👥 Team

| Name | Role |
|------|------|
| Ms. Aroua Hedhli | Supervisor / Product Owner |
| Nour Mrabet | Scrum Master |
| Wiem Ben El Haj Salah Bouhdid | Developer |
| Nourhene Grami | Developer |

---

## 🔐 Environment Variables

Create `.env` files using the provided examples in each module.

Example backend variables:

```env
FLASK_ENV=development
DATABASE_URL=postgresql://user:password@localhost:5432/aeroverse
OPENAI_API_KEY=your_openai_key_here
SECRET_KEY=your_secret_key_here
CV_API_URL=http://localhost:5001
```

---

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

<div align="center">

Made with ❤️ by the AeroVerse team — ENSI 2025/2026

</div>
