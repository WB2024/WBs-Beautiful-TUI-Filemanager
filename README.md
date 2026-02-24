# 🗂️ Terminal File Manager

A beautiful, interactive terminal-based file manager with built-in tools for Linux/Unix systems. Navigate your filesystem with arrow keys, edit text files, manage permissions, extract archives, and analyze disk usage - all from a gorgeous TUI (Terminal User Interface).

[![Buy Me A Coffee](https://img.shields.io/badge/Buy%20Me%20A%20Coffee-Support-yellow?logo=buy-me-a-coffee)](https://buymeacoffee.com/succinctrecords)

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Python](https://img.shields.io/badge/python-3.6%2B-blue.svg)

## ✨ Features

### 🎮 Interactive Navigation
- **Arrow key navigation** - Browse files and folders with ↑/↓ keys
- **Color-coded files** - Different colors for audio 🎵, video 🎬, images 🖼️, archives 📦, code 💻, and more
- **Smart scrolling** - Smooth scrolling with visual scrollbar
- **Quick jumps** - Instantly jump to home, root, or bookmarked locations

### 📝 Built-in Text Editor
- **Syntax highlighting** for Python, JSON, Shell scripts, Markdown, and more
- **Line numbers** and cursor position tracking
- **Full editing capabilities** - Insert, delete, newlines, navigation
- **Save functionality** with modification tracking
- **Auto-detection** of text files (supports 40+ file extensions)
- **Page Up/Down** support for large files

### 🔖 Bookmark System
- **Save favorite directories** with custom names
- **Quick access** to frequently used locations
- **Persistent storage** - Bookmarks saved to `~/.filemanager_config.json`
- Perfect for long paths like `/srv/dev-disk-by-uuid-...`

### 🛠️ Built-in Tools

#### 🔓 Permission Manager
- Set **777 permissions recursively** on current directory
- Confirmation prompts for safety
- One-key access with `p`

#### 📦 Archive Extractor
- Extract **zip, tar, gz, bz2, xz, rar, 7z** archives
- Select individual files or extract all
- Integrates with system `extractfile` command
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
- Optional: `extractfile` command for archive extraction (can be installed separately)

## 🚀 Installation

### Quick Install

```bash
# 1. Clone the repository
cd /path/to/your/projects
git clone https://github.com/YOUR_USERNAME/terminal-filemanager.git
cd terminal-filemanager

# 2. Copy to system path
sudo cp filemanager /usr/local/bin/filemanager
sudo chmod +x /usr/local/bin/filemanager

# 3. Run it!
filemanager
```

### Manual Installation

```bash
# 1. Download the filemanager script
wget https://raw.githubusercontent.com/YOUR_USERNAME/terminal-filemanager/main/filemanager

# 2. Make it executable
chmod +x filemanager

# 3. Move to PATH
sudo mv filemanager /usr/local/bin/

# 4. Run from anywhere
filemanager
```

### Verify Installation

```bash
# Check if installed correctly
which filemanager

# Should output: /usr/local/bin/filemanager
```

## 📖 Usage Guide

### Basic Navigation

```
Launch:           filemanager
Navigate:         ↑/↓ arrow keys
Open folder:      Enter
Edit file:        Enter (on text files)
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
| `Enter` | Open directory or edit file |
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

When editing a file:

```
^S (Ctrl+S):      Save file
^Q (Ctrl+Q):      Quit (with warning if modified)
^X (Ctrl+X):      Quit without saving (double confirm)
Arrow keys:       Navigate cursor
Page Up/Down:     Scroll by page
Home/End:         Jump to line start/end
Tab:              Insert 4 spaces
Backspace:        Delete character before cursor
Delete:           Delete character at cursor
Enter:            New line
```

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
3. Choose:
   - "Extract All" to extract all archives
   - Select individual archive by number
4. Press `Enter` to confirm
5. Archives extracted to folders with same name

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
- 💻 **Blue** - Code files
- 📄 **White** - Regular files

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
