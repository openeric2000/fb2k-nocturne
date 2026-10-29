# Nocturne for foobar2000

[繁體中文](https://github.com/openeric2000/fb2k-nocturne/blob/main/README.md) | **English**

A dark, streaming-style look for foobar2000: an album header on top, underlined playlist tabs, and an expandable now playing view with lyrics.

Download: https://github.com/openeric2000/fb2k-nocturne/releases (English: `fb2k-nocturne-v1.10-en.zip`; Traditional Chinese: `fb2k-nocturne-v1.10-zh-TW.zip`)

> **For a fresh foobar2000 install only.** The ZIP overwrites the interface settings. If you have already customized your foobar2000 interface, back up the whole profile folder first.

## Requirements

- Windows 10 or 11
- foobar2000 2.x **64-bit** (32-bit is not supported)
- Microsoft Edge WebView2 Runtime (built into Windows 11; most Windows 10 PCs already have it)

## Installation

### Step 1: Install foobar2000 and three required components (do this first)

The authors of these three components do not allow redistribution, so they are not included. Please download them from their official pages.

**Install all three and restart foobar2000 before going on to Step 2.** If any of them is missing, the lyrics, album header or play counts will not show.

1. Install foobar2000 2.x 64-bit: https://www.foobar2000.org/download (installer or portable both work)
2. Download the three components (all are `.fb2k-component` files):

   | Component | Used for | Download | Tested version |
   |-----------|----------|----------|----------------|
   | ESLyric | Now playing bar, now playing view, lyrics | https://github.com/ESLyric/release/releases | 1.0.7.0 |
   | WebView2 (foo_webview2) | Album header at the top | https://www.foobar2000.org/components/view/foo_webview2 | 0.3.28 |
   | Playback Statistics (foo_playcount) | Plays column, "Recently Played" and "Not Played in 6 Months" playlists | https://www.foobar2000.org/components/view/foo_playcount | 3.1.11 |

3. Open foobar2000 → File → Preferences → Components → click "Install..." and pick each downloaded `.fb2k-component`. After adding all three, click OK and restart foobar2000 when asked.
4. After the restart, go back to Preferences → Components and check that ESLyric, WebView2 and Playback Statistics are all listed.

### Step 2: Close foobar2000 and copy the ZIP contents into the profile folder

1. File → Exit to close foobar2000.
2. Open the foobar2000 profile folder:
   - Portable: the `profile` folder next to `foobar2000.exe`
   - Installed: paste `%APPDATA%\foobar2000-v2` into the File Explorer address bar and press Enter
3. In File Explorer, double-click the ZIP to open it → Ctrl+A → Copy → go back to the profile folder and paste. When asked about existing files, choose "Replace the files in the destination".

After copying, folders such as `user-components-x64`, `configuration`, `eslyric-data` and `webview` should be directly inside the profile folder. If they ended up one folder deeper, the theme will not work. The `Docs` folder only contains this guide and the license files; you can keep or delete it.

### Step 3: Open foobar2000 and switch to the theme

1. Open foobar2000. Because a new user interface component was added, foobar2000 asks which user interface to use. Choose **Columns UI**.
2. If a "Quick setup – Columns UI" window appears, **just click Cancel** and do not pick any layout in it. Picking a layout and clicking OK replaces the theme's layout.

### Step 4: Add your music folders

File → Preferences → Media Library → click "Add..." and add your music folders. The folder tree on the left follows your folder structure.

### Where lyrics are saved

Lyrics found during playback are saved automatically to the `lyrics` folder inside the foobar2000 profile folder. Nothing to set up:

- Portable: `foobar2000\profile\lyrics\`
- Installed: `%APPDATA%\foobar2000-v2\lyrics\`

## Fonts

The theme uses **Segoe UI**, which comes with Windows, so there is nothing to install. Segoe UI does not include Chinese or Japanese characters. If your library has many Chinese or Japanese titles, switch to one of the recommended fonts below.

### Recommended fonts

These free fonts cover both Chinese and Japanese well. Tested against about 100,000 Chinese and Japanese song and folder names, each is missing fewer than 0.2% of the characters:

| Font | Style | Missing | Download |
|------|-------|---------|----------|
| LXGW WenKai TC | Handwritten Kai style, matches the theme best (recommended) | 0.17% | https://github.com/lxgw/LxgwWenkaiTC/releases |
| Chiron Hei HK | Sans-serif, clean and easy to read | 0.06% | https://github.com/chiron-fonts/chiron-hei-hk/releases |
| Chiron GoRound TC | Rounded, softer look | 0.19% | https://github.com/chiron-fonts/chiron-go-round-tc/releases |

After downloading, right-click the font file → "Install" (or "Install for all users"), then change the theme font as described below.

### Changing the theme font

1. Main menu **View → Layout → Theme Font…** (also available from the ☰ button at the top left → View → Layout).
2. Pick a font and an overall size → OK. The lists, tabs, folder tree, now playing bar, now playing view and album header all change together.
3. When the message appears, click "Yes" to restart foobar2000 so the now playing bar and album header pick up the new font.
4. **The lyrics font is set separately**: right-click the lyrics → **Panel Options...** and change the font there.

- The weight is always Regular.
- The overall size (Small / Standard / Large / Extra Large) only scales the lists, tabs and folder tree; the now playing bar and album header keep their size. Choose "Standard" to go back to the theme's original size.

To fine-tune individual items, go to File → Preferences → Display → Columns UI → Colours and fonts → Fonts. When you change the font family there, the style below jumps to the first entry in the list (often Light), so remember to set it back to Regular.

## Notes

- **Do not replace Columns UI through foobar2000's component updates.** This theme uses a modified Columns UI; the official version lacks the now playing view, the underlined tabs and other features.
- To go back to plain foobar2000: delete the whole profile folder, then reinstall or re-extract the official version.
- So far tested only on Windows 10 (Traditional Chinese edition) with foobar2000 2.26.1. Not yet tested on English Windows or on Windows 11 (where the Segoe MDL2 Assets font used by the now playing bar icons and the ☰ button has not been checked).

## License

- The theme itself (ESLyric layout, album header page, settings files, default playlists, documentation): MIT License, see [LICENSE](LICENSE)
- The modified Columns UI and the other bundled components: see [THIRD-PARTY-NOTICES.en.md](THIRD-PARTY-NOTICES.en.md)
