# ToDo – Choose Your Own Adventure Project

**Team Members:** Alec Situ & Hyobin Yook

---

## Phase 0: Setup ✅
- [x] Fork repo and add team members as contributors
- [x] Set up React + Vite project
- [x] Install dependencies: React Flow, Tailwind, Dagre
- [x] Verify local dev server runs
- [x] Commit and push initial project scaffold

---

## Phase 1: Landing Page ✅
- [x] Create `LandingPage` with title and Author / Reader buttons
- [x] Add course credit line (CSS 382 — Alec Situ and Hyobin Yook)
- [x] Improve credit text visibility in both dark and light mode

---

## Phase 2: Reader Mode ✅
- [x] `StoryList` — shows all available stories
- [x] `StoryReader` — displays node text and choices
- [x] Go Back button (history stack)
- [x] Restart button
- [x] End screen at terminal nodes
- [x] Pre-load Cave of Time demo story
- [x] End-of-story visited path graph (horizontal, interactive)
- [x] Path graph: Enlarge button for full-screen view
- [x] Path graph: Align and Vertical/Horizontal toggle buttons
- [x] Path graph: node handles adapt to layout direction
- [x] All-time visited nodes persisted to localStorage across sessions
- [x] Previous Path button — shows historically visited nodes any time during reading
- [x] Jump back to any visited node from path graph

---

## Phase 3: Author Mode ✅
- [x] `AuthorHome` — Upload JSON and Create New Story options
- [x] `GraphEditor` — interactive graph editor
- [x] Add / edit / delete nodes and choices
- [x] Node editor panel (title, text, choices, ending flag)
- [x] Node IDs hidden from users
- [x] New node spawns at viewport center
- [x] "Create new node" option inside choice target dropdown
- [x] Click edge label to open source node's editor
- [x] Selected node highlighted in gold
- [x] Export JSON button
- [x] Help modal with usage instructions
- [x] Align button — resets node positions to auto-layout
- [x] Vertical / Horizontal layout toggle
- [x] Edge style cycle button (Curve / Straight / Smooth)
- [x] Handle positions adapt to layout direction
- [x] Zoom controls styled and theme-aware

---

## Phase 4: Graph Visualization ✅
- [x] React Flow graph with dagre auto-layout
- [x] Nodes color-coded: Start (green), Ending (red), Orphan (yellow), Normal (default)
- [x] Edge labels show choice text
- [x] Smooth / stepped / straight edge style options
- [x] MiniMap with theme-aware colors
- [x] Legend (Start / Ending / Orphan / Normal)

---

## Phase 5: Data Layer ✅
- [x] JSON schema defined
- [x] `storage.js` helpers: `saveStory`, `getStory`, `generateNodeId`, `getVisitedNodes`, `mergeVisitedNodes`
- [x] On app load: seed localStorage with Cave of Time
- [x] Validate imported JSON on upload

---

## Phase 6: Theme & Settings ✅
- [x] `SettingsContext.jsx` — global state for theme and edge style
- [x] Dark mode default; Light mode toggle in navbar
- [x] Settings modal: Appearance (Dark/Light) + Graph Connection Style
- [x] All graph elements (nodes, edges, controls, minimap, legend) theme-aware
- [x] Navbar: filled diamond, sun/moon toggle, gear icon

---

## Phase 7: Deploy
- [ ] Build production bundle: `npm run build`
- [ ] Deploy to Netlify or GitHub Pages
- [ ] Verify deployed URL end-to-end
- [ ] Update README.md with deployed URL and repo URL

---

## Phase 8: Documentation
- [x] Brainstorm.md created and updated
- [x] ToDo.md created and updated
- [x] CHANGELOG-v3.md created
- [ ] Update Codebase.md to describe current architecture
- [ ] Ensure all team members have commits visible on GitHub
- [ ] README.md includes deployed URL + repo URL

---

## Assignment Checklist
- [x] Repo forked, all members are contributors
- [x] Brainstorm.md created
- [x] ToDo.md created
- [x] CHANGELOG-v3.md created
- [ ] Project deployed on public website
- [ ] All members have commits on GitHub
- [ ] README.md includes deployed URL + repo URL
