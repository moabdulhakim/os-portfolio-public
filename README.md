<div align="center">

# 🖥️ Portfolio OS

**An interactive portfolio disguised as a Windows 11-style operating system**

[![Next.js](https://img.shields.io/badge/Next.js-13-black?logo=next.js)](https://nextjs.org/)
[![React](https://img.shields.io/badge/React-18-61DAFB?logo=react)](https://reactjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?logo=typescript)](https://www.typescriptlang.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3-38BDF8?logo=tailwind-css)](https://tailwindcss.com/)
[![Three.js](https://img.shields.io/badge/Three.js-0.150-black?logo=three.js)](https://threejs.org/)
[![Vercel](https://img.shields.io/badge/Deployed_on-Vercel-black?logo=vercel)](https://vercel.com/)

</div>

---

## 📖 Table of Contents

- [Overview](#-overview)
- [Live Demo](#-live-demo)
- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
- [Environment Variables](#-environment-variables)
- [Pages & Navigation](#-pages--navigation)
- [OS Applications](#-os-applications)
- [Animations & Effects](#-animations--effects)
- [Deployment](#-deployment)
- [Author](#-author)

---

## 🌟 Overview

**Portfolio OS** is a unique, fully interactive developer portfolio that simulates a **Windows 11 desktop operating system** inside the browser. Instead of a traditional scrolling portfolio, visitors get to explore a real desktop experience complete with draggable/resizable windows, a Start Menu, a Taskbar, power controls, and several built-in applications — all while discovering the developer's skills and projects.

The experience is built on **Next.js 13**, enriched with **Three.js** 3D graphics, **Framer Motion** / **React Spring** animations, **tsParticles** backgrounds, and a **Zustand**-powered OS state machine.

---

## 🚀 Live Demo

> **[Try it live →](https://osportfolio.vercel.app/pc/os)**

---

## ✨ Features

### 🖥️ Windows 11-style Desktop OS
- **Draggable & resizable windows** powered by `react-rnd`
- **Taskbar** with quick-launch icons for all open programs
- **Start Menu** with app search, quick launchers, and power options
- **Right-click Context Menu** with view size controls, refresh, and appearance settings
- **Boot animation** — an 8-second startup sequence before the desktop loads
- **Fullscreen mode** for a truly immersive OS feel
- **Wallpaper customization** — choose from 7 different desktop backgrounds
- **Desktop icon size control** — Small / Medium / Large
- **Shutdown & Restart simulation**

### 🖱️ Interactive 3D PC
- A fully rendered **3D desktop computer model** (Three.js + React Three Fiber)
- Click **"Lights On"** to power up the machine and navigate into the OS
- **OrbitControls** for rotating and inspecting the 3D model
- Particle animation background

### 💼 Portfolio Section
- **Skills** — 15+ technology icons with a smooth **parallax scrolling** effect
- **Projects** — 7+ featured projects in a **Swiper carousel** (card flip effect)
- **Contact** — Email form integrated with **EmailJS** for live delivery
- **Resume** — Downloadable PDF CV

### 🎨 Visual Polish
- Cursor light effect that follows the mouse
- Particle background animations
- Glassmorphism UI design
- Smooth page transitions and micro-interactions
- Dark theme with custom accent gradients

---

## 🛠️ Tech Stack

| Category | Technology |
|---|---|
| **Framework** | Next.js 13, React 18 |
| **Language** | TypeScript 5 |
| **Styling** | Tailwind CSS 3, PostCSS, Autoprefixer |
| **State Management** | Zustand 4 |
| **Animations** | Framer Motion 10, React Spring 9, tsParticles 2 |
| **3D Graphics** | Three.js 0.150, React Three Fiber 8, React Three Drei 9 |
| **Window Management** | react-rnd 10 |
| **UI Components** | React Icons 4, Swiper 9, React Tilt 1 |
| **Email** | EmailJS 3 |
| **HTTP** | Axios 1 |
| **Utilities** | Moment.js 2 |
| **Fullscreen** | react-full-screen 1 |
| **Linting** | ESLint 8 |

---

## 📁 Project Structure

```
Portfolio_OS/
├── src/
│   ├── components/
│   │   ├── os/                        # OS shell components
│   │   │   ├── programs/              # Draggable window apps
│   │   │   │   ├── VScode.tsx         # GitHub1S embedded viewer
│   │   │   │   ├── Chrome.tsx         # Browser app
│   │   │   │   ├── Edge.tsx           # Browser app
│   │   │   │   ├── Appearance.tsx     # Wallpaper selector
│   │   │   │   └── Program.tsx        # Base draggable/resizable window
│   │   │   ├── OsContainer.tsx        # Desktop canvas
│   │   │   ├── Navbar.tsx             # Taskbar
│   │   │   ├── StartMenu.tsx          # Start menu
│   │   │   └── Startup.tsx            # Boot sequence animation
│   │   ├── portfolio/                 # Portfolio content components
│   │   │   ├── Projects.tsx           # Swiper project cards
│   │   │   ├── Skills.tsx             # Parallax skill icons
│   │   │   ├── Contact.tsx            # EmailJS contact form
│   │   │   └── Resume.tsx             # PDF resume viewer
│   │   ├── canvas/
│   │   │   └── Computers.tsx          # Three.js 3D desktop model
│   │   ├── particles/
│   │   │   └── MainParticles.tsx      # tsParticles background
│   │   ├── ContextMenu.tsx            # Right-click menu
│   │   ├── CursorLight.tsx            # Mouse cursor light effect
│   │   └── Loader.tsx                 # Loading spinner
│   ├── pages/
│   │   ├── index.tsx                  # Welcome / landing page
│   │   ├── pc/
│   │   │   ├── index.tsx              # Interactive 3D PC page
│   │   │   └── os.tsx                 # Full OS desktop environment
│   │   └── portfolio/
│   │       ├── index.tsx              # Portfolio navigation hub
│   │       ├── skills.tsx             # Skills page
│   │       ├── projects.tsx           # Projects page
│   │       └── contact.tsx            # Contact page
│   └── styles/
│       └── globals.css                # Global CSS (fonts, scrollbar, gradients)
├── constants/
│   └── index.ts                       # App-wide config (projects, nav links, programs)
├── libs/
│   └── osStates.ts                    # Zustand OS state store
├── utils/
│   ├── animationProps.ts              # React Spring animation presets
│   ├── motion.ts                      # Framer Motion animation variants
│   └── functions.ts                   # Shared utility functions
├── public/
│   ├── assets/                        # Images, icons, wallpapers, CV
│   └── desktop_pc/scene.gltf          # 3D desktop model
├── types.ts                           # Shared TypeScript interfaces
├── next.config.js                     # Next.js configuration
├── tailwind.config.js                 # Tailwind configuration
├── tsconfig.json                      # TypeScript configuration
└── vercel.json                        # Vercel deployment configuration
```

---

## 🚀 Getting Started

### Prerequisites

- **Node.js** >= 18.0.0
- **npm** or **yarn**

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/moabdulhakim/Portfolio_OS.git
cd Portfolio_OS

# 2. Install dependencies
npm install

# 3. Set up environment variables (see section below)
cp .env.example .env   # or create .env manually

# 4. Start the development server
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

### Available Scripts

| Command | Description |
|---|---|
| `npm run dev` | Start development server |
| `npm run build` | Build for production |
| `npm start` | Run production server |
| `npm run lint` | Run ESLint |

---

## 🔐 Environment Variables

Create a `.env` file in the root directory with the following variables (required for the Contact form):

```env
EMAILJS_SERVICE_ID=your_emailjs_service_id
EMAILJS_TEMPLATE_ID=your_emailjs_template_id
EMAILJS_PUBLIC_KEY=your_emailjs_public_key
```

> Sign up at [EmailJS](https://www.emailjs.com/) to obtain these credentials. Without them, the contact form will not send emails, but the rest of the application works normally.

---

## 🗺️ Pages & Navigation

| Route | Description |
|---|---|
| `/` | Welcome / landing page |
| `/pc` | Interactive 3D PC with lights toggle |
| `/pc/os` | Full Windows 11-style OS desktop |
| `/portfolio` | Portfolio navigation hub |
| `/portfolio/skills` | Skills with parallax scrolling |
| `/portfolio/projects` | Projects showcase carousel |
| `/portfolio/contact` | Contact form |

---

## 💻 OS Applications

| App | Description |
|---|---|
| **VS Code** | Embedded [GitHub1S](https://github1s.com/) code viewer for the portfolio repo |
| **Chrome** | In-OS browser application |
| **Edge** | In-OS browser application |
| **Appearance** | Choose from 7 desktop wallpapers |
| **Skills** | Browse the portfolio Skills section |
| **Projects** | Browse the portfolio Projects section |
| **Contact** | Send a message via the Contact form |

Each app opens as a **draggable, resizable window** and can be minimized, maximized, or closed — just like a real OS.

---

## 🎬 Animations & Effects

| Effect | Library |
|---|---|
| Page & element transitions | Framer Motion |
| Text, opacity & width animations | React Spring |
| Particle backgrounds | tsParticles |
| 3D desktop model | Three.js + React Three Fiber |
| Project card carousel | Swiper (card effect) |
| Skills hover tilt | React Tilt |
| Cursor light trail | Custom CSS + React |

---

## ☁️ Deployment

The project is deployed on **[Vercel](https://vercel.com/)** using the configuration in `vercel.json`. To deploy your own instance:

1. Fork this repository.
2. Import it into your Vercel account.
3. Add the three EmailJS environment variables in the Vercel dashboard.
4. Deploy — Vercel handles the rest automatically.

---

## 👤 Author

**Mohammad AbdulHakim (AboMisr)**

[![GitHub](https://img.shields.io/badge/GitHub-moabdulhakim-181717?logo=github)](https://github.com/moabdulhakim)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Mohammad_AbdulHakim-0077B5?logo=linkedin)](https://www.linkedin.com/in/moabdulhakim)

---

<div align="center">

Made with ❤️ — a portfolio unlike any other.

</div>
