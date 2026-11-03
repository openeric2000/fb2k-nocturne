# Nocturne for foobar2000

[繁體中文](https://github.com/openeric2000/fb2k-nocturne/blob/main/README.md) | **English**

A dark, streaming-style look for foobar2000: an album header on top, underlined playlist tabs, and an expandable now playing view with lyrics.

Nocturne is built around **folder structure**. I sort my music into nested folders, so the interface centers on two things: the folder tree on the left and the album header at the top. Click any level and the header shows that level's name, plus the artist, year, track count and total length ([see the demo](https://openeric2000.github.io/fb2k-nocturne/), which uses fake data). The expandable now playing view, the lyrics and the Up Next card make listening look and feel good, too.

Download: https://github.com/openeric2000/fb2k-nocturne/releases

- First installation: download the **Full** ZIP, `fb2k-nocturne-v1.20-en.zip` (English) or `fb2k-nocturne-v1.20-zh-TW.zip` (Traditional Chinese).
- You already have Nocturne and only want a newer version: download the **Update** ZIP, `fb2k-nocturne-v1.20-update-en.zip` (English) or `fb2k-nocturne-v1.20-update-zh-TW.zip` (Traditional Chinese). Your playlists and other settings stay; the ESLyric settings are replaced with the theme's. See ["Updating to a new version"](#updating-to-a-new-version).

A fresh foobar2000 install is recommended. Installing on a foobar2000 you already use overwrites your interface settings, fonts and playlists, so back up first; see ["Installation"](#installation).

## Features

### Now playing view

Click the now playing bar to expand it into a now playing view with a large cover and the lyrics. Click again to collapse it.

### Queue

The "Add to Queue" button in the album header adds the whole playlist to the playback queue in order. Select some tracks in the list first and the button becomes "Add Selected (N)" and adds only those. The "Queue" tab shows what is in the queue; select some tracks there and press "Remove from Queue" to take them out.

Playing another track (double-click, Enter, or right-click → Play) keeps the queue instead of clearing it. To go back to foobar2000's default behavior, uncheck the option under "Playback queue" on the "Up Next Notice" tab in the settings.

### Up Next card

On the expanded now playing view, when a track is about to end (the last 10 seconds by default), an Up Next card appears at the bottom right with the next track's cover, title, artist and a countdown. When the countdown ends, the next track starts. If the next track is one you added to the queue, the card says so. You can adjust the details on the "Up Next Notice" tab in the settings.

## Requirements

- Windows 10 or 11
- foobar2000 2.x **64-bit** (32-bit is not supported)
- Microsoft Edge WebView2 Runtime (built into Windows 11; most Windows 10 PCs already have it)

## Installation

The **profile folder** comes up often below: for the portable version it is the `profile` folder next to `foobar2000.exe`; for the installed version it is `%APPDATA%\foobar2000-v2` (paste it into the File Explorer address bar and press Enter to open it).

Find your situation first:

| Your situation | What to do |
|----------------|------------|
| A fresh foobar2000 (recommended) | Follow [Steps 1-4](#step-1-install-foobar2000-and-three-required-components-do-this-first) below |
| A foobar2000 you already use, without Nocturne | **Back up the profile folder first**, then follow [Steps 1-4](#step-1-install-foobar2000-and-three-required-components-do-this-first) (ESLyric must be 1.0.7.0 or newer; update it first if it is older). Your interface settings, fonts, Album list settings, ESLyric settings and playlists are replaced by the theme's; see ["Installing on a foobar2000 you already use"](#installing-on-a-foobar2000-you-already-use) |
| Nocturne already installed (for example v1.10), and you want a newer version in the same language | Download the Update ZIP and see ["Updating to a new version"](#updating-to-a-new-version): your playlists and other settings stay (the ESLyric settings are replaced with the theme's) |
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

   **If you already have ESLyric, check its version too**: below 1.0.7.0 (for example 1.0.6.2), the icons in the now playing bar show as empty boxes and there is no play button. Install the new version again as in Step 3 below.

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

### Optional: a keyboard shortcut that jumps to the playing track

In a long playlist it can be hard to see which track is playing. You can give foobar2000's "Activate now playing" a keyboard shortcut; one key press finds the playing track in the list and selects it. Shortcuts are foobar2000's own settings, so the theme does not assign one for you. Set it up once (the example below uses `F4`; use any key you like):

1. File → Preferences → Keyboard Shortcuts, then click "Add new".
2. In the Action section, type `Activate now playing` into "Filter list by", then click View → Playlist view → Activate now playing in the list.
3. Click the Key field at the bottom and press the key you want (`F4` in the example), then click Apply → OK.

![Keyboard Shortcuts: assigning F4 to Activate now playing](images/keyboard-shortcut-activate-now-playing.png)

## Installing on a foobar2000 you already use

You can, but know this first: in [Step 2](#step-2-close-foobar2000-and-copy-the-zip-contents-into-the-profile-folder), when you copy the ZIP contents and choose "Replace the files in the destination", your current interface settings are replaced with the theme's. So back up first.

### Back up first

1. File → Exit to close foobar2000.
2. Copy the whole profile folder to somewhere else.
3. To go back later, close foobar2000, copy the backup back into the profile folder and choose "Replace" when asked.

### What gets replaced

- **Interface settings**: the Columns UI layout, the playlist columns, colours, the status bar and so on are replaced with the theme's. If you already use Columns UI and have customized the layout, your changes will be gone (an official Columns UI you installed is simply replaced by the theme's modified one; they do not conflict).
- **Fonts**: the fonts of the lists, tabs, folder tree, now playing bar, now playing view and album header go back to the theme's default, Segoe UI. To use another font, choose it again in View → Layout → Theme Font….
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

If you already have Nocturne and want a newer version **in the same language**, download the Update ZIP (its name contains `update`, for example `fb2k-nocturne-v1.20-update-en.zip`). It contains the theme's own files and the complete ESLyric settings (layout, online lyric source scripts, ESLyric settings file), and does not contain your playlists or the settings of the other components, so you can simply extract it over your profile folder:

1. File → Exit to close foobar2000.
2. Open the profile folder (see the start of ["Installation"](#installation)).
3. In File Explorer, double-click the Update ZIP to open it → Ctrl+A → Copy → paste into the profile folder. When asked about existing files, choose "Replace the files in the destination". (File Explorer merges the folders and only replaces files with the same name, so your other components and files are not deleted.)
4. Start foobar2000 again.

The Update ZIP replaces: `user-components-x64` (the DLLs of the three components), `eslyric-data` (the layout `main.xml` and the online lyric source scripts), `webview` (the album header page) and `configuration\foo_uie_eslyric.dll.cfg` (the ESLyric settings). The other settings files in `configuration` and `playlists-v2.0` are not in it, so your playlists and Columns UI settings stay as they are.

Notes:

- The fonts of the now playing bar, now playing view and album header go back to the default, because they are stored in `main.xml` and `index.html`. Choose your font again in View → Layout → Theme Font… (the fonts of the lists, tabs and folder tree are not affected).
- What is inside the settings files is not updated. When updating from v1.10 to this version, that applies to the display script of the first playlist column (▶): it keeps working without the update; the only difference is that after you switch folders with Album list and back, newly added tracks may not show ▶. To switch to the new script: File → Preferences → Display → Columns UI → Playlist view → "Columns" tab, select the first column (▶), open the "Display script" tab, replace the content with the line below, click Apply in that section, then OK:

  `$if($or(%isplaying%,%cui_now_playing_file%),$if(%ispaused%,❚❚,▶),[%queue_indexes%])`

- Your ESLyric settings are replaced with the theme's, including the 7 online lyric sources and their order, the search and save settings, the desktop lyric and so on. When no local lyrics are found, ESLyric goes online during playback; how to turn that off is described above in ["Lyrics: where they come from, where they are saved, where to change settings"](#lyrics-where-they-come-from-where-they-are-saved-where-to-change-settings). To keep your own ESLyric settings, see the ESLyric item under ["What gets replaced"](#what-gets-replaced) above.
- To switch language (Chinese version to English, or the other way round), do not use the Update ZIP. Overwrite everything with the Full ZIP (after making a backup). The settings files still remember the names of the other language, so replacing only the theme files leaves the now playing bar blank.
- If you are not sure, overwrite everything with the Full ZIP as described in ["Installing on a foobar2000 you already use"](#installing-on-a-foobar2000-you-already-use) above, after making a backup.

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

1. Main menu View → Layout → Theme Font… (also available from the ☰ button at the top left → View → Layout).
2. Pick a font and an overall size → OK. The lists, tabs, folder tree, now playing bar, now playing view and album header all change together.
3. When the message appears, click "Yes" to restart foobar2000 so the now playing bar and album header pick up the new font.
4. The lyrics font is set separately: right-click the lyrics → Panel Options... and change the font there.
5. The desktop lyric (off by default) has its own font: File → Preferences → Tools → ESLyric → Desktop Lyric → Display settings.

- The weight is always Regular.
- The overall size (Small / Standard / Large / Extra Large) only scales the lists, tabs and folder tree; the now playing bar and album header keep their size. Choose "Standard" to go back to the theme's original size.

To fine-tune individual items, go to File → Preferences → Display → Columns UI → Colours and fonts → Fonts. When you change the font family there, the style below jumps to the first entry in the list (often Light), so remember to set it back to Regular.

## Notes

- **Do not replace Columns UI through foobar2000's component updates.** This theme uses a modified Columns UI; the official version lacks the now playing view, the underlined tabs and other features.
- To go back to plain foobar2000: delete the whole profile folder, then reinstall or re-extract the official version.
- So far tested only on Windows 10 (Traditional Chinese edition) with foobar2000 2.26.1. Not yet tested on English Windows or on Windows 11 (where the Segoe MDL2 Assets font used by the now playing bar icons and the ☰ button has not been checked).

## License

- The theme itself (ESLyric layout and settings file, album header page, settings files, default playlists, documentation): MIT License, see [LICENSE](LICENSE)
- The bundled ESLyric lyric source scripts come from the official ESLyric script repository and have no license of their own; see [THIRD-PARTY-NOTICES.en.md](THIRD-PARTY-NOTICES.en.md) for their origin and details
- The modified Columns UI and the other bundled components: see [THIRD-PARTY-NOTICES.en.md](THIRD-PARTY-NOTICES.en.md)
