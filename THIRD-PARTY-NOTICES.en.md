# Third-party notices

This theme package uses the works listed below. For the bundled parts, the full license texts are in the `licenses\` folder next to this file. Components that are not bundled must be downloaded from their official pages as described in the README. File locations below are relative to the foobar2000 profile folder.

## Bundled

### Columns UI 3.7.1 (modified)

- File: `user-components-x64\foo_ui_columns\foo_ui_columns.dll`
- Copyright: Copyright (c) musicmusic and contributors 2003-2025
- License: GNU Lesser General Public License v3 (`licenses\columns_ui\COPYING.LESSER`, together with the GNU GPL v3 in `licenses\columns_ui\COPYING`)
- **This is a modified version**: based on upstream v3.7.1 with changes, then rebuilt. Examples: the now playing view, underlined tabs, the main menu button, freezing the seek bar while paused, the Theme Font command, English/Chinese interface text, and, new in v1.20, the Up next toast, the Stopped screen, the Stop button that closes the now playing view, keeping the playback queue when you play another track, and improvements to the progress bar; v1.40 adds the blurred cover background of the now playing view, thin scroll bars, pointing foobar2000 at the bundled vinyl picture for tracks without a cover, and a reorganized preferences page; v1.50 adds switching what the now playing view shows (VU meter, spectrum), the track info card and the zoom button for the large cover, locking the lyrics against dragging, self-drawn tooltips, one look for notice cards, and the new stop behaviour of the now playing view.
- Complete source code of the modified version: https://github.com/openeric2000/columns_ui (tag `fb2k-nocturne-v1.50`; v1.40 shipped with tag `fb2k-nocturne-v1.40`, v1.30 with `fb2k-nocturne-v1.30`, v1.20 with `fb2k-nocturne-v1.20`, v1.10 with `fb2k-nocturne-v1.10`). The changes are in the commit history, one or a few commits per feature; `git clone --recursive` also fetches the modified ui_helpers. See that repository's README for build instructions. The English build defines `NOCTURNE_LANG_EN` (the interface text is in `foo_ui_columns\nocturne_text.h`).
- Upstream source code: https://github.com/reupen/columns_ui (tag `v3.7.1`)
- Libraries compiled into this DLL:
  - ui_helpers (**modified**: in dark mode the dividers between list column headers are only shown for the column under the mouse; v1.40 adds thin scroll bars for lists, v1.50 adds box selection in lists; source https://github.com/openeric2000/ui_helpers branch `fb2k-nocturne`, tag `fb2k-nocturne-v1.50`), mmh, fbh: Copyright (c) Reupen Shah 2003–2017, BSD 3-Clause License (`licenses\columns_ui\ui_helpers-LICENCE`, `mmh-LICENCE`, `fbh-LICENCE`)
  - columns_ui-sdk, svg-services interfaces: Reupen Shah, 0BSD (`columns_ui-sdk-LICENCE`, `svg-services-LICENCE`)
  - foobar2000 SDK: Copyright (c) Peter Pawlowski, BSD-style license (`licenses\columns_ui\foobar2000-sdk-license.txt`)
  - pfc: Copyright (C) Peter Pawlowski, zlib-style license (`licenses\columns_ui\pfc-license.txt`)
  - {fmt}: Copyright (c) 2012 - present, Victor Zverovich and {fmt} contributors, MIT License (`fmt-LICENSE`)
  - GSL: Copyright (c) 2015 Microsoft Corporation, MIT License (`GSL-LICENSE`)
  - WIL: Copyright (c) Microsoft Corporation, MIT License (`WIL-LICENSE`)
  - lexy, range-v3: Boost Software License 1.0 (`lexy-LICENSE`, `range-v3-LICENSE`)

### Album list panel 2.2.0 (modified, since v1.40)

- File: `user-components-x64\foo_uie_albumlist\foo_uie_albumlist.dll`
- Based on Album List 3.1.0 by Peter Pawlowski, maintained by reupen
- License: GNU Lesser General Public License v3 (`licenses\album_list_panel\COPYING.LESSER`, `COPYING`)
- **This is a modified version**: based on upstream v2.2.0 with changes, then rebuilt: the search box look (rounded, magnifier, clear button), a new main menu command "Search Album list", thin scroll bars for the folder tree, and English/Chinese search box hint text; v1.50 adds hiding instrumental versions in the "Selected Folder" playlist, a choice of search box position, and auto-hiding thin scroll bars. v1.30 and earlier shipped the unmodified official version.
- Complete source code of the modified version: https://github.com/openeric2000/album_list_panel (branch `fb2k-nocturne`, tag `fb2k-nocturne-v1.50`). The changes are in the commit history; the English build defines `NOCTURNE_LANG_EN`.
- Upstream source code: https://github.com/reupen/album_list_panel (tag `v2.2.0`)
- Libraries compiled into this DLL: ui_helpers, mmh, fbh (BSD 3-Clause), columns_ui-sdk (0BSD), foobar2000 SDK, pfc; licenses as above

### foo_queue_mirror 1.3.2

- File: `user-components-x64\foo_queue_mirror\foo_queue_mirror.dll`
- Copyright: Copyright (c) 2026 openeric2000
- License: MIT License (`licenses\foo_queue_mirror\LICENSE`)
- Source code: https://github.com/openeric2000/foo_queue_mirror (tag `v1.3.2`)

### ESLyric lyric source and parser scripts

- Files: `eslyric-data\scripts\searcher\` (kugou.js, lrclib.js, minilyrics.js, musixmatch.js, netease.js, netease_en.js, qqmusic.js), `eslyric-data\scripts\parser\` (krc.js, qrc.js, srt.js), `eslyric-data\scripts\lib\`
- Origin: the official ESLyric script repository https://github.com/ESLyric/scripts (the "Get More..." button in the ESLyric settings downloads from there too), unmodified. The authors named in the file headers are ohyeah, wistaria, anonymous and TT (https://github.com/TT-ReBORN; lrclib, minilyrics, musixmatch and netease_en contain his changes or rewrites). The scripts also credit Binaryify/NeteaseCloudMusicApi, jsososo/QQMusicApi, xmcp/QRCD and olee/minilyrics-proxy.
- **License: neither these scripts nor the official ESLyric script repository come with a license, and the authors have not explicitly allowed redistribution.** They are included only so that users do not have to hunt for scripts themselves; they will be removed immediately if an author asks. If you prefer not to use them, delete the whole `eslyric-data\scripts` folder and download scripts yourself with "Get More..." in the ESLyric settings when you need them.
- Libraries used by the scripts (`lib\`, only the files needed at run time):
  - crypto-es: Copyright (c) 2018-2020 LIN Chen, MIT License (`licenses\eslyric-scripts\crypto-es-LICENSE`)
  - himalaya: Copyright (c) 2017 Chris Andrejewski, ISC License (`licenses\eslyric-scripts\himalaya-LICENSE`)
  - querystring: Copyright (c) 2013 Greg Allen, MIT License (`licenses\eslyric-scripts\querystring-LICENSE`)
  - parser_ext.so: an extension module for parsing QRC lyrics (the header of `qrc.js` names wistaria as the author); no license information
- These scripts contact the servers of NetEase Cloud Music, Kugou, QQ Music, LRCLIB, MiniLyrics and Musixmatch to search for lyrics; see the README for details.

## Not bundled, please download yourself

The authors of these components have not published a license that allows redistribution, so they are not included in this package. Please download and install them from their official pages:

| Component | Author | Download |
|-----------|--------|----------|
| foobar2000 2.x (64-bit) | Peter Pawlowski | https://www.foobar2000.org/download |
| ESLyric 1.0.7.0 or later | ESLyric | https://github.com/ESLyric/release/releases |
| WebView2 (foo_webview2) 0.3.28 or later | P. Stuer, J. Cassis | https://www.foobar2000.org/components/view/foo_webview2 |
| Playback Statistics (foo_playcount) | Peter Pawlowski | https://www.foobar2000.org/components/view/foo_playcount |
