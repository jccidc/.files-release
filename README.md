# .files

A modern Windows file explorer replacement built with Tauri v2. Fast, lightweight, and packed with features that Windows Explorer should have had years ago.

**3.8 MB installer. ~30 MB RAM. No Electron.**

---

## Install

Download the latest `.files_x64-setup.exe` from [Releases](https://github.com/200df7/.files-release/releases) and run it.

**Requirements:**
- Windows 10/11 (64-bit)
- WebView2 Runtime (pre-installed on Windows 10 21H2+ and all Windows 11)

No other dependencies. No admin rights needed for per-user install.

---

## Screenshots

### Explorer
![Explorer](Exp.png)

### Terminal
![Terminal](term.png)

### Themes & Customization
![Themes](theme.png)

### Git Integration
![Git](git.png)

### Inline Peek
![Scrolling Peek](scrolling%20peek.png)

### Multi-Pane Split
![Multi-Pane](Multipane.png)

---

## Features

### Core Explorer
- Tabbed browsing with split panels (horizontal/vertical)
- List and grid views with sortable, resizable, show/hide columns
- Group files by type, extension, size, or date
- Inline folder peek (expand folders in-place without navigating)
- Breadcrumb path bar with click-to-navigate and editable path input (Ctrl+L)
- Natural sort order (file2 before file10)
- Virtual scrolling for large directories
- Drag and drop (move/copy files, import from desktop)
- Recycle Bin delete (never permanent unless you ask)
- .lnk shortcut resolution (shows target path, folder icon with arrow overlay)
- File search with fuzzy matching (Ctrl+P)
- Batch rename with preview

### Built-in Terminal
- Full PowerShell terminal tab (not a toy -- real PTY via portable-pty)
- Multiple terminal tabs alongside explorer tabs
- Runs Claude Code, git, npm, anything PowerShell can

### File Preview
- Click any file to preview in the side panel or press Space for quick peek
- Image preview with zoom/pan (PNG, JPG, GIF, SVG, WebP)
- PDF preview with page navigation and zoom (pdfjs-dist)
- DOCX preview (mammoth.js rendering)
- XLSX/CSV preview with sheet tabs (SheetJS)
- Markdown preview (rendered GitHub-flavored markdown)
- Code/text preview with word wrap and copy button
- Video/audio playback (native HTML5 player)

### Git Integration
- Full sidebar git panel: branch switcher, stage/unstage, commit, push/pull
- Inline diff viewer with add/remove highlighting
- Git status icons on file rows (modified, staged, untracked, conflict)
- Branch + ahead/behind indicator in status bar
- Context menu: stage, discard, view diff
- Clone repos from GitHub directly

### Cloud Sources
- GitHub repo browser with PAT authentication
- Auto-detect OneDrive and Google Drive local mounts
- Link GitHub repos to local clones for one-click access
- Google Drive .lnk shortcut resolution

### Sidebar
- Draggable, reorderable sections: Sources, Cloud, Quick Access, Git
- Pin folders to Quick Access (drag to reorder, right-click to unpin)
- Expandable folder trees with lazy loading
- Drive eject button for removable media
- Hot-plug detection (plug/unplug USB while running)
- Section order persisted across sessions

### Theming & Customization
- 9 built-in themes (dark, light, high contrast, and more)
- Custom theme creator: smart mode (6 colors) or advanced mode (24 tokens)
- Import/export themes as JSON
- Window transparency with acrylic/mica effects
- Background patterns (dots, grid, noise, gradient, custom image)
- Opacity controls per-region (sidebar, toolbar, terminal)
- Glow effects, cursor trail, animation speed controls
- 3 density modes (compact, comfortable, spacious)
- Font size, UI scale, border radius sliders
- System font picker with live preview
- Custom font import (TTF/OTF/WOFF2)
- Custom CSS injection for full control
- Icon themes (minimal, colorful, monochrome)

### Windows Integration
- "Open with .files" in right-click context menu
- Optional: set as default folder handler (double-click folders opens .files)
- System tray with show/quit (close-to-tray)
- Single instance: opening a second folder adds a tab instead of a new window
- NSIS installer with auto context menu registration

### Keyboard Shortcuts
| Shortcut | Action |
|----------|--------|
| Ctrl+T | New explorer tab |
| Ctrl+Shift+T | New terminal tab |
| Ctrl+W | Close tab |
| Ctrl+L | Edit path bar |
| Ctrl+P | Fuzzy file search |
| Ctrl+B | Toggle sidebar |
| Ctrl+Shift+P | Toggle preview panel |
| Ctrl+Shift+D | Split panel right |
| Ctrl+Shift+S | Split panel down |
| Ctrl+, | Settings |
| Space | Quick preview selected file |
| F5 | Refresh |
| F2 | Rename |
| Delete | Delete to Recycle Bin |
| Alt+Left/Right | Back/Forward |
| Alt+Up | Go to parent folder |

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
| Styling | CSS custom properties (no Tailwind runtime) |
| Installer | NSIS |

**Binary size:** 8.8 MB exe, 3.8 MB installer (NSIS compressed)
**Memory:** ~30 MB baseline
**DLL dependencies:** None shipped -- links only to standard Windows system DLLs + WebView2

---

## License

MIT

---

Built by [Jimmy CrakCrn](https://github.com/200df7)
