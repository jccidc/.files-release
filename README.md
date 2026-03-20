# .files

A modern Windows file explorer replacement built with Tauri v2. Fast, lightweight, and packed with features that Windows Explorer should have had years ago.

**4.1 MB installer. ~35 MB RAM. No Electron.**

![Demo](demo-v3.gif)

---

## Install

Download the latest `.files_0.1.0_x64-setup.exe` from [Releases](https://github.com/jccidc/.files-release/releases) and run it.

**Requirements:**
- Windows 10/11 (64-bit)
- WebView2 Runtime (pre-installed on Windows 10 21H2+ and all Windows 11)

No other dependencies. No admin rights needed for per-user install.

---

## Screenshots

### This PC View
Drive capacity bars, folder shortcuts, network -- all at a glance.

![This PC](this-pc.png)

### File Browser
Rainbow folders, file counts, natural sort, breadcrumb navigation.

![File List](file-list.png)

### Breadcrumb Dropdown Navigation
Click the dropdown arrow on any breadcrumb segment to see sibling folders and jump directly.

![Breadcrumb Dropdown](breadcrumb-dropdown.png)

### Inline Peek
Expand folders in-place without navigating away.

![Peek](peek-expand.png)

### Context Menu with File Tags
Right-click context menu with tag submenu -- mark files as Important, Archive, Favorite, Private, Done, In Progress, or Pinned. Tags show as colored icons in a dedicated column.

![Context Menu Tags](context-menu-tags.png)

![Context Menu Tags v2](context-menu-tags-v2.png)

### File Age Coloring
Date columns color-coded by age -- green for today, cyan for this week, fading to gray for older files. Hover the column header for the color legend.

![Age Color Legend](age-color-legend.png)

### 12 Themes + Full Customization
Dark, light, high contrast, Dracula, Nord, Catppuccin, Synthwave, Cyberpunk, and more. Custom theme creator, accent colors, window effects (Mica, Acrylic).

![Settings](settings-themes.png)

### Split Panes
Side-by-side browsing with independent tabs per pane.

![Split Panes](split-panes.png)

### Integrated Terminal
Full PowerShell PTY -- run Claude Code, git, npm, anything. First-class tab alongside explorer.

![Terminal](terminal.png)

### Claude Theme + Widgets
Custom Claude theme, flip clock, live weather, Spotify controls, system stats, disk space -- all configurable.

![Claude Theme](claude-theme.png)

### Full Layout
Bible verse marquee, draggable titlebar widgets, footer widget bar with Spotify + system stats.

![Full Layout](full-layout.png)

### Context Menu
Open With, Compress to ZIP/7z/TAR, Extract, Create Shortcut, Properties, Tags, New Folder -- everything you'd expect.

![Context Menu](context-menu.png)

### Grid View + Quick Preview
Grid mode with colorful file icons. Press Space for instant file preview overlay.

![Grid View](grid-view-v2.png)

### In-App Properties
File properties with size, dates, deep folder stats, and attribute toggles (Read-only, Hidden, System).

![Properties](properties-panel.png)

### Treemap View
Disk space visualization -- rectangles sized proportionally to file size. Color gradient from blue (tiny) through green/yellow to red (massive). Click to drill into folders.

![Treemap](treemap.png)

### Miller Columns
macOS-style column navigation -- each folder opens as a new column to the right. See your full path at a glance.

![Miller Columns](miller-columns.png)

### Gallery View
Large preview of selected file with horizontal thumbnail strip for scrubbing.

![Gallery](gallery-view.png)

### Tiles View
Medium icons with metadata (type, size, date) beside each item.

![Tiles](tiles-view.png)

### Flat View
Every file from all subfolders in one searchable list. 1669 files at a glance.

![Flat View](flat-view.png)

---

## Features

### Core Explorer
- Tabbed browsing with split panels (horizontal/vertical)
- List and grid views with sortable, resizable, reorderable, show/hide columns
- Group files by type, extension, size, or date
- Inline folder peek (expand folders in-place without navigating)
- Breadcrumb path bar with click-to-navigate, dropdown sibling navigation, and editable path input (Ctrl+L)
- Natural sort order (file2 before file10)
- Virtual scrolling for large directories
- File search with fuzzy matching (Ctrl+P)
- 7 view modes: List, Grid, Miller Columns, Gallery, Tiles, Flat, Treemap
- Treemap: disk space visualization with size-based color gradient
- Miller Columns: macOS-style column navigation
- Gallery: large preview + thumbnail strip
- Flat View: recursive file listing across all subfolders
- Folder sizes calculated and shown inline in Size column
- File age coloring: green (today), cyan (week), fading to gray for older files, with color legend tooltip
- Accessed column with age coloring
- Draggable column headers with persisted order
- File status tags (Important, Archive, Favorite, Private, Done, In Progress, Pinned) with icon column and filtering
- Batch rename with preview
- Type-ahead selection (start typing to jump to matching file)
- Middle-click folder opens in new tab
- Recent files and folders tracking
- Daily NASB 1977 Bible verse scrolling in titlebar (366 verses, non-removable)

### Titlebar & Footer Widgets
- Configurable widget system -- place widgets in titlebar or footer
- Draggable widget reordering with grip handles
- Flip clock with retro digit-flip animation (12h/24h)
- Live weather (auto-detect by IP or set ZIP code, F/C toggle)
- Spotify now-playing with scrolling track info + prev/pause/next controls
- System stats: live CPU %, RAM usage, battery %
- Disk space: mini capacity bars per drive
- Claude theme: warm terracotta accent on dark brown
- Widget visibility toggles in Settings > Explorer

### Clipboard & Drag-Drop
- Full system clipboard integration (copy/paste between .files and Windows Explorer)
- Native drag-and-drop to external apps (email, Slack, Explorer)
- Drop files from other apps into .files
- Cross-pane drag-and-drop between split panels
- Ctrl+C/X/V keyboard shortcuts

### File Operations
- Copy/move with progress bars and cancel
- Conflict resolution dialog (Skip / Replace / Keep Both)
- Undo/redo (Ctrl+Z) for copy, move, and create operations
- Multi-format archive support: compress/extract ZIP, 7z, TAR, GZ, BZ2
- Create shortcuts (.lnk)
- Permanent delete (Shift+Delete) or Recycle Bin (Delete)
- Recycle Bin browsing, restore, and empty
- Create symbolic links / junctions

### Context Menu
- Open, Open With, Cut, Copy, Paste, Rename, Delete
- Compress to ZIP/7z/TAR, Extract All (for archive files)
- Create Shortcut
- Copy Name, Copy Path, Show in Explorer
- Pin to Quick Access
- Tag as... (Important, Archive, Favorite, Private, Done, In Progress, Pinned)
- Properties (in-app panel with file attributes)
- New Folder (Ctrl+Shift+N), New Text File

### This PC View
- Drive cards with capacity bars (instant load via Win32 API)
- Folder shortcuts: Desktop, Documents, Downloads, Pictures, Music, Videos
- Network browser link

### Sidebar
- Home, Folders, This PC, Recent, Quick Access, Sources, Cloud, Git
- Custom SVG icons per folder type
- Configurable folder visibility in Settings > Explorer
- Pin folders to Quick Access (drag to reorder)
- Expandable folder trees with lazy loading
- Drive eject button for removable media
- Hot-plug detection
- Draggable, reorderable sections
- Sidebar right-click: Open in Terminal, New Folder, Compress, Properties

### Properties & Search
- In-app Properties panel (size, dates, file/folder count)
- File attribute toggles (Read-only, Hidden, System)
- Drive properties for drive roots
- Search with type/size/date filters
- Content search (grep-like, searches inside text files)

### Built-in Terminal
- Full PowerShell terminal tab (real PTY via portable-pty)
- Multiple terminal tabs alongside explorer tabs
- Runs Claude Code, git, npm, anything PowerShell can

### File Preview
- Image preview with zoom/pan (PNG, JPG, GIF, SVG, WebP)
- PDF preview with page navigation and zoom
- DOCX preview, XLSX/CSV with sheet tabs
- Markdown preview (GitHub-flavored)
- Code/text preview with syntax highlighting
- Video/audio playback
- Space bar quick preview overlay

### Git Integration
- Full sidebar git panel: branch switcher, stage/unstage, commit, push/pull
- Inline diff viewer with add/remove highlighting
- Git status icons on file rows
- Clone repos from GitHub directly

### Cloud Sources
- GitHub repo browser with PAT authentication
- Auto-detect OneDrive and Google Drive local mounts

### Theming & Customization
- 13 built-in themes + custom theme creator (copies active theme as starting point)
- Window effects: Mica, Mica Alt, Acrylic, Tabbed
- Background patterns, opacity controls, glow effects, neon mode
- Rainbow folders, gradient accents, 3 density modes
- Custom CSS injection, icon themes, font picker

### Windows Integration
- Set as default folder handler
- System tray, single instance, F11 fullscreen
- NSIS installer

### Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| Ctrl+A | Select all |
| Ctrl+C / X / V | Copy / Cut / Paste (system clipboard) |
| Ctrl+Z | Undo |
| Ctrl+T | New tab |
| Ctrl+Shift+T | New terminal |
| Ctrl+Shift+N | New folder |
| Ctrl+W | Close tab |
| Ctrl+L | Edit path |
| Ctrl+B | Toggle sidebar |
| Ctrl+Shift+P | Toggle preview |
| Ctrl+Shift+D / S | Split right / down |
| Ctrl+Shift+C | Copy path |
| Space | Quick preview |
| F2 | Rename |
| F5 | Refresh |
| F11 | Fullscreen |
| Delete | Recycle Bin |
| Shift+Delete | Permanent delete |

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Runtime | Tauri v2 (WebView2) |
| Backend | Rust |
| Frontend | React 19 + TypeScript + Vite |
| State | Zustand |
| Terminal | xterm.js + portable-pty |
| Git | libgit2 (git2 crate) |
| Clipboard | clipboard-win + PowerShell |
| Drag-Drop | tauri-plugin-drag |
| Installer | NSIS |

**Binary:** 9.3 MB exe, 4.1 MB installer | **Memory:** ~35 MB baseline

---

## License

MIT

---

Built by [Jimmy CrakCrn](https://jimmycc.com) | [GitHub](https://github.com/jccidc)
