# 🗂️ Terminal File Manager

A beautiful, modern TUI file manager with a three-panel layout, command palette, built-in text editor, media inspectors, and powerful tools — all rendered in true color with Nerd Font icons. Designed for Kitty and other modern terminals.

[![Buy Me A Coffee](https://img.shields.io/badge/Buy%20Me%20A%20Coffee-Support-yellow?logo=buy-me-a-coffee)](https://buymeacoffee.com/succinctrecords)

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Python](https://img.shields.io/badge/python-3.6%2B-blue.svg)

## ✨ Features

### 🖥️ Modern Three-Panel Layout
- **Sidebar** (left) — Expandable directory tree rooted at `~` plus Quick Access shortcuts
- **File list** (center) — Color-coded entries with Nerd Font icons, git status indicators, and extension badges
- **Preview pane** (right) — Context-sensitive preview: text content, image thumbnails (Kitty graphics protocol), audio/video metadata, or directory listings
- Toggle panels with `Tab` (sidebar) and `P` (preview) to suit your screen

### 🎨 True-Color Rendering
- Automatic **Kitty terminal detection** for true-color RGB and inline image previews
- Gradient selection bar, themed panels, and design-token-based color system
- Graceful fallback to 256-color mode on other terminals
- Nerd Font icons throughout (file types, git status, UI chrome)

### ⌨️ Command Palette
- Press **`:`** to open the **command palette** — a VS Code-style floating overlay that lets you search and execute any action by name
- Press **`/`** to open **file search** — fuzzy-filter files in the current directory and jump to them instantly

### 🎮 Interactive Navigation
- Arrow key navigation with smooth scrolling and visual scrollbar
- Quick jumps to home (`h`), root (`r`), or bookmarked locations (`b`)
- Focus sidebar with `[`, return to files with `]` or `Esc`
- Expand/collapse tree nodes with `→`/`←`

### 📁 File Management
- **Mark files** with `Space`, mark all with `a`, unmark with `u`
- **Copy** (`c`), **Cut** (`x`), **Paste** (`v`) with conflict resolution
- **Delete** (`d`) with confirmation prompt
- **Create** (`n`) new files or complex folder structures
- **Rename** (`R`) in-place
- **Bulk operations** (`o`) — copy/move/delete all or marked files

### 🛠️ Tools Menu
Press **`t`** to open the tools menu with 13 built-in tools:

| # | Tool | Description |
|---|------|-------------|
| 1 | Convert Audio to FLAC | Intelligent conversion with metadata/artwork preservation |
| 2 | Convert Images | Batch conversion via ImageMagick (JPG, PNG, WebP, AVIF, etc.) |
| 3 | Extract Archives | zip, tar, gz, bz2, xz, rar, 7z via `extractfile` |
| 4 | Extract & Convert | Extract archives then convert audio to FLAC |
| 5 | ISO to GOD | Xbox 360 ISO converter via `iso2god-rs` |
| 6 | Sort Files | Organize by type, extension, size, date, or letter |
| 7 | Play Video | Terminal playback via buddy or ncplayer |
| 8 | Browse Images | Image browser via `pixel-index` |
| 9 | Permission Manager | Interactive permissions with human-readable presets |
| e | Essentia Tagger | ML-powered genre/mood tagging |
| t | File Transfer | Dual-pane file browser/transfer tool |
| 0 | Run Command | Execute any shell command in current directory |
| s | Video Player Settings | Choose auto/buddy/ncplayer |

### 📝 Built-in Text Editor
- Syntax highlighting for Python, JSON, and more
- Line numbers, cursor position tracking, modification indicator
- Clipboard: Select All (`Ctrl+A`), Copy Line (`Ctrl+C`), Paste (`Ctrl+V`)
- Save (`Ctrl+S`), Quit (`Ctrl+Q`), Force Quit (`Ctrl+X`)

### 🔍 Media Inspectors
- **Audio Inspector** — ffprobe analysis with quality score (0-100), codec info, sample rate, bitrate, comparison mode
- **Video Inspector** — Resolution, codec, bitrate, FPS scoring with comparison mode
- **Image Inspector** — Megapixels, bit depth, compression ratio, comparison mode
- Press `Enter` on any media file to inspect; press `c` inside an inspector to compare two files

### 🔖 Bookmarks
- Save directories with custom names, stored in `~/.filemanager_config.json`
- Quick access from anywhere with `b`

### 🔍 Empty Folder Finder
- Press `f` to scan for empty and near-empty folders
- Inspect, mark, and bulk-delete

### 🐙 Git Integration
- Per-file git status indicators (modified, added, untracked, etc.)
- Branch name and dirty flag in the header bar

---

## ⌨️ Keyboard Reference

### Main File Manager

| Key | Action |
|-----|--------|
| `↑` / `↓` | Navigate files |
| `Enter` | Open directory / file in appropriate viewer |
| `Backspace` | Go to parent directory |
| `h` | Jump to home directory |
| `r` | Jump to root directory |
| `?` | Toggle help display |
| `q` | Quit |

### Panels

| Key | Action |
|-----|--------|
| `Tab` | Toggle sidebar visibility |
| `P` | Toggle preview pane visibility |
| `[` | Focus sidebar |
| `]` / `Esc` | Return focus to file list |

### Sidebar (when focused)

| Key | Action |
|-----|--------|
| `↑` / `↓` | Navigate tree items |
| `Enter` | Open/expand directory or quick access item |
| `→` | Expand tree node |
| `←` | Collapse tree node |
| `]` / `Esc` | Return to file list |

### File Marking & Operations

| Key | Action |
|-----|--------|
| `Space` | Toggle mark on current file |
| `a` | Mark all files |
| `u` | Unmark all files |
| `c` | Copy marked files (or current) |
| `x` | Cut marked files (or current) |
| `v` | Paste from clipboard |
| `d` | Delete marked files (or current) |
| `n` | Create new file (`f`) or directory (`d`) |
| `R` | Rename current item |
| `o` | Open bulk operations menu |

### Menus & Palette

| Key | Action |
|-----|--------|
| `:` | Open command palette |
| `/` | Open file search |
| `t` | Open tools menu |
| `b` | Open bookmarks menu |

### Direct Tool Shortcuts

| Key | Action |
|-----|--------|
| `p` | Fix permissions |
| `e` | Extract archives |
| `f` | Find empty folders |
| `V` | Play selected video |
| `I` | Browse images with pixel-index |

### Operations Menu (via `o`)

| Key | Action |
|-----|--------|
| `1` | Copy All Files |
| `2` | Move All Files |
| `3` | Delete All Files |
| `4` | Copy Marked Files |
| `5` | Move Marked Files |
| `6` | Delete Marked Files |
| `7` | Mark All Files |
| `8` | Unmark All Files |
| `q` | Cancel |

### Tools Menu (via `t`)

| Key | Action |
|-----|--------|
| `1` | Convert Audio to FLAC |
| `2` | Convert Images |
| `3` | Extract Archives |
| `4` | Extract & Convert |
| `5` | ISO to GOD |
| `6` | Sort Files |
| `7` | Play Video |
| `8` | Browse Images |
| `9` | Permission Manager |
| `e` | Essentia Tagger |
| `t` | File Transfer |
| `0` | Run Command |
| `s` | Video Player Settings |
| `q` | Cancel |

### Text Editor (opens on text files)

| Key | Action |
|-----|--------|
| `Ctrl+S` | Save file |
| `Ctrl+Q` | Quit (warns if unsaved) |
| `Ctrl+X` | Force quit without saving |
| `Ctrl+A` | Select all (copy to clipboard) |
| `Ctrl+C` | Copy current line |
| `Ctrl+V` | Paste from clipboard |
| `Ctrl+D` | Delete all text |
| `↑` / `↓` / `←` / `→` | Navigate cursor |
| `Page Up` / `Page Down` | Scroll by page |
| `Home` / `End` | Jump to line start/end |
| `Tab` | Insert 4 spaces |
| `Enter` | New line |
| `Backspace` / `Delete` | Delete character |

### Media Inspectors (audio, video, image)

| Key | Action |
|-----|--------|
| `c` | Start/clear comparison mode |
| `q` / `Esc` | Exit inspector |
| `↑` / `↓` | Navigate files (comparison browse) |
| `Enter` | Select file for comparison |
| `Backspace` | Go up directory (comparison browse) |

### Create Folder Structure (via `n` → `d`)

| Key | Action |
|-----|--------|
| `a` | Add child to root folder |
| `s` | Add child to specific folder |
| `c` | Create the structure |
| `q` / `Esc` | Cancel |

### Find Empty Folders (via `f`)

| Key | Action |
|-----|--------|
| `↑` / `↓` | Navigate folder list |
| `Space` | Toggle mark |
| `i` | Inspect folder details |
| `d` | Delete selected folder |
| `D` | Delete all marked folders |
| `E` | Delete ALL empty folders |
| `N` | Delete ALL near-empty folders |
| `q` | Return |

---

## 📋 Requirements

- **Python 3.6+**
- **Linux/Unix** system
- Terminal with **color support** (Kitty recommended for full features)
- **ffmpeg/ffprobe** (for media inspectors) — `sudo apt install ffmpeg`
- **ImageMagick** (for image conversion) — `sudo apt install imagemagick`
- **essentia-tensorflow** + **mutagen** (optional, for Essentia Tagger) — `pip install essentia-tensorflow mutagen`
- **Nerd Font** (recommended) for icons — any [Nerd Font](https://www.nerdfonts.com/)

## 🚀 Installation

### Quick Install

```bash
# 1. Clone the repository
git clone https://github.com/WB2024/WBs-Beautiful-TUI-Filemanager.git
cd WBs-Beautiful-TUI-Filemanager

# 2. Copy all utilities to system path
sudo cp filemanager extractfile fixperms audio-to-flac extract-and-convert image-convert iso2god file-sort video-player essentia-tagger file-transfer /usr/local/bin/
sudo chmod +x /usr/local/bin/filemanager /usr/local/bin/extractfile /usr/local/bin/fixperms /usr/local/bin/audio-to-flac /usr/local/bin/extract-and-convert /usr/local/bin/image-convert /usr/local/bin/iso2god /usr/local/bin/file-sort /usr/local/bin/video-player /usr/local/bin/essentia-tagger /usr/local/bin/file-transfer

# 3. Run it!
filemanager
```

**What gets installed:**

| Utility | Description |
|---------|-------------|
| `filemanager` | Main TUI file manager |
| `extractfile` | Archive extraction (zip, tar, rar, 7z, etc.) |
| `fixperms` | Interactive permission manager |
| `audio-to-flac` | Audio conversion to FLAC |
| `extract-and-convert` | Extract archives + convert audio |
| `image-convert` | Image format conversion (ImageMagick) |
| `iso2god` | Xbox/360 ISO to GOD converter |
| `file-sort` | File organization by type/size/date |
| `video-player` | Terminal video player (buddy/ncplayer) |
| `essentia-tagger` | ML audio genre/mood tagger |
| `file-transfer` | Dual-pane file transfer tool |

### Manual Installation

```bash
# Download all scripts
for tool in filemanager extractfile fixperms audio-to-flac extract-and-convert image-convert iso2god file-sort video-player essentia-tagger file-transfer; do
  wget "https://raw.githubusercontent.com/WB2024/WBs-Beautiful-TUI-Filemanager/main/$tool" -O "$tool"
done

# Make executable and install
chmod +x filemanager extractfile fixperms audio-to-flac extract-and-convert image-convert iso2god file-sort video-player essentia-tagger file-transfer
sudo mv filemanager extractfile fixperms audio-to-flac extract-and-convert image-convert iso2god file-sort video-player essentia-tagger file-transfer /usr/local/bin/
```

### Verify Installation

```bash
which filemanager extractfile fixperms audio-to-flac extract-and-convert image-convert iso2god file-sort video-player essentia-tagger file-transfer
```

## 🔄 Updating

```bash
cd /path/to/WBs-Beautiful-TUI-Filemanager
git pull origin main
sudo cp filemanager extractfile fixperms audio-to-flac extract-and-convert image-convert iso2god file-sort video-player essentia-tagger file-transfer /usr/local/bin/
sudo chmod +x /usr/local/bin/filemanager /usr/local/bin/extractfile /usr/local/bin/fixperms /usr/local/bin/audio-to-flac /usr/local/bin/extract-and-convert /usr/local/bin/image-convert /usr/local/bin/iso2god /usr/local/bin/file-sort /usr/local/bin/video-player /usr/local/bin/essentia-tagger /usr/local/bin/file-transfer
```

Your bookmarks and config (`~/.filemanager_config.json`) are preserved during updates.

---

## 📖 Detailed Feature Guide

### Command Palette

Press **`:`** to open the command palette. Type to filter commands, use `↑`/`↓` to select, `Enter` to execute, `Esc` to close.

Available commands:
- Copy / Cut / Paste / Delete / Rename / New file or folder
- Bookmarks / Tools menu / Fix permissions
- Find empty folders / Extract archives
- Toggle help / Quit

Press **`/`** for file search mode — fuzzy-filters all entries in the current directory.

### Three-Panel Layout

The interface has three panels. All are independently togglable:

- **Sidebar** (`Tab` to toggle, `[` to focus) — Shows an expandable directory tree starting from `~` and Quick Access shortcuts. Navigate with arrow keys, expand/collapse with `→`/`←`.
- **File list** (always visible) — The main panel. Shows entries with icons, git indicators, file type badges, permissions, and sizes. The selected row has a horizontal gradient highlight.
- **Preview pane** (`P` to toggle) — Shows context-sensitive previews: text file contents, image thumbnails (via Kitty graphics protocol), audio metadata, video info, or directory listings.

### Bookmarks

| Action | How |
|--------|-----|
| Open bookmarks | Press `b` |
| Add bookmark | `b` → select "Add current directory" → enter a name |
| Jump to bookmark | `b` → select bookmark |
| Remove bookmark | `b` → select "Remove a bookmark" → enter name |

Bookmarks are stored in `~/.filemanager_config.json`.

### Audio Quality Inspector

Press `Enter` on any audio file (MP3, FLAC, WAV, M4A, OGG, etc.) to open the inspector.

**Metrics shown:** Quality score (0-100), file size, duration, format, codec, sample rate, bitrate, bit depth, channels.

**Quality ratings:** Exceptional (90-100), Excellent (75-89), Very Good (60-74), Good (45-59), Fair (30-44), Poor (0-29).

**Comparison:** Press `c` to start comparison mode → browse to a second file → press `Enter`. Side-by-side analysis with winner recommendation.

### Video Quality Inspector

Press `Enter` on any video file (MP4, MKV, AVI, MOV, WebM, etc.).

**Metrics shown:** Quality score (0-100), resolution (8K/4K/1080p/720p/SD), codec (AV1/HEVC/H.264/VP9), bitrate, FPS, audio info.

**Scoring:** Resolution (35pts) + Bitrate (30pts) + Codec (20pts) + FPS (15pts).

**Comparison:** Same as audio — press `c` to compare two files.

### Image Quality Inspector

Press `Enter` on any image file (JPG, PNG, WebP, TIFF, HEIC, RAW, etc.).

**Metrics shown:** Quality score (0-100), dimensions, megapixels, aspect ratio, codec, lossless detection, bit depth, color space, alpha channel, compression ratio.

**Comparison:** Same as audio/video — press `c` to compare.

### Permission Manager

Access via `p` or Tools menu → `9`. Uses the `fixperms` utility for interactive permission management with human-readable presets like "Owner Only - Completely Private" instead of raw numbers.

Features: inspect permissions, inspect contents, 15 permission presets, owner/group selection, scope control, quick fix mode.

### Archive Extraction

Press `e` or Tools menu → `3`. Select individual archives or "Extract All". Supports zip, tar, gz, bz2, xz, rar, 7z.

### Empty Folder Finder

Press `f`. Scans for empty folders (no files at any depth) and near-empty folders (<10MB). Inspect details with `i`, delete individually or in bulk.

### Audio to FLAC Converter

Tools menu → `1` or run `audio-to-flac` standalone. Intelligent codec detection, configurable compression (0-8), metadata/artwork preservation, optional cleanup.

### Image Converter

Tools menu → `2` or run `image-convert` standalone. Batch conversion via ImageMagick. Output formats: JPG, PNG, WebP, GIF, BMP, TIFF, AVIF. Configurable quality.

### Extract and Convert

Tools menu → `4` or run `extract-and-convert` standalone. Extracts archives then converts audio to FLAC. CLI flags: `--delete-audio` (`-d`), `--delete-archive` (`-a`), `--delete-all`.

### File Sort

Tools menu → `6` or run `file-sort` standalone. Organizes files by type, extension, size, date, or first letter.

### Video Player

Press `V` on a video file, or Tools menu → `7`. Uses buddy or ncplayer. Configure preferred player via Tools menu → `s`.

### Essentia Tagger

Tools menu → `e` or run `essentia-tagger` standalone. ML-powered genre classification (400 Discogs classes) and mood tagging (MTG Jamendo). Requires `essentia-tensorflow` and `mutagen`.

---

## 📦 Included Utilities

All utilities can be used standalone from the command line:

```bash
extractfile archive.zip              # Extract specific archive
extractfile                          # Extract all archives in current directory
fixperms                             # Interactive permission manager
fixperms /var/www                    # Manage specific directory
audio-to-flac                        # Convert audio to FLAC
extract-and-convert                  # Extract + convert workflow
extract-and-convert -da              # Delete archives and originals
image-convert                        # Batch image conversion
iso2god                              # ISO to GOD conversion
file-sort                            # Interactive file sorting
video-player video.mp4               # Play video in terminal
essentia-tagger                      # ML audio tagging
essentia-tagger --dry-run            # Analyze without writing
file-transfer                        # Dual-pane file browser
```

**Archive format dependencies:**
- RAR files: `sudo apt install unrar`
- 7z files: `sudo apt install p7zip-full`

---

## 🔧 Configuration

Settings are stored in `~/.filemanager_config.json`:

```json
{
  "bookmarks": {
    "projects": "/home/user/projects",
    "downloads": "/home/user/Downloads"
  },
  "video_player": "auto"
}
```

- `bookmarks` — Named directory shortcuts (managed via `b`)
- `video_player` — `"auto"` (default), `"buddy"`, or `"ncplayer"`

---

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

MIT License — see [LICENSE](LICENSE).

## 🐛 Bug Reports

Open an issue with: your OS, Python version, steps to reproduce, expected vs actual behavior, and any error messages.

## ☕ Support

[![Buy Me A Coffee](https://img.shields.io/badge/Buy%20Me%20A%20Coffee-Support-yellow?logo=buy-me-a-coffee)](https://buymeacoffee.com/succinctrecords)

## 📞 Contact

- GitHub: [@WB2024](https://github.com/WB2024)
- Buy Me A Coffee: [succinctrecords](https://buymeacoffee.com/succinctrecords)

---

**Made with ❤️ for the terminal**
