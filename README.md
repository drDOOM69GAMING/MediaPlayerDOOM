<img width="3840" height="2160" alt="Screenshot from 2026-04-23 15-00-37" src="https://github.com/user-attachments/assets/77373a2e-99a6-4b47-bbda-807d44eec8b0" />


# Music Player

A Python-based graphical music player for Linux with equalizer, playlist management, system tray support, and keyboard shortcuts.

## Features

- **Multiple Audio Formats**: MP3, WAV, FLAC, M4A, OGG, WMA, AAC, AIFF, and more
- **Equalizer**: 10-band graphic equalizer with customizable presets
- **Playlist Management**: Create, save, and load playlists
- **System Tray**: Minimize to system tray with playback controls
- **Themes**: Multiple visual themes (Matrix, Cyberpunk, Dracula, Midnight, Sunset, Forest)
- **Keyboard Shortcuts**: Full keyboard control for playback
- **Metadata**: View and edit audio file metadata
- **Shuffle & Repeat**: Shuffle play and repeat modes
- **Search**: Search within your music library

## Requirements

### System Dependencies

Install the following system packages:

**Debian/Ubuntu:**
```bash
sudo apt update
sudo apt install python3 python3-pip python3-tk libsdl2-mixer-2.0-0 libsdl2-image-2.0-0 libportmidi0 libavcodec-extra ffmpeg
```

**Fedora:**
```bash
sudo dnf install python3 python3-pip python3-tkinter SDL2_mixer SDL2_image ffmpeg
```

**Arch Linux:**
```bash
sudo pacman -S python python-pip tk SDL2 ffmpeg
```

### Python Dependencies

```bash
pip install pygame mutagen pydub numpy scipy pillow pystray keyboard requests pynput
```

## Installation

### Option 1: Run from Source

1. Clone or extract the project to your desired location
2. Navigate to the project directory:
   ```bash
   cd /path/to/my_music_player
   ```
3. Install dependencies (or use the provided virtual environment):
   ```bash
   source venv/bin/activate   # If using the included venv
   pip install pygame mutagen pydub numpy scipy pillow pystray keyboard requests pynput
   ```
4. Run the player:
   ```bash
   python music_player.py
   ```

Or use the provided launcher script:
```bash
./music_player.sh
 ```

### Option 2: Use Pre-built Binary

If there's a pre-built executable in `dist/music_player`:

```bash
cd /path/to/my_music_player/dist
./music_player
```

Make it executable and optionally add to your PATH:

```bash
chmod +x /path/to/my_music_player/dist/music_player
sudo cp /path/to/my_music_player/dist/music_player /usr/local/bin/
```

Then run from anywhere:
```bash
music_player
```

## Usage

### Adding Music

1. Click **"Open Files"** or use **Ctrl+O** to add individual audio files
2. Click **"Open Folder"** or use **Ctrl+Shift+O** to add all music from a folder
3. Your library will display in the main playlist view

### Playback Controls

| Action | Button | Keyboard Shortcut |
|--------|--------|-----------------|
| Play/Pause | Play button | `Space` |
| Stop | Stop button | `s` |
| Next Track | Next button | `Right Arrow` |
| Previous Track | Prev button | `Left Arrow` |
| Volume Up | Volume slider | `Up Arrow` |
| Volume Down | Volume slider | `Down Arrow` |
| Mute/Unmute | Mute button | `m` |
| Shuffle | Shuffle button | `z` |
| Repeat | Repeat button | `x` |

### Equalizer

1. Click the **EQ** button to open the equalizer panel
2. Adjust the 10 frequency bands (32Hz to 16kHz)
3. Save custom presets for different music genres

### Playlist Management

1. Create a new playlist with **Ctrl+N**
2. Save the current playlist with **Ctrl+S**
3. Load an existing playlist with **Ctrl+L**
4. Drag and drop tracks to reorder

### System Tray

- Click the close button (X) to minimize to system tray
- Right-click the tray icon for playback controls
- Left-click to restore the window
- Enable/disable minimize to tray in settings

### Themes

Access theme options from the menu or use **Ctrl+T** to cycle through themes:
- Matrix (green terminal style)
- Cyberpunk (neon pink/cyan)
- Dracula (purple)
- Midnight (dark blue)
- Sunset (warm orange)
- Forest (earth tones)

## Troubleshooting

### "tkinter not available"
Install `python3-tk` from your package manager.

### "pygame not installed"
```bash
pip install pygame
```

### "mutagen not installed"
```bash
pip install mutagen
```

### No audio output
- Check your system volume
- Ensure audio file is not corrupted
- Verify the correct audio device is selected in system settings

### Keyboard shortcuts not working
Install the keyboard library:
```bash
pip install keyboard
```

### System tray not working
Install pystray:
```bash
pip install pystray
```

### Equalizer not working
Install numpy and scipy:
```bash
pip install numpy scipy
```

### Missing dependencies
If using the virtual environment, ensure it's activated:
```bash
source venv/bin/activate
```

## Building from Source

To build your own executable:

```bash
pip install pyinstaller
pyinstaller music_player.spec
```

The executable will be created in the `dist` directory.

## License

MIT License

## Support

For issues and feature requests, visit the project repository.
