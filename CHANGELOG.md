# Changelog

All notable changes to HexStats are documented here.

This project follows [Semantic Versioning](https://semver.org/):
- **MAJOR** — breaking changes or full rewrites
- **MINOR** — new features or significant improvements
- **PATCH** — bug fixes and small tweaks

---

## [v1.2.0] — 2026-06-03 *(Planned)*
> *"The court gets its crests."*

### Added
- SVG vector icons for CPU, RAM, and Disk C: stat rows
- Footer bar with `© 2026 Anysti LLC` and version number
- Net speed arrows now color-coded — teal for download, pink for upload

### Fixed
- Icon and label text spacing — breathing room between SVG and text
- Window height trimmed to eliminate body color bleed below footer
- `setInterval` corrected to string form for proper VBScript/JS cross-scope calling

---

## [v1.0.0] — 2026-05-27 *(Planned)*
> *"The grimoire grows."*

### Added
- **Disk C:** usage tracking with progress bar
- **Uptime** display (days, hours, minutes since last boot)
- **Network speed** — live download & upload via `Win32_PerfFormattedData_Tcpip_NetworkInterface`
- Frameless window mode (`border="none"`, `caption="no"`) with border outline
- Auto-positioning to top-right corner on launch (`window.moveTo`)
- SVG hex icon and clock icon in header and uptime row

### Changed
- Full rewrite from VBScript to **pure JavaScript** for consistency and maintainability
- WMI connection initialized **once globally** and reused — eliminates memory leak
- All WMI collection handles explicitly nulled after each query cycle
- `CollectGarbage()` called at end of every poll to force JScript engine cleanup
- Color-coded progress bars — pink → purple → red based on load thresholds
- Pulsing live indicator dot in header

### Fixed
- `setInterval` cross-language scope bug — changed from anonymous function wrapper to string evaluation so JScript finds VBScript-defined functions correctly

---

## [v0.1.0] — 2026-05-20
> *"Where it all began."*

### Added
- Initial release of HexStats
- **CPU** usage tracking via `Win32_PerfFormattedData_PerfOS_Processor`
- **RAM** used / total / percentage via `Win32_OperatingSystem`
- Dark background (`#1e1e1e`) with hot pink (`#FF69B4`) stat values
- Auto-refresh every 2 seconds
- Single instance enforcement

---

*Built with 🖤 by [Anysti LLC](https://anysti.me)*
