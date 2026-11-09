# Nocturne for foobar2000

[繁體中文](https://github.com/openeric2000/fb2k-nocturne/blob/main/README.md) | **English**

A dark, streaming-style look for foobar2000: an album header on top, underlined playlist tabs, and an expandable now playing view with lyrics.

Nocturne is built around **folder structure**: I sort my music into nested folders, so the interface centers on the folder tree on the left and the album header at the top, which shows the name, artist, year, track count and total length of whichever level you click.

![Main window: folder tree, album header, playlist and playback bar](images/main-en.png)

Download: https://github.com/openeric2000/fb2k-nocturne/releases

- First installation: download the **Full** ZIP.
- You already have Nocturne: download the **Update** ZIP; see ["Updating to a new version"](#updating-to-a-new-version).

A fresh foobar2000 install is recommended. Installing on a foobar2000 you already use overwrites your interface settings, fonts and playlists, so back up first; see ["Installation"](#installation).

## Features

New in v1.40: a blurred cover background on the now playing view, thin scroll bars, a folder search box, a vinyl picture for tracks without a cover, and faster album header updates.

"Preferences page" below means File → Preferences → Tools → Nocturne; see ["Preferences page"](#preferences-page). The animations were recorded with the author's own music library and font; see ["Fonts"](#fonts) to change the font.

### Now playing view

Click the now playing bar to expand it into a now playing view with a large cover and the lyrics. Click again to collapse it.

![Expanding and collapsing the now playing view](images/expand-collapse-en.webp)

### Blurred cover background

The background of the now playing view takes on a soft, blurred version of the current cover, so every track looks different. To turn it off or dim it, go to the "Interface" tab of the preferences page.

![The blurred cover background of the now playing view](images/cover-blur-en.webp)

### Output device

The playback bar shows which device the sound is going to: an output type on the left (Default, Exclusive, ASIO, Muted) and the device name on the right. Hover over it to see the full name and the output mode; click it to switch device.

![Output device: hover for the info, click for the device list](images/output-device-en.webp)

You can rename devices (for example `Holo Audio=DAC (Holo Audio)`) or turn this off on the "Playback" tab of the preferences page.

### Mouse wheel on the progress bar

Put the mouse over the progress bar and scroll to seek: up to go forward, down to go back, 5 seconds per notch, or 30 seconds per notch while holding Shift. You can change the seconds on the "Playback" tab of the preferences page, or turn it off.

### Queue

The "Add to Queue" button in the album header adds the whole playlist to the playback queue; select some tracks first and it adds only those. The "Queue" tab shows what is in the queue: select some tracks and press "Remove Selected (N)" to take only those out; with nothing selected, press "Remove from Queue" and press again within 3 seconds to clear the whole queue.

![Adding four tracks to the queue, looking at the Queue tab, and removing one](images/queue-en.webp)

Playing another track (double-click, Enter, or right-click → Play) keeps the queue by default; to go back to foobar2000's default (playing another track clears the queue), untick the option on the "Up Next & Queue" tab of the preferences page.

### Up Next card

On the expanded now playing view, when a track is about to end, an Up Next card appears at the bottom right with the next track's cover, title, artist and a countdown; when it reaches 0, the next track starts. The countdown length, position and card size can be changed on the "Up Next & Queue" tab of the preferences page.

![The Up Next card appears near the end of a track, counts down, and the next track starts](images/up-next-en.webp)

### Preferences page

The theme's own settings are in File → Preferences → Tools → Nocturne, split into five tabs (Playback, Up Next & Queue, Fonts, Interface, About), and take effect immediately.

![The Nocturne preferences page](images/settings-en-v140.webp)

## Requirements

- Windows 10 or 11
- foobar2000 2.x **64-bit** (32-bit is not supported)
- Microsoft Edge WebView2 Runtime (built into Windows 11; most Windows 10 PCs already have it)
- An SSD is recommended. On an HDD the first launch is slower.

## Installation

The **profile folder** comes up often below: for the portable version it is the `profile` folder next to `foobar2000.exe`; for the installed version it is `%APPDATA%\foobar2000-v2` (paste it into the File Explorer address bar and press Enter to open it).

Find your situation first:

| Your situation | What to do |
|----------------|------------|
| A fresh foobar2000 (recommended) | Follow [Steps 1-4](#step-1-install-foobar2000-and-three-required-components-do-this-first) below |
| A foobar2000 you already use, without Nocturne | **Back up the profile folder first**, then follow [Steps 1-4](#step-1-install-foobar2000-and-three-required-components-do-this-first). Your interface settings are replaced by the theme's; see ["Installing on a foobar2000 you already use"](#installing-on-a-foobar2000-you-already-use) |
| Nocturne already installed (for example v1.30), and you want a newer version in the same language | Download the Update ZIP and see ["Updating to a new version"](#updating-to-a-new-version) |
| Switching from the Chinese version to the English one (or the other way round) | Overwrite everything with the Full ZIP (as in [Step 2](#step-2-close-foobar2000-and-copy-the-zip-contents-into-the-profile-folder)). Do not use the Update ZIP, or the now playing bar will be blank |

### Step 1: Install foobar2000 and three required components (do this first)

The authors of these three components do not allow redistribution, so they are not included. Please download them from their official pages.

**Install all three and restart foobar2000 before going on to [Step 2](#step-2-close-foobar2000-and-copy-the-zip-contents-into-the-profile-folder).** If any of them is missing, the lyrics, album header or play counts will not show.

1. Install foobar2000 2.x 64-bit: https://www.foobar2000.org/download (installer or portable both work)
2. Download the three components (all are `.fb2k-component` files):

   | Component | Used for | Download | Tested version |
   |-----------|----------|----------|----------------|
   | ESLyric | Now playing bar, now playing view, lyrics | https://github.com/ESLyric/release/releases | 1.0.7.0 (older versions do not work) |
   | WebView2 (foo_webview2) | Album header at the top | https://www.foobar2000.org/components/view/foo_webview2 | 0.3.28 |
   | Playback Statistics (foo_playcount) | Plays column, "Recently Played" and "Not Played in 6 Months" playlists | https://www.foobar2000.org/components/view/foo_playcount | 3.1.11 |

   **If you already have ESLyric, check its version too**: below 1.0.7.0, the icons in the now playing bar show as empty boxes and there is no play button. Install the new version as in item 3 below.

3. Open foobar2000 → File → Preferences → Components → click "Install..." and pick each downloaded `.fb2k-component`. After adding all three, click OK and restart foobar2000 when asked.
4. After the restart, go back to Preferences → Components and check that ESLyric, WebView2 and Playback Statistics are all listed.

### Step 2: Close foobar2000 and copy the ZIP contents into the profile folder

(This step uses the Full ZIP.)

1. File → Exit to close foobar2000.
2. Open the profile folder (see the start of ["Installation"](#installation) above).
3. In File Explorer, double-click the ZIP to open it → Ctrl+A → Copy → go back to the profile folder and paste. When asked about existing files, choose "Replace the files in the destination".

After copying, folders such as `user-components-x64`, `configuration`, `eslyric-data` and `webview` should be directly inside the profile folder. If they ended up one folder deeper, the theme will not work. The `Docs` folder only contains this guide and the license files; you can keep or delete it.

### Step 3: Open foobar2000 and switch to the theme

1. Open foobar2000. Because a new user interface component was added, foobar2000 asks which user interface to use. Choose Columns UI.
2. If a "Quick setup – Columns UI" window appears, **just click Cancel** and do not pick any layout in it. Picking a layout and clicking OK replaces the theme's layout.

### Step 4: Add your music folders

File → Preferences → Media Library → click "Add..." and add your music folders. The folder tree on the left follows your folder structure.

### Lyrics: where they come from, where they are saved, where to change settings

The ESLyric settings are already tuned for you (they are installed together with the theme), and lyrics are searched for automatically during playback:

1. First, lyric files on your computer: in the same folder as the song, or in the `lyrics` folder inside the profile folder.
2. Only if nothing is found, ESLyric goes online and searches NetEase Cloud Music, Kugou, QQ Music, NetEase English, LRCLIB, MiniLyrics and Musixmatch. **This sends the song title and artist to those services**; how to turn it off is below.

Synced lyrics that are found are saved automatically to the `lyrics` folder inside the profile folder. Nothing to set up:

- Portable: `foobar2000\profile\lyrics\`
- Installed: `%APPDATA%\foobar2000-v2\lyrics\`

To change the lyric settings, go to File → Preferences → Tools → ESLyric:

- Do not want online searches: under "Lyric Options" turn off "Automatically search on playback start", or untick the sources you do not want under "Lyric Sources" (the built-in "Local File" source only reads lyric files on your computer).
- Want more lyric sources: "Get More..." at the top right of the "Lyric Sources" page.
- Where lyrics are saved and when: "Save Settings".

## Installing on a foobar2000 you already use

You can, but know this first: in [Step 2](#step-2-close-foobar2000-and-copy-the-zip-contents-into-the-profile-folder), when you copy the ZIP contents and choose "Replace the files in the destination", your current interface settings are replaced with the theme's. So back up first.

### Back up first

1. File → Exit to close foobar2000.
2. Copy the whole profile folder to somewhere else.
3. To go back later, close foobar2000, copy the backup back into the profile folder and choose "Replace" when asked.

### What gets replaced

- **Interface settings**: the Columns UI layout, the playlist columns, colours, the status bar and so on are replaced with the theme's. If you already use Columns UI and have customized the layout, your changes will be gone (an official Columns UI you installed is simply replaced by the theme's modified one; they do not conflict).
- **Fonts**: the fonts of the lists, tabs, folder tree, now playing bar, now playing view and album header go back to the theme's default, Segoe UI. To use another font, see ["Fonts"](#fonts).
- **Album list settings**.
- **ESLyric settings**: the lyric sources and their order, the search and save settings, the desktop lyric and so on are replaced with the theme's. Lyrics are now saved to the `lyrics` folder inside the profile folder; lyric files you kept somewhere else are not deleted, but ESLyric no longer looks there or saves there. To keep your own ESLyric settings, choose "Skip" for the file `configuration\foo_uie_eslyric.dll.cfg` when copying the ZIP contents, **and do not copy** the `eslyric-data\scripts` folder (if you skip only the settings file but copy the scripts, the 7 online sources appear at the end of your source list, ticked).
- **Album header page**: if you put your own page in `webview\default\` in the profile folder, it is replaced by the theme's.
- **Playlists**: the five playlists that come with the theme (Selected Folder, Queue, Recently Added, Recently Played, Not Played in 6 Months) go back to their defaults. Other playlists you made are not deleted, but they no longer appear in the playlist tabs (restoring your backup brings them back).

### What is not affected

- foobar2000's own settings: output device, media library folders, keyboard shortcuts, DSP and so on.
- Your media library and play counts.
- The lyric files you have already saved (but your ESLyric settings are replaced, see above).
- The settings of other components.

### If you do not want to touch your current foobar2000

Install a separate portable foobar2000 and try the theme there. The one you use now is not touched at all.

## Updating to a new version

If you already have Nocturne and want a newer version **in the same language**, download the Update ZIP (its name contains `update`, for example `fb2k-nocturne-v1.40-update-en.zip`) and extract it over your profile folder:

1. File → Exit to close foobar2000.
2. **Back up the `configuration` folder in your profile folder** (see the start of ["Installation"](#installation)).
3. In File Explorer, double-click the Update ZIP to open it → Ctrl+A → Copy → paste into the profile folder. When asked about existing files, choose "Replace the files in the destination". (File Explorer merges the folders and only replaces files with the same name, so your other components and files are not deleted.)
4. Start foobar2000 again.

Replaced with the new version:

- The three components (Columns UI, Album list, foo_queue_mirror).
- ESLyric: the layout `main.xml`, the online lyric source scripts and the ESLyric settings file.
- The album header page (`webview`).
- **The Columns UI settings file `configuration\foo_ui_columns.dll.cfg` (since v1.40)**: the layout, playlist columns, fonts and colours, and every option on the preferences page. New features such as the blurred cover background keep their settings here and do not work without it.
- The vinyl picture shown for tracks without a cover, `no-cover.png` (new).

Not touched: your playlists, the media library, foobar2000's core settings (output device, volume, keyboard shortcuts, the no-cover stub setting), Album list's own settings file, your lyric files and other components.

Notes:

- **To keep your own Columns UI settings**, choose "Skip this file" for `configuration\foo_ui_columns.dll.cfg` while copying. The cost: no blurred cover background and the old playlist columns; the other new features work as usual.
- If you have edited `main.xml` or picked other fonts, do it again after updating: the fonts of the now playing bar, now playing view and album header go back to the default. Choose them again on the "Fonts" tab of the preferences page.
- Your ESLyric settings are replaced with the theme's (including the 7 online lyric sources). To stop online lyric searches, see ["Lyrics"](#lyrics-where-they-come-from-where-they-are-saved-where-to-change-settings); to keep your own ESLyric settings, see ["What gets replaced"](#what-gets-replaced).
- To switch language (Chinese version to English, or the other way round), do not use the Update ZIP, or the now playing bar will be blank. Overwrite everything with the Full ZIP as described in ["Installing on a foobar2000 you already use"](#installing-on-a-foobar2000-you-already-use), after making a backup. Do the same if you are not sure.

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

Use the "Fonts" tab of the preferences page:

- The top row, "All parts", changes everything at once.
- Playlist, Playlist tabs, Folder tree, Other interface text: both the font and the size can be changed, and it is applied immediately.
- Now playing bar and view, Album header: only the font can be changed (the size is fixed), it takes effect after restarting foobar2000, and a "Restart now" button appears at the bottom of the tab once you change one.

You can also change everything at once from the main menu View → Layout → Theme Font… (also under the ☰ button at the top left → View → Layout) and pick an overall size (Small / Standard / Large / Extra Large, which only scales the lists, tabs and folder tree). Click "Yes" to restart when asked.

### Lyrics font

The lyrics font is not set here but in ESLyric:

- Lyrics: right-click the lyrics → Panel Options....
- Desktop lyric (off by default): File → Preferences → Tools → ESLyric → Desktop Lyric → Display settings.

## Tips

### A keyboard shortcut that jumps to the playing track

Give foobar2000's "Activate now playing" a keyboard shortcut and one key press finds and selects the playing track in a long playlist. This is foobar2000's own setting, so set it up once yourself (the example uses `F4`):

1. File → Preferences → Keyboard Shortcuts, then click "Add new".
2. In the Action section, type `Activate now playing` into "Filter list by", then click View → Playlist view → Activate now playing in the list.
3. Click the Key field at the bottom and press the key you want, then click Apply → OK.

![Keyboard Shortcuts: assigning F4 to Activate now playing](images/keyboard-shortcut-activate-now-playing.png)

## Notes

- **Do not replace Columns UI through foobar2000's component updates.** This theme uses a modified Columns UI; the official version lacks the now playing view, the underlined tabs and other features.
- **The same goes for Album list (since v1.40).** The theme ships a modified version; the official one lacks the new search box and the "Search Album list" command. Put the file from the ZIP back if that happens.
- To go back to plain foobar2000: delete the whole profile folder, then reinstall or re-extract the official version.

## License

- The theme itself (ESLyric layout and settings file, album header page, settings files, default playlists, documentation): MIT License, see [LICENSE](LICENSE)
- The bundled ESLyric lyric source scripts come from the official ESLyric script repository and have no license of their own; see [THIRD-PARTY-NOTICES.en.md](THIRD-PARTY-NOTICES.en.md) for their origin and details
- The modified Columns UI and the other bundled components: see [THIRD-PARTY-NOTICES.en.md](THIRD-PARTY-NOTICES.en.md)
