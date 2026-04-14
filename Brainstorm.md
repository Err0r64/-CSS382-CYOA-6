# Brainstorm – Choose Your Own Adventure Authoring Tool

**Team Members:** Alec Situ & Hyobin Yook

## Project Summary

A web-based tool with two modes:

1. **Author Mode** – Create and manage branching CYOA stories (nodes, choices, graph visualization), then export for readers
2. **Reader Mode** – Browse available stories and play through them by making choices at each branch point

---

## Finalized User Flow

### Landing Page
- Title: **"Choose Your Own Adventure"**
- Two buttons: **[Author]** and **[Reader]**
- Course credit: CSS 382 — CYOA Group Project, created by Alec Situ and Hyobin Yook

### Author Flow
1. Author clicks **[Author]**
2. Options: **[Upload JSON]** or **[Create New Story]**
3. In the graph editor:
   - Click a node to edit its text and choices
   - Drag to reposition nodes; use **[Align]** to reset layout
   - Add new nodes (spawns at viewport center)
   - Connect nodes by dragging from handles
   - Click an edge label to open the source node's editor
   - Toggle **Vertical / Horizontal** layout
   - Cycle edge style: Curve / Straight / Smooth
4. Export story as JSON

### Reader Flow
1. Reader clicks **[Reader]**
2. Sees a list of available stories
3. Plays through a story:
   - Story text at each node with choice buttons
   - **[Go Back]** and **[Restart]** buttons
   - **[Previous Path]** button shows all historically visited nodes
   - "The End" screen with interactive path graph of visited nodes
   - Can jump back to any previously visited node from the path graph

---

## Key Design Decisions

### Tech Stack
- **React + Vite** – fast setup, component-based
- **React Flow** – interactive graph visualization
- **Tailwind CSS** – rapid styling
- **Dagre** – auto-layout for graph nodes
- **Deployment**: GitHub Pages or Netlify

### Data Format
- All story data stored as **JSON** — no backend required
- Stories stored in **localStorage**; "The Cave of Time" bundled as static JSON

```json
{
  "title": "My Story",
  "startNode": "start",
  "nodes": {
    "start": {
      "title": "Beginning",
      "text": "Your story begins here...",
      "choices": [
        { "text": "Go left", "target": "node-a" },
        { "text": "Go right", "target": "node-b" }
      ],
      "isEnding": false
    }
  }
}
```

### Theme & Settings
- Dark mode default; Light mode available via navbar toggle
- Graph connection style (Curve / Straight / Smooth) persisted to localStorage
- Settings managed globally via `SettingsContext.jsx`

---

## Feature Ideas

### Completed ✅
- Landing page with Author / Reader buttons
- Reader: story list, text display, choice navigation
- Reader: Go Back, Restart, end screen
- Reader: end-of-story visited path graph (horizontal, interactive)
- Reader: Previous Path button (shows all-time visited nodes)
- Reader: jump back to any visited node from path graph
- Author: Upload JSON, Create New Story
- Author: graph editor (add/edit/delete nodes and choices)
- Author: Export JSON
- Author: Help modal
- Author: Align button, layout toggle (vertical/horizontal)
- Author: edge style cycle button
- Author: selected node highlight
- Author: click edge label to edit source node
- Author: "Create new node" from choice dropdown
- Dark / Light mode with full theme support
- Settings modal (appearance + graph connection style)
- Navbar symbols (diamond, sun/moon, gear)

### Nice to Have
- [ ] AI-assisted story continuation (Claude API)
- [ ] Collaborative editing
- [ ] Audio narration
- [ ] Animated page transitions

---

## Architecture

```
src/
├── components/
│   ├── Landing/LandingPage.jsx
│   ├── Reader/StoryList.jsx
│   ├── Reader/StoryReader.jsx
│   ├── Author/AuthorHome.jsx
│   ├── Author/GraphEditor.jsx
│   └── Author/NodeEditor.jsx
├── data/cave-of-time.json
├── utils/storage.js
├── utils/storyHelpers.js
├── SettingsContext.jsx
└── main.jsx
```
