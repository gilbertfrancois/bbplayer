## BLiTzBLiT Player (`bbplayer`)

_Gilbert Francois Duivesteijn_

A lightweight, Vim-navigable terminal TUI for streaming internet radio and SoundCloud playlists, powered by Python, `ncurses`, and `ffplay`.

### Key Features

- ⌨️ **Vim-Style Navigation:** Effortlessly browse your stations and tracks using standard `j`, `k`, `gg`, and `G` keystrokes.
- ⚙️ **TOML-Driven Configuration:** Manage your audio sources seamlessly by adding standard `label` and `url` pairs to a simple `stations.toml` file.
- ☁️ **Smart SoundCloud Playback:** Instead of fighting flaky CDN streams, `bbplayer` uses `yt-dlp` to resolve, cache, and play tracks from a local temp file for skip-free listening.
- 🔄 **Auto-Advance Toggle:** Keep the music flowing. Toggle continuous playback for SoundCloud tracklists with a single keypress.

### Controls

| Key        | Action                                      |
| :--------- | :------------------------------------------ |
| `j` / `k`  | Move down / up                              |
| `gg` / `G` | Jump to top / bottom                        |
| `Enter`    | Select and play station/track               |
| `c`        | Toggle continuous auto-advance (SoundCloud) |

### Installation

Copy bbplayer to e.g. `/usr/local/bin` or `$HOME/.local/bin` and create your stations.toml file in `$XDG_CONFIG_HOME/bbplayer`, usually `$HOME/.config/bbplayer`

`bbplayer` requires `ffmpeg` (which provides `ffplay`) and `yt-dlp` to handle background streaming and media resolution.

**Fedora:**

```bash
sudo dnf install ffmpeg yt-dlp
```

**Ubuntu**:

```bash
sudo apt install ffmpeg yt-dlp
```
