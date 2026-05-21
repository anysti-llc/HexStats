<div align="center">

# ⬡ HexStats

**A lightweight, gothic-aesthetic Windows system monitor widget**

![Version](https://img.shields.io/badge/version-v1.2.0-FF69B4?style=flat-square)
![License](https://img.shields.io/badge/license-MIT-da5bff?style=flat-square)
![Platform](https://img.shields.io/badge/platform-Windows-0c0810?style=flat-square&logoColor=FF69B4)
![Open Source](https://img.shields.io/badge/open%20source-yes-FF69B4?style=flat-square)

*Born from candlelight and code. Built for those who want beauty in their workflow.*

</div>

---

## ✨ What is HexStats?

HexStats is a minimal, always-on-top Windows desktop widget that keeps your system vitals visible at a glance — styled in a dark gothic aesthetic with hot pink accents. No bloat, no installation, no background services. Just one `.hta` file sitting quietly in the corner of your screen, doing its job with elegance.

**Tracks:**
- 🔲 **CPU** usage with color-coded progress bar
- 📋 **RAM** used / total with percentage
- 💿 **Disk C:** used / total with percentage
- ⏱ **Uptime** since last boot
- 🌐 **Network** download & upload speed (live)

**Bar colors respond to load:**
| Usage | Color | Status |
|---|---|---|
| 0 – 54% | 🩷 Hot Pink | All good |
| 55 – 79% | 🟣 Purple | Getting warm |
| 80 – 100% | 🔴 Red-Pink | Danger zone |

---

## 📋 Requirements

- **Windows 10 or 11**
- No installation required
- No third-party software needed
- Runs natively via Windows HTA (HTML Application) engine

---

## 🚀 Getting Started

**1. Download**

Head to the [Releases](../../releases) page and download the latest `HexStats.hta` file.

**2. Place it somewhere permanent**

We recommend:
```
C:\YourName\Tools\HexStats.hta
```
Avoid keeping it on the Desktop where it might get accidentally moved or deleted.

**3. Run it**

Double-click `HexStats.hta` — it will appear in the top-right corner of your screen automatically.

**4. Add to startup (optional but recommended)**

Press `Win + R` → type `shell:startup` → hit Enter.
Drop a **shortcut** to `HexStats.hta` into that folder.
It will now launch automatically every time you log in.

---

## 🔓 Open Source — Clone It, Break It, Make It Yours

HexStats is fully open source under the **MIT License**. That means you are free to:

- ✅ Clone and run it for personal use
- ✅ Fork it and build your own version
- ✅ Edit the colors, layout, and stats to fit your setup
- ✅ Redistribute your modified version
- ✅ Use it as a base for your own widget projects

This project was built with the belief that good tools should be shared. If you make something cool with it, we'd love to see it — open a PR, drop an issue, or just share it with the world. 🖤

```bash
git clone https://github.com/YOUR_USERNAME/HexStats.git
```

---

## 🗂 Repository Structure

```
HexStats/
├── README.md
├── LICENSE
├── CHANGELOG.md
└── releases/
    ├── v0.1.0/
    │   └── HexStats.hta
    ├── v1.0.0/
    │   └── HexStats.hta
    └── v1.2.0/
        └── HexStats.hta
```

---

## 🛠 Customization Tips

Want to make it your own? Here are the key things to change:

**Colors** — find these CSS variables in the `<style>` block:
```css
/* Primary accent — change this to your color */
color: #FF69B4;
background-color: #FF69B4;

/* Background */
background: #0c0810;

/* Warning threshold color */
#da5bff  /* purple  — triggers at 55% */
#ff4466  /* red     — triggers at 80% */
```

**Poll rate** — how often stats refresh (default 2 seconds):
```javascript
setInterval("updateStats()", 2000); /* change 2000 to any ms value */
```

**Window position** — top-right by default:
```javascript
window.moveTo(screen.width - 268, 40); /* adjust to taste */
```

**Window size:**
```javascript
window.resizeTo(248, 258);
```

---

## 📦 Release History

See [CHANGELOG.md](./CHANGELOG.md) for the full version history.

| Version | Highlights |
|---|---|
| v1.2.0 | SVG icons, footer, spacing fixes, v1.0.0 bug fixes |
| v1.0.0 | Disk C:, Uptime, Network speed, memory leak fix, pure JS rewrite |
| v0.1.0 | Initial release — CPU & RAM tracking |

---

## 📄 License

MIT License — see [LICENSE](./LICENSE) for full details.

---

<div align="center">

*Crafted with 🖤 by [Anysti LLC](https://anysti.me)*

*© 2026 Anysti LLC*

</div>
