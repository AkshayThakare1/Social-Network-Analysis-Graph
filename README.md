# 🔗 Interactive Social Network Analysis — UTA School of Social Work

An interactive, force-directed network graph that visualizes research-interest connections among 28 faculty members, PhD students, postdoctoral fellows, and alumni. Built with **D3.js**, powered by data processed in **Python/pandas**, and deployable as a single static HTML file via **GitHub Pages**.

🌐 **[Live Demo](https://your-username.github.io)** *(replace with your actual GitHub Pages link)*

---

## 📸 Preview

> Click any node to see who's connected, search by name, and explore the network.

---

## ✨ Features

- **Force-directed layout** — nodes naturally cluster based on shared connections
- **Click-to-inspect side panel** — shows full details for any selected node
- **Person profiles** — click a person to see Role, Institution, Email, and Profile URL
- **Connection explorer** — click a node to highlight it and all its direct neighbors; everything else dims
- **Clickable connection chips** — jump from node to node without losing context
- **Live search bar** — type a name or interest to instantly locate and zoom to it
- **Pan, zoom, and drag** — fully interactive canvas; reposition any node manually
- **Reset View / Fit to Screen / Pause Motion** — toolbar controls for easier navigation
- **Zero backend** — runs entirely in the browser, no server or database required

---

## 🗂️ Dataset

Source file: `peopleToInterests_matrixAndEdgelist.xlsx`

| Sheet | Description |
|---|---|
| `Matrix` | 28×40 binary adjacency matrix (person × research interest) |
| `Edgelist` | 309 flattened (Person → Interest) relationship pairs |
| `Member_Info` | Role, Institution, Profile URL, and Email for each person |

**Network stats:** 68 nodes (28 people + 40 interests) · 309 connections

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Data processing | Python, pandas, openpyxl |
| Visualization engine | [D3.js v7](https://d3js.org/) (force simulation + SVG) |
| Interactivity | Vanilla JavaScript |
| Styling | Custom CSS |
| Hosting | GitHub Pages (static site) |

> **Note:** This project originally explored using [Pyvis](https://pyvis.readthedocs.io/), but was built directly in D3.js instead for finer control over physics, styling, and custom interactivity (click panels, search, neighbor highlighting) that Pyvis doesn't natively support.

---

## 🚀 Getting Started

### View Locally
1. Clone or download this repository
2. Open `index.html` directly in any modern web browser (Chrome, Firefox, Edge, Safari)
3. No installation, server, or build step required

```bash
git clone https://github.com/your-username/your-repo.git
cd your-repo
open index.html   # or just double-click the file
```

### Host on GitHub Pages
1. Push this repository to GitHub
2. Go to **Settings → Pages**
3. Under **Source**, select **Deploy from a branch** → `main` → `/ (root)`
4. Your site will be live at `https://your-username.github.io` within a few minutes

---

## 📁 Project Structure

```
.
├── index.html          # Self-contained graph (HTML + CSS + JS + embedded data)
└── README.md            # This file
```

---

## 🎨 Visual Encoding

| Property | Meaning |
|---|---|
| 🟠 Orange circle | Person (faculty, student, postdoc, alumnus) |
| 🔵 Blue square | Research interest |
| Node size | Number of connections (larger = more connected) |
| Highlighted edges | Connections of the currently selected node |

---

## 🔮 Future Improvements

- [ ] Filter by Role or Institution
- [ ] Auto-color clusters using community detection
- [ ] Export current view as PNG/SVG
- [ ] "Shortest path" finder between any two people
- [ ] Connect to a live data source for easier updates

---

## 📄 License

This project is for academic/educational purposes. Feel free to fork and adapt for your own dataset.

---

## 👤 Author

Built as part of a Social Network Analysis project for UT Arlington School of Social Work.
