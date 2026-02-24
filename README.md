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

### 🔖 Bookmark System
- **Save favorite directories** with custom names
- **Quick access** to frequently used locations
- **Persistent storage** - Bookmarks saved to `~/.filemanager_config.json`
- Perfect for long paths like `/srv/dev-disk-by-uuid-...`

### 🛠️ Built-in Tools

#### 🔓 Permission Manager
- Set **777 permissions recursively** on current directory
- Uses `chmod -R 777` command
- Confirmation prompts for safety
- One-key access with `p`

**Note:** For a standalone permission tool with more options (including ownership changes), use the included `fixperms` utility from the command line.

#### 📦 Archive Extractor
- Extract **zip, tar, gz, bz2, xz, rar, 7z** archives
- Select individual files or extract all
- Uses the included `extractfile` utility
- Automatically sets 777 permissions on extracted files
- Visual progress and confirmation

#### 🔍 Empty Folder Analyzer
- Find **empty folders** (no files at any level)
- Identify **near-empty folders** (<10MB)
- List **file types** contained (audio, video, documents, etc.)
- **Inspect folders** with detailed breakdown
- **Delete unwanted folders** safely
- Size analysis with human-readable formats

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

**Note:** The required `extractfile` and `fixperms` utilities are included in this repository and will be installed along with the file manager.

## 🚀 Installation

### Quick Install

```bash
# 1. Clone the repository
cd /path/to/your/projects
git clone https://github.com/WB2024/WBs-Beautiful-TUI-Filemanager.git
cd WBs-Beautiful-TUI-Filemanager

# 2. Copy all three utilities to system path
sudo cp filemanager extractfile fixperms /usr/local/bin/
sudo chmod +x /usr/local/bin/filemanager /usr/local/bin/extractfile /usr/local/bin/fixperms

# 3. Run it!
filemanager
```

**What gets installed:**
- `filemanager` - The main TUI file manager
- `extractfile` - Archive extraction utility (used by the file manager)
- `fixperms` - Standalone permission fixing tool (sets 777 recursively)

### Manual Installation

```bash
# 1. Download all three scripts
wget https://raw.githubusercontent.com/WB2024/WBs-Beautiful-TUI-Filemanager/main/filemanager
wget https://raw.githubusercontent.com/WB2024/WBs-Beautiful-TUI-Filemanager/main/extractfile
wget https://raw.githubusercontent.com/WB2024/WBs-Beautiful-TUI-Filemanager/main/fixperms

# 2. Make them executable
chmod +x filemanager extractfile fixperms

# 3. Move to PATH
sudo mv filemanager extractfile fixperms /usr/local/bin/

# 4. Run from anywhere
filemanager
```

### Verify Installation

```bash
# Check if all utilities are installed correctly
which filemanager extractfile fixperms

# Should output:
# /usr/local/bin/filemanager
# /usr/local/bin/extractfile
# /usr/local/bin/fixperms
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
sudo cp filemanager extractfile fixperms /usr/local/bin/
sudo chmod +x /usr/local/bin/filemanager /usr/local/bin/extractfile /usr/local/bin/fixperms

# 4. Verify the update
filemanager
```

### If You Downloaded Files Manually

```bash
# 1. Download the latest versions
wget https://raw.githubusercontent.com/WB2024/WBs-Beautiful-TUI-Filemanager/main/filemanager -O filemanager
wget https://raw.githubusercontent.com/WB2024/WBs-Beautiful-TUI-Filemanager/main/extractfile -O extractfile
wget https://raw.githubusercontent.com/WB2024/WBs-Beautiful-TUI-Filemanager/main/fixperms -O fixperms

# 2. Make them executable
chmod +x filemanager extractfile fixperms

# 3. Replace old versions in system path
sudo mv filemanager extractfile fixperms /usr/local/bin/

# 4. Verify the update
filemanager
```

**Note:** Your bookmarks and configuration file (`~/.filemanager_config.json`) will be preserved during updates.
## � Included Utilities

This package includes three powerful command-line tools:

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

### 3. `fixperms` - Permission Fixer
A standalone utility for recursively setting 777 permissions and ownership on directories.

**Features:**
- Sets 777 (rwxrwxrwx) permissions recursively
- Can optionally change ownership
- Interactive confirmation prompts
- Detailed progress reporting

**Usage examples:**
```bash
fixperms                             # Fix current directory
fixperms /var/www                    # Fix specific directory
fixperms . nobody:nogroup            # Fix with specific ownership
sudo fixperms                        # Run with sudo for ownership changes
```

## �📖 Usage Guide

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
| `Enter` | Open directory / Edit text file / Inspect audio file |
| `Backspace` | Go to parent directory |
| `h` | Jump to home directory |
| `r` | Jump to root directory (/) |
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
Bitrate values show an icon indicating how the data was obtained:
- **📊 Stream**: Extracted directly from audio stream analysis (most accurate)
- **🔢 Calculated**: Computed from file size and duration
- **📝 Format**: Extracted from container format metadata

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
Bitrate values show an icon indicating how the data was obtained:
- **📊 Stream**: Extracted directly from video/audio stream analysis (most accurate)
- **🔢 Calculated**: Computed from file size and duration
- **📝 Format**: Extracted from container format metadata
- **⚠️ Estimated**: Rough estimate based on typical ratios (audio only)

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

## 🎨 Color Scheme

- 📁 **Cyan** - Directories
- 📦 **Green** - Archives
- 🎵 **Magenta** - Audio files
- 🎬 **Red** - Video files
- 🖼️ **Yellow** - Images
- � **White** - Regular files (including code, documents, etc.)

## 🔧 Configuration

Bookmarks are stored in: `~/.filemanager_config.json`

Example config:
```json
{
  "bookmarks": {
    "external": "/srv/dev-disk-by-uuid-dc4918d5-6597-465b-9567-ce442fbd8e2a",
    "projects": "/home/user/projects",
    "downloads": "/home/user/Downloads"
  }
}
```

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
