# 🗂️ Terminal File Manager

A beautiful, interactive terminal-based file manager with a built-in text editor, audio & video quality inspectors, and powerful tools for Linux/Unix systems. Navigate your filesystem with arrow keys, edit files with syntax highlighting, inspect audio and video quality, compare media files, manage permissions, extract archives, and analyze disk usage - all from a gorgeous TUI (Terminal User Interface).

[![Buy Me A Coffee](https://img.shields.io/badge/Buy%20Me%20A%20Coffee-Support-yellow?logo=buy-me-a-coffee)](https://buymeacoffee.com/succinctrecords)

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Python](https://img.shields.io/badge/python-3.6%2B-blue.svg)

## ✨ Features

### 🎮 Interactive Navigation
- **Arrow key navigation** - Browse files and folders with ↑/↓ keys
- **Color-coded files** - Different colors for audio 🎵, video 🎬, images 🖼️, archives 📦, code 💻, and more
- **Smart scrolling** - Smooth scrolling with visual scrollbar
- **Quick jumps** - Instantly jump to home, root, or bookmarked locations
- **File information** - Press Enter on files to view name and size

### 📁 File Management Operations
- **File Selection System**
  - `Space` - Toggle mark on current file (moves to next)
  - `a` - Mark all files in current folder
  - `u` - Unmark all selected files
  - Visual markers `[*]` show selected files
  - Selection count displayed in status bar
- **Copy, Cut & Paste**
  - `c` - Copy marked files (or current file if none marked)
  - `x` - Cut marked files (or current file if none marked)
  - `v` - Paste files from clipboard to current directory
  - Clipboard status shown in footer
  - Automatic rename on conflict (appends _1, _2, etc.)
- **Delete**
  - `d` - Delete marked files or current file
  - Confirmation prompt before deletion
  - Works on files and folders
- **Create & Rename**
  - `n` - Create new file or folder
  - `R` - Rename current file or folder
- **Bulk Operations Menu** (`o`)
  - Copy All Files - Copy all files in folder
  - Move All Files - Move all files in folder
  - Delete All Files - Delete all files (with confirmation)
  - Copy/Move/Delete Marked Files
  - Mark/Unmark All Files

### 📝 Built-in Text Editor
- **Syntax highlighting** for Python, JSON, and more
- **Line numbers** with current line highlighting
- **Cursor position tracking** (line/column display)
- **Full editing capabilities** - Insert, delete, newlines, navigation
- **Save functionality** with modification tracking (Ctrl+S)
- **Smart quit** - Warns if unsaved changes (Ctrl+Q)
- **Force quit** without saving (Ctrl+X)
- **Page Up/Down** support for large files
- **Advanced features**:
  - **Select All** (Ctrl+A) - Copy entire file to clipboard
  - **Copy Line** (Ctrl+C) - Copy current line
  - **Paste** (Ctrl+V) - Paste from clipboard
  - **Delete All** (Ctrl+D) - Clear entire file
- **Auto-detection** of text files (supports 50+ file extensions)
- **Home/End** keys for line navigation
- **Tab support** (4 spaces)

### 🎵 Audio Quality Inspector
- **Professional audio analysis** using ffprobe
- **Press Enter on audio files** to inspect quality
- **Comprehensive metrics**:
  - File size and duration
  - Format and codec information
  - Sample rate (Hz)
  - Bitrate (kbps)
  - Bit depth
  - Channels (stereo/mono)
  - Quality score (0-100)
- **Quality indicators**:
  - Color-coded ratings (Exceptional, Excellent, Very Good, Good, Fair, Poor)
  - Lossless format detection (FLAC, ALAC, WAV, APE)
  - High-resolution audio highlighting
- **File comparison mode**:
  - Compare two audio files side-by-side
  - Quality score comparison
  - Clear winner indication
  - Recommendation on which file to keep
  - Perfect for finding the best version of duplicate songs
- **Supported formats**: MP3, FLAC, WAV, M4A, AAC, OGG, Opus, WMA, APE, ALAC, AIFF, DSD
- **Easy navigation**: Browse to second file without leaving inspector

### 🎬 Video Quality Inspector
- **Professional video analysis** using ffprobe
- **Press Enter on video files** to inspect quality
- **Comprehensive metrics**:
  - File size and duration
  - Resolution (8K, 4K, 1080p, 720p, etc.)
  - Exact dimensions (pixels)
  - Video codec (AV1, HEVC, H.264, VP9, etc.)
  - Video bitrate (Mbps)
  - Frame rate (fps)
  - Audio codec and bitrate
  - Quality score (0-100)
- **Quality indicators**:
  - Color-coded ratings (Exceptional, Excellent, Very Good, Good, Fair, Poor)
  - Modern codec detection (AV1, HEVC/H.265)
  - High resolution highlighting (4K/8K)
  - High frame rate detection (60fps/120fps)
- **File comparison mode**:
  - Compare two video files side-by-side
  - Quality score comparison
  - Clear winner indication
  - Recommendation on which file to keep
  - Perfect for comparing different encodings or resolutions
- **Supported formats**: MP4, MKV, AVI, MOV, WMV, FLV, WebM, M4V, MPG, MPEG, 3GP, OGV, TS, M2TS, VOB, DivX, XviD, and more
- **Easy navigation**: Browse to second file without leaving inspector

### �️ Image Quality Inspector
- **Professional image analysis** using ffprobe
- **Press Enter on image files** to inspect quality
- **Comprehensive metrics**:
  - File size
  - Dimensions (width x height)
  - Megapixels
  - Resolution category (Ultra High, Very High, High, Medium, Low)
  - Aspect ratio (16:9, 4:3, 3:2, etc.)
  - Format/codec (PNG, JPEG, WebP, TIFF, etc.)
  - Lossless vs Lossy detection
  - Bit depth (8-bit, 10-bit, 16-bit)
  - Color space (RGB, YUV, Grayscale)
  - Alpha channel detection
  - Compression ratio
  - Quality score (0-100)
- **Quality indicators**:
  - Color-coded ratings (Exceptional, Excellent, Very Good, Good, Fair, Poor)
  - Lossless format highlighting (PNG, TIFF, BMP)
  - High resolution highlighting (12+ MP)
  - High bit depth highlighting (16-bit)
- **File comparison mode**:
  - Compare two images side-by-side
  - Quality score comparison
  - Clear winner indication
  - Recommendation on which file to keep
  - Perfect for finding the best version of duplicate images
- **Supported formats**: JPG, JPEG, PNG, GIF, BMP, TIFF, WebP, SVG, ICO, HEIC, HEIF, AVIF, RAW, CR2, NEF, ARW, DNG, PSD, XCF
- **Easy navigation**: Browse to second file without leaving inspector

### �🔖 Bookmark System
- **Save favorite directories** with custom names
- **Quick access** to frequently used locations
- **Persistent storage** - Bookmarks saved to `~/.filemanager_config.json`
- Perfect for long paths like `/srv/dev-disk-by-uuid-...`

### 🛠️ Built-in Tools

#### 🔓 Permission Manager
- **Inspect permissions** - View current permissions and ownership with plain-English explanations
- **Inspect contents** - See permissions of every file and folder inside a directory
- **Human-readable permission presets** - Choose access levels like "Owner Only - Completely Private" instead of memorizing numbers like 700
- **Change owner** - Pick from a list of system users
- **Change group** - Pick from a list of system groups
- **Set everything at once** - Permissions, owner, and group in one workflow
- **Quick fix** - One-click Full Access (777) for the original behavior
- **Scope control** - Apply to just the folder, or recursively to everything inside
- Access from file manager with `p` key, or Tools menu → `[9]`

#### 📦 Archive Extractor
- Extract **zip, tar, gz, bz2, xz, rar, 7z** archives
- Select individual files or extract all
- Uses the included `extractfile` utility
- Automatically sets 777 permissions on extracted files
- Visual progress and confirmation

#### 🎵 Audio to FLAC Converter
- **Intelligent audio conversion** to FLAC format
- **Codec detection** - Distinguishes lossless vs lossy sources
- **Quality preservation** - Warns when converting lossy sources
- **Configurable compression** (0-8 levels)
- **Metadata preservation** - Artist, album, title, etc.
- **Artwork embedding** - Preserves album covers
- **Optional cleanup** - Delete originals after conversion
- **Output options** - Same directory or FLAC subdirectory
- **Standalone or integrated** - Run from command line or file manager

#### �️ Image Converter
- **Batch image conversion** using ImageMagick
- **Multiple output formats** - JPG (default), PNG, WebP, GIF, BMP, TIFF, AVIF
- **Quality control** - Configurable quality for lossy formats (1-100)
- **File selection** - Convert all images or select specific files
- **Optional cleanup** - Delete originals after conversion
- **Permission management** - Sets 777 permissions on output files
- **Standalone or integrated** - Run from command line or file manager

#### �📦➡️🎵 Extract and Convert
- **Combined workflow** - Extract archives AND convert audio in one step
- **Perfect for music archives** - Download, extract, convert to FLAC
- **Automatic folder detection** - Finds newly extracted directories
- **Batch processing** - Handles multiple archives at once
- **Cleanup options**:
  - `--delete-audio` - Delete original audio after conversion
  - `--delete-archive` - Delete archives after extraction
  - `--delete-all` - Delete both (same as `-d -a`)
- **Standalone or integrated** - Run from command line or file manager

#### 🔍 Empty Folder Analyzer
- Find **empty folders** (no files at any level)
- Identify **near-empty folders** (<10MB)
- List **file types** contained (audio, video, documents, etc.)
- **Inspect folders** with detailed breakdown
- **Delete unwanted folders** safely
- Size analysis with human-readable formats

#### 🎵 Essentia Music Tagger
- **ML-powered audio analysis** using Essentia TensorFlow models
- **Genre classification** with 400 Discogs genre classes
- **Mood/theme tagging** using MTG Jamendo mood model
- **Configurable thresholds** for genre and mood confidence
- **Multiple genre formats** - Parent-child, child-parent, child-only, raw
- **Dry run mode** - Analyze without writing tags
- **Recursive scanning** - Finds audio in all subdirectories
- **Standalone or integrated** - Run from command line or file manager

### 🎨 Beautiful Interface
- **Color-coded everything** - Directories, file types, messages
- **File icons** - Visual indicators for different file types
- **Status messages** - Clear feedback for all operations
- **Responsive design** - Adapts to terminal size
- **Professional layout** - Headers, footers, separators

## 📋 Requirements

- **Python 3.6+**
- **Linux/Unix** system (tested on Debian/Ubuntu)
- Terminal with **color support**
- **ffmpeg/ffprobe** (for audio quality inspection) - Install with: `sudo apt install ffmpeg`
- **ImageMagick** (for image conversion) - Install with: `sudo apt install imagemagick`
- **essentia-tensorflow** + **mutagen** (for Essentia Tagger, optional) - Install with: `pip install essentia-tensorflow mutagen`

**Note:** All utilities are included in this repository and will be installed along with the file manager.

## 🚀 Installation

### Quick Install

```bash
# 1. Clone the repository
cd /path/to/your/projects
git clone https://github.com/WB2024/WBs-Beautiful-TUI-Filemanager.git
cd WBs-Beautiful-TUI-Filemanager

# 2. Copy all utilities to system path
sudo cp filemanager extractfile fixperms audio-to-flac extract-and-convert image-convert iso2god file-sort video-player essentia-tagger /usr/local/bin/
sudo chmod +x /usr/local/bin/filemanager /usr/local/bin/extractfile /usr/local/bin/fixperms /usr/local/bin/audio-to-flac /usr/local/bin/extract-and-convert /usr/local/bin/image-convert /usr/local/bin/iso2god /usr/local/bin/file-sort /usr/local/bin/video-player /usr/local/bin/essentia-tagger

# 3. Run it!
filemanager
```

**What gets installed:**
- `filemanager` - The main TUI file manager
- `extractfile` - Archive extraction utility
- `fixperms` - Permission fixing tool (sets 777 recursively)
- `audio-to-flac` - Audio conversion utility (any format to FLAC)
- `extract-and-convert` - Combined extract archives + convert audio workflow
- `image-convert` - Image format conversion utility (using ImageMagick)
- `iso2god` - Xbox/Xbox 360 ISO to GOD converter (using iso2god-rs)
- `file-sort` - File organization utility (sort by type, extension, size, date)
- `video-player` - Terminal video player (using buddy)
- `essentia-tagger` - ML-powered audio genre/mood tagger (using Essentia)

### Manual Installation

```bash
# 1. Download all scripts
wget https://raw.githubusercontent.com/WB2024/WBs-Beautiful-TUI-Filemanager/main/filemanager
wget https://raw.githubusercontent.com/WB2024/WBs-Beautiful-TUI-Filemanager/main/extractfile
wget https://raw.githubusercontent.com/WB2024/WBs-Beautiful-TUI-Filemanager/main/fixperms
wget https://raw.githubusercontent.com/WB2024/WBs-Beautiful-TUI-Filemanager/main/audio-to-flac
wget https://raw.githubusercontent.com/WB2024/WBs-Beautiful-TUI-Filemanager/main/extract-and-convert
wget https://raw.githubusercontent.com/WB2024/WBs-Beautiful-TUI-Filemanager/main/image-convert
wget https://raw.githubusercontent.com/WB2024/WBs-Beautiful-TUI-Filemanager/main/iso2god
wget https://raw.githubusercontent.com/WB2024/WBs-Beautiful-TUI-Filemanager/main/file-sort
wget https://raw.githubusercontent.com/WB2024/WBs-Beautiful-TUI-Filemanager/main/video-player
wget https://raw.githubusercontent.com/WB2024/WBs-Beautiful-TUI-Filemanager/main/essentia-tagger

# 2. Make them executable
chmod +x filemanager extractfile fixperms audio-to-flac extract-and-convert image-convert iso2god file-sort video-player essentia-tagger

# 3. Move to PATH
sudo mv filemanager extractfile fixperms audio-to-flac extract-and-convert image-convert iso2god file-sort video-player essentia-tagger /usr/local/bin/

# 4. Run from anywhere
filemanager
```

### Verify Installation

```bash
# Check if all utilities are installed correctly
which filemanager extractfile fixperms audio-to-flac extract-and-convert image-convert iso2god file-sort video-player essentia-tagger

# Should output:
# /usr/local/bin/filemanager
# /usr/local/bin/extractfile
# /usr/local/bin/fixperms
# /usr/local/bin/audio-to-flac
# /usr/local/bin/extract-and-convert
# /usr/local/bin/image-convert
# /usr/local/bin/iso2god
# /usr/local/bin/file-sort
# /usr/local/bin/video-player
# /usr/local/bin/essentia-tagger
```
## 🔄 Updating

To update to the latest version:

### If You Cloned the Repository

```bash
# 1. Navigate to your cloned repository
cd /path/to/your/WBs-Beautiful-TUI-Filemanager

# 2. Pull the latest changes
git pull origin main

# 3. Copy updated files to system path (replace old versions)
sudo cp filemanager extractfile fixperms audio-to-flac extract-and-convert image-convert iso2god file-sort video-player essentia-tagger /usr/local/bin/
sudo chmod +x /usr/local/bin/filemanager /usr/local/bin/extractfile /usr/local/bin/fixperms /usr/local/bin/audio-to-flac /usr/local/bin/extract-and-convert /usr/local/bin/image-convert /usr/local/bin/iso2god /usr/local/bin/file-sort /usr/local/bin/video-player /usr/local/bin/essentia-tagger

# 4. Verify the update
filemanager
```

### If You Downloaded Files Manually

```bash
# 1. Download the latest versions
wget https://raw.githubusercontent.com/WB2024/WBs-Beautiful-TUI-Filemanager/main/filemanager -O filemanager
wget https://raw.githubusercontent.com/WB2024/WBs-Beautiful-TUI-Filemanager/main/extractfile -O extractfile
wget https://raw.githubusercontent.com/WB2024/WBs-Beautiful-TUI-Filemanager/main/fixperms -O fixperms
wget https://raw.githubusercontent.com/WB2024/WBs-Beautiful-TUI-Filemanager/main/audio-to-flac -O audio-to-flac
wget https://raw.githubusercontent.com/WB2024/WBs-Beautiful-TUI-Filemanager/main/extract-and-convert -O extract-and-convert
wget https://raw.githubusercontent.com/WB2024/WBs-Beautiful-TUI-Filemanager/main/image-convert -O image-convert
wget https://raw.githubusercontent.com/WB2024/WBs-Beautiful-TUI-Filemanager/main/iso2god -O iso2god
wget https://raw.githubusercontent.com/WB2024/WBs-Beautiful-TUI-Filemanager/main/file-sort -O file-sort
wget https://raw.githubusercontent.com/WB2024/WBs-Beautiful-TUI-Filemanager/main/video-player -O video-player
wget https://raw.githubusercontent.com/WB2024/WBs-Beautiful-TUI-Filemanager/main/essentia-tagger -O essentia-tagger

# 2. Make them executable
chmod +x filemanager extractfile fixperms audio-to-flac extract-and-convert image-convert iso2god file-sort video-player essentia-tagger

# 3. Replace old versions in system path
sudo mv filemanager extractfile fixperms audio-to-flac extract-and-convert image-convert iso2god file-sort video-player essentia-tagger /usr/local/bin/

# 4. Verify the update
filemanager
```

**Note:** Your bookmarks and configuration file (`~/.filemanager_config.json`) will be preserved during updates.
## 📦 Included Utilities

This package includes ten powerful command-line tools:

### 1. `filemanager` - Interactive TUI File Manager
The main application providing a beautiful terminal-based file browser with built-in text editor, audio quality inspector, and tools for navigation, bookmarks, archive extraction, and folder analysis.

**Key Features:**
- Color-coded file browser with icons
- Built-in text editor with syntax highlighting
- Audio quality inspector with comparison mode
- Bookmark system for quick directory access
- Archive extraction tool
- Empty folder analyzer
- Permission management

### 2. `extractfile` - Universal Archive Extractor
A standalone utility for extracting various archive formats. Can be used independently or is automatically called by the file manager.

**Features:**
- Supports: `.zip`, `.tar`, `.tar.gz`, `.tgz`, `.tar.bz2`, `.tbz2`, `.tar.xz`, `.txz`, `.gz`, `.bz2`, `.xz`, `.rar`, `.7z`
- Automatically sets 777 permissions on extracted files
- Can extract single archives or all archives in a directory

**Usage examples:**
```bash
extractfile archive.zip              # Extract specific file
extractfile file1.zip file2.tar.gz   # Extract multiple files
extractfile                          # Extract all archives in current directory
extractfile -l                       # List extractable files
```

**Dependencies for some formats:**
- RAR files: `sudo apt install unrar`
- 7z files: `sudo apt install p7zip-full`

### 3. `fixperms` - Permission Manager
An interactive utility for inspecting and managing file/folder permissions and ownership. Designed for users who don't know Linux permission numbers — everything uses human-readable names and descriptions.

**Features:**
- **Inspect permissions** - View current permissions, ownership, and a plain-English breakdown of what they mean
- **Inspect contents** - See permissions of every item inside a directory at a glance
- **15 permission presets** with friendly names:
  - "Full Access for Everyone" (777)
  - "Owner Only - Completely Private" (700)
  - "Read-Only for Everyone" (444)
  - "No Access for Anyone - Completely Locked" (000)
  - And 11 more common configurations
- **Owner selection** - Lists all system users with labels (regular users, service accounts, root)
- **Group selection** - Lists system groups with member info
- **Scope control** - Apply to just a folder, or recursively to everything inside
- **Quick fix mode** - One-click 777 for the original behavior
- **Review before applying** - Always shows a summary of changes before executing
- Falls back to simple `chmod -R 777` when run from the file manager if `fixperms` is not in PATH

**Usage examples:**
```bash
fixperms                             # Interactive mode in current directory
fixperms /var/www                    # Manage permissions for specific directory
sudo fixperms                        # Run with sudo for ownership changes
```

**No external dependencies required.**
### 4. `audio-to-flac` - Audio Converter
A standalone utility for converting audio files to FLAC format with intelligent codec detection.

**Features:**
- Converts any audio format to FLAC
- Distinguishes lossless vs lossy sources (warns when converting lossy)
- Configurable compression level (0-8)
- Preserves metadata and album artwork
- Optional deletion of original files

**Usage examples:**
```bash
audio-to-flac                        # Interactive conversion in current directory
```

**Dependencies:** `ffmpeg` (`sudo apt install ffmpeg`)

### 5. `extract-and-convert` - Archive to FLAC Workflow
A combined utility that extracts archives and converts audio to FLAC in one step.

**Features:**
- Extracts archives, then converts audio in extracted folders
- Supports all archive formats via `extractfile`
- Cleanup options for archives and/or original audio

**Usage examples:**
```bash
extract-and-convert                  # Process all archives in current directory
extract-and-convert album.zip        # Process specific archive
extract-and-convert -d               # Delete original audio after conversion
extract-and-convert -a               # Delete archive after extraction
extract-and-convert -da              # Delete both
```

### 6. `image-convert` - Image Format Converter
A standalone utility for batch converting images between formats using ImageMagick.

**Features:**
- Convert to JPG, PNG, WebP, GIF, BMP, TIFF, or AVIF
- Configurable quality for lossy formats (1-100)
- Select all images or specific files
- Optional deletion of original files
- Sets 777 permissions on output files

**Usage examples:**
```bash
image-convert                        # Interactive conversion in current directory
```

**Dependencies:** ImageMagick (`sudo apt install imagemagick` or `brew install imagemagick`)

### 7. `iso2god` - Xbox ISO to GOD Converter
A standalone utility for converting Xbox 360 and original Xbox disc images (ISO) to Games-On-Demand (GOD) format.

**Features:**
- Convert Xbox 360 and original Xbox ISOs to GOD format
- Trim unused space from ISO images
- Set custom game titles
- Multi-threaded conversion for faster processing
- Select all ISOs or specific files
- Optional deletion of original ISO files
- Sets 777 permissions on output files

**Usage examples:**
```bash
iso2god                              # Interactive conversion in current directory
```

**Dependencies:** iso2god-rs binary from https://github.com/iliazeus/iso2god-rs/releases

**Quick install for iso2god-rs (Linux x86_64):**
```bash
wget https://github.com/iliazeus/iso2god-rs/releases/download/v1.8.1/iso2god-x86_64-linux
chmod +x iso2god-x86_64-linux
sudo mv iso2god-x86_64-linux /usr/local/bin/iso2god-rs
```

### 8. `file-sort` - File Organization Tool
A standalone utility for sorting and organizing files in a directory by various criteria.

**Features:**
- **Scope selection** - Sort current directory only, or recursively collect files from all subdirectories
- **Sort by File Type** - Groups files into categories: Audio, Video, Images, Documents, Text, Code, Data, Web, Archives, Executables, Fonts, Ebooks, 3D Models, CAD, Torrents, Other
- **Sort by Extension** - Creates folders for each file extension (MP3, JPG, PY, etc.)
- **Sort by Size** - Groups files by size: Tiny (<100KB), Small (100KB-1MB), Medium (1MB-100MB), Large (100MB-1GB), Huge (>1GB)
- **Sort by Date Modified** - Groups files by modification time: Today, Yesterday, This Week, This Month, This Year, or by year
- **Sort by First Letter** - Alphabetical organization (A-Z, 0-9, Special characters)
- **Recursive mode** - Collect files from all child folders and organize into the root directory
- **Empty folder cleanup** - Optionally remove empty folders left behind after recursive sort
- Preview before sorting
- Handles permission issues automatically
- Sets 777 permissions on created folders and moved files
- Handles filename collisions (appends _1, _2, etc.)

**Usage examples:**
```bash
file-sort                            # Interactive sorting in current directory
```

**No external dependencies required.**

### 9. `video-player` - Terminal Video Player
A standalone utility for playing videos directly in the terminal. Supports **two video players** with configurable default:

**Supported Players:**
- **buddy** - Python-based player with true 24-bit color (https://github.com/JVSCHANDRADITHYA/buddy)
- **ncplayer** - C-based player from notcurses library (https://github.com/dankamongmen/notcurses)

**Features:**
- **Configurable player preference** - Set default to `auto`, `buddy`, or `ncplayer`
- Settings stored in `~/.filemanager_config.json`
- **buddy render modes:**
  - **half** (default) - Best quality using Unicode half-blocks, 2x vertical resolution
  - **ascii** - Classic ASCII art look with true-color tinting
  - **braille** - Highest spatial resolution using braille patterns
- **buddy quality levels:**
  - Fast (nearest-neighbor sampling)
  - Balanced (4-tap supersample, default)
  - Best (full box filter)
- Scale video to fit terminal (10%-100%)
- Loop videos indefinitely
- Hide/show status bar
- Interactive file selection
- Works with all common video formats
- **Ctrl+C stops video without exiting filemanager**

**Usage examples:**
```bash
video-player                         # Interactive playback in current directory
```

**Keyboard shortcuts in file manager:**
- Press `V` on any video file to play it directly
- Press `t` for Tools menu → `[7] Play Video` for interactive selection
- Press `t` for Tools menu → `[s] Video Player Settings` to change player

**Installing buddy (venv method for PEP 668 systems):**
```bash
git clone https://github.com/JVSCHANDRADITHYA/buddy
cd buddy
python3 -m venv venv
venv/bin/pip install numpy imageio imageio-ffmpeg

# Create wrapper script
cat > buddy-wrapper.sh << 'EOF'
#!/bin/bash
SOURCE="${BASH_SOURCE[0]}"
while [ -L "$SOURCE" ]; do
    DIR="$(cd -P "$(dirname "$SOURCE")" && pwd)"
    SOURCE="$(readlink "$SOURCE")"
    [[ $SOURCE != /* ]] && SOURCE="$DIR/$SOURCE"
done
SCRIPT_DIR="$(cd -P "$(dirname "$SOURCE")" && pwd)"
"$SCRIPT_DIR/venv/bin/python" "$SCRIPT_DIR/ascii_play/cli.py" "$@"
EOF

chmod +x buddy-wrapper.sh
sudo ln -sf "$(pwd)/buddy-wrapper.sh" /usr/local/bin/buddy
```

**Installing ncplayer (simpler, from package manager):**
```bash
# Debian/Ubuntu
sudo apt install notcurses-bin

# Arch Linux
sudo pacman -S notcurses

# macOS
brew install notcurses
```

**Requirements:**
- For buddy: Python 3.9+, terminal with 24-bit true color support
- For ncplayer: Just the notcurses package

### 10. `essentia-tagger` - ML-Powered Audio Genre/Mood Tagger
A standalone utility for analyzing audio files with Essentia ML models and writing genre/mood tags to file metadata. Based on [Essentia-to-Metadata](https://github.com/WB2024/Essentia-to-Metadata).

**Features:**
- **ML-powered analysis** using Essentia TensorFlow models (Discogs-EffNet)
- **Genre classification** with 400 genre classes from the Discogs taxonomy
- **Mood/theme tagging** using the MTG Jamendo mood model
- **Configurable settings:**
  - Number of genre tags per file (1-10)
  - Genre confidence threshold (1-50%)
  - Mood confidence threshold
  - Genre format: parent-child, child-parent, child-only, or raw
  - Dry run mode (analyze without writing)
  - Overwrite existing tags or preserve them
  - Confidence score tags
- **Broad format support:** FLAC, MP3, OGG, Opus, M4A, AAC, WMA, AIFF, WAV, WavPack, APE, Musepack, DSF
- **Recursive scanning** - Finds audio files in all subdirectories
- **Detailed logging** - Full analysis log saved to timestamped log file
- **CLI and interactive modes** - Run interactively or with command-line arguments

**Usage examples:**
```bash
# Interactive mode (run in current directory)
essentia-tagger

# Automated mode with path
essentia-tagger /path/to/music --auto

# Custom settings
essentia-tagger /path/to/music --auto --genres 4 --genre-threshold 20

# Dry run (analyze without writing tags)
essentia-tagger /path/to/music --auto --dry-run

# Single file
essentia-tagger /path/to/song.flac --auto --single-file
```

**Dependencies:**
- `essentia-tensorflow` - Install with: `pip install essentia-tensorflow`
- `mutagen` - Install with: `pip install mutagen`
- `numpy` - Install with: `pip install numpy`
- Essentia ML models (downloaded to `~/essentia_models/`):
```bash
mkdir -p ~/essentia_models && cd ~/essentia_models
wget https://essentia.upf.edu/models/music-style-classification/discogs-effnet/discogs-effnet-bs64-1.pb
wget https://essentia.upf.edu/models/classification-heads/genre_discogs400/genre_discogs400-discogs-effnet-1.pb
wget https://essentia.upf.edu/models/classification-heads/genre_discogs400/genre_discogs400-discogs-effnet-1.json
wget https://essentia.upf.edu/models/classification-heads/mtg_jamendo_moodtheme/mtg_jamendo_moodtheme-discogs-effnet-1.pb
wget https://essentia.upf.edu/models/classification-heads/mtg_jamendo_moodtheme/mtg_jamendo_moodtheme-discogs-effnet-1.json
```

## 📖 Usage Guide

### Basic Navigation

```
Launch:           filemanager
Navigate:         ↑/↓ arrow keys
Open folder:      Enter
Edit text file:   Enter (on text files)
Inspect audio:    Enter (on audio files)
View file info:   Enter (on other files)
Go up:            Backspace or select ".."
Go to home:       h
Go to root:       r
Toggle help:      ?
Quit:             q
```

### Keyboard Shortcuts

| Key | Action |
|-----|--------|
| `↑` / `↓` | Navigate up/down through files |
| `Enter` | Open directory / Edit text file / Inspect audio/video file |
| `Backspace` | Go to parent directory |
| `h` | Jump to home directory |
| `r` | Jump to root directory (/) |
| `Space` | Toggle mark on current file |
| `a` | Mark all files in current folder |
| `u` | Unmark all files |
| `c` | Copy marked files (or current file) to clipboard |
| `x` | Cut marked files (or current file) to clipboard |
| `v` | Paste from clipboard to current directory |
| `d` | Delete marked files (or current file) |
| `n` | Create new file or folder |
| `R` | Rename current file or folder |
| `o` | Open file operations menu |
| `t` | Open tools menu (FLAC, image convert, extract, file sort, video) |
| `V` | Play selected video file with buddy |
| `b` | Open bookmarks menu |
| `p` | Fix permissions (777 recursive) |
| `e` | Extract archives |
| `f` | Find empty/near-empty folders |
| `?` | Toggle help display |
| `q` | Quit file manager |

### Text Editor Controls

When editing a text file:

| Key | Action |
|-----|--------|
| `Ctrl+S` | Save file |
| `Ctrl+Q` | Quit editor (warns if unsaved) |
| `Ctrl+X` | Force quit without saving |
| `Ctrl+A` | Select all text (copy to clipboard) |
| `Ctrl+C` | Copy current line |
| `Ctrl+V` | Paste from clipboard |
| `Ctrl+D` | Delete all text |
| `↑` / `↓` / `←` / `→` | Navigate cursor |
| `Page Up` / `Page Down` | Scroll by page |
| `Home` / `End` | Jump to line start/end |
| `Tab` | Insert 4 spaces |
| `Backspace` | Delete character before cursor |
| `Delete` | Delete character at cursor |
| `Enter` | New line |

### Audio Inspector Controls

When inspecting an audio file:

| Key | Action |
|-----|--------|
| `c` | Start/Clear comparison mode |
| `q` | Exit inspector (or return to single view from comparison) |
| `ESC` | Exit inspector (or return to single view from comparison) |
| `↑` / `↓` | Navigate files (in comparison browse mode) |
| `Enter` | Select file for comparison (in comparison browse mode) |
| `Backspace` | Go up directory (in comparison browse mode) |

### Video Inspector Controls

When inspecting a video file:

| Key | Action |
|-----|--------|
| `c` | Start/Clear comparison mode |
| `q` | Exit inspector (or return to single view from comparison) |
| `ESC` | Exit inspector (or return to single view from comparison) |
| `↑` / `↓` | Navigate files (in comparison browse mode) |
| `Enter` | Select file for comparison (in comparison browse mode) |
| `Backspace` | Go up directory (in comparison browse mode) |

### Image Inspector Controls

When inspecting an image file:

| Key | Action |
|-----|--------|
| `c` | Start/Clear comparison mode |
| `q` | Exit inspector (or return to single view from comparison) |
| `ESC` | Exit inspector (or return to single view from comparison) |
| `↑` / `↓` | Navigate files (in comparison browse mode) |
| `Enter` | Select file for comparison (in comparison browse mode) |
| `Backspace` | Go up directory (in comparison browse mode) |

### Bookmarks

**Add a bookmark:**
1. Navigate to the directory you want to bookmark
2. Press `b` for bookmarks menu
3. Select "Add current directory as bookmark"
4. Enter a name (e.g., "external-drive", "projects", "downloads")

**Use a bookmark:**
1. Press `b`
2. Select your bookmark from the list
3. Instantly jump to that location!

**Remove a bookmark:**
1. Press `b`
2. Select "Remove a bookmark"
3. Enter the bookmark name

### Text Editor

**Opening files:**
- The text editor automatically opens when you press Enter on any supported text file
- Supports 50+ file extensions including:
  - **Programming**: `.py`, `.js`, `.java`, `.c`, `.cpp`, `.go`, `.rs`, `.php`, `.rb`, etc.
  - **Web**: `.html`, `.css`, `.json`, `.xml`, `.yaml`, `.yml`
  - **Scripts**: `.sh`, `.bash`, `.ps1`, `.bat`
  - **Documents**: `.txt`, `.md`, `.log`, `.csv`, `.ini`, `.cfg`
  - And many more!

**Editing features:**
- **Line numbers** displayed on the left with current line highlighted
- **Syntax highlighting** for Python, JSON, and other formats
- **Cursor position** shown in header (Line X/Y Col Z)
- **Modification indicator** shows [Modified] when file has unsaved changes
- **Smart scrolling** - Both horizontal and vertical scrolling for large files

**Clipboard operations:**
- **Ctrl+A**: Copy entire file to internal clipboard
- **Ctrl+C**: Copy current line to clipboard
- **Ctrl+V**: Paste clipboard contents at cursor
  - Single-line paste inserts at cursor position
  - Multi-line paste inserts lines starting at cursor

**File operations:**
- **Ctrl+S**: Save file (shows success message)
- **Ctrl+Q**: Quit editor (warns if unsaved changes exist)
- **Ctrl+X**: Force quit without saving (no confirmation)
- **Ctrl+D**: Delete all text in file (leaves one empty line)

**Navigation:**
- Arrow keys move cursor character by character
- **Page Up/Down** scroll by full pages
- **Home/End** jump to start/end of current line
- Cursor automatically scrolls viewport when moving off-screen

**Tips:**
- Tab key inserts 4 spaces (configurable in code)
- The editor handles large files efficiently
- Syntax highlighting adapts to file extension
- UTF-8 encoding is used for all file operations

### Audio Quality Inspector

**Opening the inspector:**
- Navigate to any audio file (MP3, FLAC, WAV, M4A, AAC, OGG, Opus, WMA, etc.)
- Press **Enter** to launch the Audio Quality Inspector
- Instant professional-grade analysis using ffprobe

**Quality metrics displayed:**
- **Quality Score** (0-100) with color-coded rating:
  - 90-100: Exceptional (Green)
  - 75-89: Excellent (Green)
  - 60-74: Very Good (Blue)
  - 45-59: Good (Yellow)
  - 30-44: Fair (Yellow)
  - 0-29: Poor (Red)
- **File Size**: Total file size in MB/GB
- **Duration**: Track length in MM:SS format
- **Format**: Container format (MP3, FLAC, etc.)
- **Codec**: Audio codec with lossless detection
- **Sample Rate**: Frequency in Hz (higher is better)
  - 192000 Hz: Hi-Res audio
  - 96000 Hz: Studio quality
  - 48000 Hz / 44100 Hz: CD quality
- **Bitrate**: Data rate in kbps (higher is better)
  - 1411+ kbps: Lossless
  - 320 kbps: High quality MP3
  - 256-192 kbps: Good quality
  - 128 kbps: Standard quality
- **Bit Depth**: Resolution in bits (16-bit, 24-bit, etc.)
- **Channels**: Stereo, Mono, or surround configuration

**Data source indicators:**
Bitrate values show a tag indicating how the data was obtained:
- **[S] Stream**: Extracted directly from audio stream analysis (most accurate)
- **[F] Format**: Extracted from container format metadata
- **[C] Calculated**: Computed from file size and duration

**Comparing two audio files:**
1. Open the first audio file (press Enter)
2. In the inspector, press **c** to start comparison
3. Navigate to the second audio file using arrow keys
4. Press **Enter** to select the comparison file
5. View side-by-side comparison with:
   - All metrics displayed for both files
   - Quality scores compared
   - Clear winner indication with recommendation
   - Score difference highlighted

**Comparison use cases:**
- **Duplicate songs**: Find which version has better quality
- **Format comparison**: Compare lossy vs lossless versions
- **Download verification**: Ensure you got the best quality version
- **Library cleanup**: Identify and remove lower-quality duplicates

**Controls:**
- **q** or **ESC**: Exit inspector (or return to single view from comparison)
- **c**: Start comparison mode / Clear comparison
- Navigate normally in comparison browse mode

**Tips:**
- Lossless formats (FLAC, ALAC, WAV, APE) automatically get higher scores
- Green-colored metrics indicate high-quality values
- The quality score combines sample rate, bitrate, bit depth, and codec
- Perfect for deciding which duplicate file to keep!

### Video Quality Inspector

**Opening the inspector:**
- Navigate to any video file (MP4, MKV, AVI, MOV, WebM, etc.)
- Press **Enter** to launch the Video Quality Inspector
- Professional-grade video analysis using ffprobe

**Quality metrics displayed:**
- **Quality Score** (0-100) with color-coded rating:
  - 90-100: Exceptional (Green)
  - 75-89: Excellent (Green)
  - 60-74: Very Good (Blue)
  - 45-59: Good (Yellow)
  - 30-44: Fair (Yellow)
  - 0-29: Poor (Red)
- **File Size**: Total file size in MB/GB
- **Duration**: Video length in HH:MM:SS or MM:SS format
- **Resolution**: Common name (8K UHD, 4K UHD, Full HD, etc.)
- **Dimensions**: Exact pixel dimensions (e.g., 1920x1080)
- **Video Codec**: Compression format with quality indicator
  - AV1: Most modern and efficient (Green)
  - HEVC/H.265: Excellent quality (Green)
  - VP9: Very good quality
  - H.264/AVC: Good standard
- **Video Bitrate**: Data rate in Mbps (higher is better)
  - 50+ Mbps: Exceptional quality
  - 20+ Mbps: Excellent for 4K
  - 10+ Mbps: Very good for 1080p
  - 5+ Mbps: Good for 1080p
- **Frame Rate**: Frames per second (60fps/120fps = smoother)
- **Audio Codec**: Audio compression format
- **Audio Bitrate**: Audio data rate if audio track present

**Resolution categories:**
- **8K UHD**: 7680x4320 or higher
- **4K UHD (2160p)**: 3840x2160 or higher
- **QHD (1440p)**: 2560x1440 or higher
- **Full HD (1080p)**: 1920x1080 or higher
- **HD (720p)**: 1280x720 or higher
- **SD (480p)**: 854x480 or higher

**Data source indicators:**
Bitrate values show a tag indicating how the data was obtained:
- **[S] Stream**: Extracted directly from video/audio stream analysis (most accurate)
- **[F] Format**: Extracted from container format metadata
- **[C] Calculated**: Computed from file size and duration
- **[E] Estimated**: Rough estimate based on typical ratios (audio bitrate in videos)

The inspector prioritizes stream analysis, then falls back to calculations if stream data is unavailable.

**Comparing two video files:**
1. Open the first video file (press Enter)
2. In the inspector, press **c** to start comparison
3. Navigate to the second video file using arrow keys
4. The message bar shows which file you're comparing FROM
5. Press **Enter** to select the comparison file
6. View side-by-side comparison with:
   - All metrics displayed for both files
   - Quality scores compared
   - Clear winner indication with recommendation
   - Score difference highlighted

**Comparison use cases:**
- **Format comparison**: Compare different encodings (H.264 vs H.265)
- **Resolution comparison**: Compare 1080p vs 4K versions
- **Bitrate testing**: Find optimal bitrate for file size
- **Download verification**: Ensure you got the best quality version
- **Library cleanup**: Identify and remove lower-quality duplicates
- **Transcoding validation**: Verify re-encoded videos maintain quality

**Quality scoring algorithm:**
The 0-100 score is calculated from:
- **Resolution** (35 points): Higher resolutions score better
- **Video Bitrate** (30 points): Higher bitrates score better
- **Codec** (20 points): Modern codecs (AV1, HEVC) score higher
- **Frame Rate** (15 points): 60fps+ scores higher than 30fps

**Controls:**
- **q** or **ESC**: Exit inspector (or return to single view from comparison)
- **c**: Start comparison mode / Clear comparison
- Navigate normally in comparison browse mode

**Supported formats:**
MP4, MKV, AVI, MOV, WMV, FLV, WebM, M4V, MPG, MPEG, 3GP, OGV, TS, M2TS, VOB, DivX, XviD, F4V, RM, RMVB

**Tips:**
- Green-colored metrics indicate high-quality values
- Modern codecs (AV1, HEVC/H.265) provide better quality at lower bitrates
- 4K at 20 Mbps often looks better than 1080p at 10 Mbps
- Frame rate matters: 60fps is noticeably smoother than 30fps for action
- Perfect for comparing different encodes of the same content!

### Empty Folder Analysis

**Find and manage empty folders:**
1. Navigate to the directory you want to analyze
2. Press `f`
3. Wait for scan to complete
4. Review results:
   - **Empty** (red): No files at any level
   - **Near-empty** (yellow): < 10MB with file type info
   - **Non-empty** (green): ≥ 10MB with file type info

**Inspect a folder:**
- Use `↑`/`↓` to select a folder
- Press `i` to inspect
- See detailed breakdown:
  - Total size and file count
  - File types with counts and sizes
  - Sample files from each category

**Delete a folder:**
- Select folder with `↑`/`↓`
- Press `d` to delete
- Confirm with `y`

### Archive Extraction

**Extract archives:**
1. Navigate to directory containing archives
2. Press `e`
3. Use `↑`/`↓` to navigate menu
4. Press `Space` on "Extract All" to toggle, or select individual archive
5. Press `Enter` to extract selected archives

**Supported formats:**
- `.zip`, `.tar`, `.tar.gz`, `.tgz`
- `.tar.bz2`, `.tbz2`, `.tar.xz`, `.txz`
- `.gz`, `.bz2`, `.xz`, `.rar`, `.7z`

### Audio to FLAC Converter

**From the file manager:**
1. Navigate to a folder containing audio files
2. Press `t` to open Tools menu
3. Select "Convert Audio to FLAC"
4. Follow interactive prompts

**From command line:**
```bash
# Navigate to folder with audio files
cd /path/to/audio/files

# Run interactively
audio-to-flac
```

**Features:**
- Scans current directory for audio files
- Analyzes each file with ffprobe (codec, sample rate, bit depth)
- Distinguishes **lossless** vs **lossy** sources
- Warns that converting lossy→FLAC won't improve quality (only increases file size)
- Interactive prompts for:
  - **Compression level** (0-8, default 8 for smallest files)
  - **Metadata preservation** (artist, album, title, etc.)
  - **Artwork preservation** (embedded album covers)
  - **Delete originals** (optional cleanup)
  - **Output directory** (same folder or FLAC subdirectory)
- Sets 777 permissions on output files

**Supported input formats:**
M4A, MP3, WAV, AAC, OGG, Opus, WMA, APE, ALAC, AIFF, FLAC (skipped), MKA, MP2, AC3, DTS, TTA, WV, MPC

### Image Converter

**From the file manager:**
1. Navigate to a folder containing image files
2. Press `t` to open Tools menu
3. Select "Convert Images"
4. Follow interactive prompts

**From command line:**
```bash
# Navigate to folder with image files
cd /path/to/image/files

# Run interactively
image-convert
```

**Features:**
- Scans current directory for image files
- Select all images or choose specific files
- Multiple output formats:
  - **JPG** (default) - Best for photos, small file size
  - **PNG** - Lossless, supports transparency
  - **WebP** - Modern format, excellent compression
  - **GIF** - 256 colors, supports animation
  - **BMP** - Uncompressed bitmap
  - **TIFF** - High quality, large files
  - **AVIF** - Next-gen format, best compression
- Configurable quality (1-100) for lossy formats
- Optional deletion of original files
- Sets 777 permissions on output files

**Supported input formats:**
JPG, JPEG, PNG, GIF, BMP, TIFF, TIF, WebP, HEIC, HEIF, AVIF, ICO, SVG, RAW, CR2, NEF, ARW, DNG, PSD, XCF

### Extract and Convert

**From the file manager:**
1. Navigate to a folder containing archives with audio files
2. Press `t` to open Tools menu
3. Select "Extract & Convert"
4. The tool extracts archives, then converts audio in each extracted folder

**From command line:**
```bash
# Extract all archives and convert audio (interactive)
extract-and-convert

# Extract specific archive
extract-and-convert album.zip

# Delete original audio files after conversion
extract-and-convert --delete-audio
extract-and-convert -d album.zip

# Delete archive after extraction
extract-and-convert --delete-archive
extract-and-convert -a album.zip

# Delete both archives and original audio
extract-and-convert --delete-all
extract-and-convert -da album.zip

# Quiet mode (less output)
extract-and-convert -q
```

**Workflow:**
1. **Extract** - Uses `extractfile` to extract archives
2. **Detect** - Finds newly created directories
3. **Convert** - Runs `audio-to-flac` in each directory
4. **Cleanup** - Optionally deletes archives and/or original audio

**Use cases:**
- Download music archives → extract → convert to FLAC
- Batch process multiple album downloads
- Automated music library management

## 🎨 Color Scheme

- 📁 **Cyan** - Directories
- 📦 **Green** - Archives
- 🎵 **Magenta** - Audio files
- 🎬 **Red** - Video files
- 🖼️ **Yellow** - Images
- � **White** - Regular files (including code, documents, etc.)

## 🔧 Configuration

Settings are stored in: `~/.filemanager_config.json`

Example config:
```json
{
  "bookmarks": {
    "external": "/srv/dev-disk-by-uuid-dc4918d5-6597-465b-9567-ce442fbd8e2a",
    "projects": "/home/user/projects",
    "downloads": "/home/user/Downloads"
  },
  "video_player": "auto"
}
```

**Configuration options:**
- `bookmarks` - Named directory shortcuts (managed via `b` key)
- `video_player` - Preferred terminal video player:
  - `"auto"` (default) - Try buddy first, fall back to ncplayer
  - `"buddy"` - Use buddy (Python-based, more render options)
  - `"ncplayer"` - Use ncplayer from notcurses (simpler, C-based)

**Change video player via:**
- Tools menu (`t`) → `[s] Video Player Settings`
- Or edit the config file directly

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🐛 Bug Reports

Found a bug? Please open an issue on GitHub with:
- Your OS and Python version
- Steps to reproduce
- Expected vs actual behavior
- Any error messages

## 💡 Feature Requests

Have an idea? Open an issue with the `enhancement` label!

## ☕ Support

If you find this tool useful, consider buying me a coffee!

[![Buy Me A Coffee](https://img.shields.io/badge/Buy%20Me%20A%20Coffee-Support-yellow?logo=buy-me-a-coffee)](https://buymeacoffee.com/succinctrecords)

## 🙏 Acknowledgments

- Built with Python's `curses` library
- Inspired by classic file managers like Midnight Commander and Ranger
- Thanks to all contributors and users!

## 📚 Related Projects

## 📞 Contact

- GitHub: [@WB2024](https://github.com/WB2024)
- Buy Me A Coffee: [succinctrecords](https://buymeacoffee.com/succinctrecords)

---

**Made with ❤️ for the terminal**
