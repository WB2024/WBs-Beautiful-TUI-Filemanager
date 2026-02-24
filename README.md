# 🗂️ Terminal File Manager

A beautiful, interactive terminal-based file manager with a built-in text editor and powerful tools for Linux/Unix systems. Navigate your filesystem with arrow keys, edit files with syntax highlighting, manage permissions, extract archives, and analyze disk usage - all from a gorgeous TUI (Terminal User Interface).

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
The main application providing a beautiful terminal-based file browser with built-in text editor and tools for navigation, bookmarks, archive extraction, and folder analysis.

**Key Features:**
- Color-coded file browser with icons
- Built-in text editor with syntax highlighting
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
View file info:   Enter (on non-text files)
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
| `Enter` | Open directory or edit text file |
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
