# 🐕 Dogstudio 3D Website Clone
 
A pixel-perfect clone of the award-winning Dogstudio website featuring a fully animated 3D dog model, custom GLSL shaders, and scroll-based animations.
 
## 🌐 Live Demo
 
- **Frontend:** (add your deployment link here)
- **Original Site:** https://dogstudio.co
 
---
 
## ✨ Features
 
- 🐕 **3D Animated Model** — GLTF dog model with real-time animations using React Three Fiber
- 🎨 **Custom GLSL Shaders** — Dynamic matcap material transitions with smooth interpolation
- 🖱️ **Hover Interactions** — Mouse hover triggers real-time shader uniform updates
- 📜 **Scroll Animations** — GSAP ScrollTrigger for smooth scroll-based 3D transformations
- 🌄 **Background Transitions** — Hover-triggered image transitions with CSS blend modes
- 💡 **WebGL Rendering** — Three.js ReinhardToneMapping and SRGB color space for realistic lighting
 
---
 
## 🛠️ Tech Stack
 
| Technology | Purpose |
|---|---|
| React + Vite | UI Framework |
| Three.js | 3D Graphics Engine |
| React Three Fiber | React renderer for Three.js |
| React Three Drei | 3D helpers (GLTF, Textures, Controls) |
| GSAP + ScrollTrigger | Scroll-based animations |
| Custom GLSL Shaders | Material transitions |
 
---
 
## 📁 Project Structure
 
```
dogstudio-clone/
├── public/
│   ├── models/
│   │   ├── dog.drc.glb        → 3D dog model
│   │   ├── dog_normals.jpg    → Normal map texture
│   │   ├── branches_diffuse.jpg
│   │   └── branches_normals.jpg
│   ├── matcap/
│   │   └── mat-1.png to mat-20.png  → Matcap textures
│   └── background-l.png
│
└── src/
    ├── components/
    │   └── Dog.jsx            → 3D model + shaders + animations
    ├── App.jsx                → Main layout + sections
    ├── App.css                → Styles
    └── main.jsx               → Entry point
```
 
---
 
## 🚀 Getting Started
 
### Prerequisites
- Node.js v18+
 
### 1. Clone the repository
```bash
git clone https://github.com/Priyanksri/dog-studio-clone.git
cd dog-studio-clone
```
 
### 2. Install dependencies
```bash
npm install
```
 
### 3. Start the dev server
```bash
npm run dev
```
 
### 4. Open the app
```
http://localhost:5173
```
 
---
 
## 🎨 How It Works
 
### 3D Model & Animations
```
→ GLTF dog model loaded with useGLTF hook
→ Built-in animations played using useAnimations
→ Model positioned and rotated in 3D space
→ DirectionalLight for realistic lighting
```
 
### Custom GLSL Shaders
```
→ Two matcap textures blended using smoothstep()
→ uProgress uniform controls transition amount
→ GSAP animates uProgress from 1.0 → 0.0
→ Creates smooth material color transitions
```
 
### Scroll Animations
```
→ GSAP ScrollTrigger watches scroll position
→ Dog model moves along Z and Y axis on scroll
→ Model rotates 180° as user scrolls down
→ Scrub: true creates smooth tied-to-scroll feel
```
 
### Hover Interactions
```
→ Each title hover updates uMatcap1 uniform
→ GSAP animates the transition smoothly
→ Background image changes via CSS :has() selector
→ Dog material color matches the hovered section
```
 
---
 
## 📦 Dependencies
 
```bash
npm install three @react-three/fiber @react-three/drei gsap @gsap/react
```
 
---
 
## 👨‍💻 Author
 
**Priyank**
- GitHub: [@Priyanksri](https://github.com/Priyanksri)
 
---
 
## 📝 License
 
This project is open source and available under the [MIT License](LICENSE).
 
---
 
## 🙏 Credits
 
- Original design by [Dogstudio](https://dogstudio.co)
- Built for educational purposes only