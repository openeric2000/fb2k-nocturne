# Third-party notices

This theme package uses the works listed below. For the bundled parts, the full license texts are in the `licenses\` folder next to this file. Components that are not bundled must be downloaded from their official pages as described in the README. File locations below are relative to the foobar2000 profile folder.

## Bundled

### Columns UI 3.7.1 (modified)

- File: `user-components-x64\foo_ui_columns\foo_ui_columns.dll`
- Copyright: Copyright (c) musicmusic and contributors 2003-2025
- License: GNU Lesser General Public License v3 (`licenses\columns_ui\COPYING.LESSER`, together with the GNU GPL v3 in `licenses\columns_ui\COPYING`)
- **This is a modified version**: based on upstream v3.7.1 with 21 changes (patches 0001–0021, such as the now playing view, underlined tabs, the main menu button, freezing the seek bar while paused, the Theme Font command, and English/Chinese interface text), then rebuilt.
- Complete source code of the modified version: https://github.com/openeric2000/columns_ui (tag `fb2k-nocturne-v1.10`). Each change is one commit; `git clone --recursive` also fetches the modified ui_helpers. See that repository's README for build instructions. The English build defines `NOCTURNE_LANG_EN` (the interface text is in `foo_ui_columns\nocturne_text.h`).
- Upstream source code: https://github.com/reupen/columns_ui (tag `v3.7.1`)
- Libraries compiled into this DLL:
  - ui_helpers (**modified**: patch 0019 removes the dividers between list column headers in dark mode; source https://github.com/openeric2000/ui_helpers branch `fb2k-nocturne`), mmh, fbh: Copyright (c) Reupen Shah 2003–2017, BSD 3-Clause License (`licenses\columns_ui\ui_helpers-LICENCE`, `mmh-LICENCE`, `fbh-LICENCE`)
  - columns_ui-sdk, svg-services interfaces: Reupen Shah, 0BSD (`columns_ui-sdk-LICENCE`, `svg-services-LICENCE`)
  - foobar2000 SDK: Copyright (c) Peter Pawlowski, BSD-style license (`licenses\columns_ui\foobar2000-sdk-license.txt`)
  - pfc: Copyright (C) Peter Pawlowski, zlib-style license (`licenses\columns_ui\pfc-license.txt`)
  - {fmt}: Copyright (c) 2012 - present, Victor Zverovich and {fmt} contributors, MIT License (`fmt-LICENSE`)
  - GSL: Copyright (c) 2015 Microsoft Corporation, MIT License (`GSL-LICENSE`)
  - WIL: Copyright (c) Microsoft Corporation, MIT License (`WIL-LICENSE`)
  - lexy, range-v3: Boost Software License 1.0 (`lexy-LICENSE`, `range-v3-LICENSE`)

### Album list panel 2.2.0

- File: `user-components-x64\foo_uie_albumlist\foo_uie_albumlist.dll` (unmodified, taken from the official component package)
- Based on Album List 3.1.0 by Peter Pawlowski, maintained by reupen
- License: GNU Lesser General Public License v3 (`licenses\album_list_panel\COPYING.LESSER`, `COPYING`)
- Source code: https://github.com/reupen/album_list_panel (tag `v2.2.0`)
- Libraries compiled into this DLL: ui_helpers, mmh, fbh (BSD 3-Clause), columns_ui-sdk (0BSD), foobar2000 SDK, pfc; licenses as above

### foo_queue_mirror 1.3.0

- File: `user-components-x64\foo_queue_mirror\foo_queue_mirror.dll`
- Copyright: Copyright (c) 2026 openeric2000
- License: MIT License (`licenses\foo_queue_mirror\LICENSE`)
- Source code: https://github.com/openeric2000/foo_queue_mirror (tag `v1.3.0`)

## Not bundled, please download yourself

The authors of these components have not published a license that allows redistribution, so they are not included in this package. Please download and install them from their official pages:

| Component | Author | Download |
|-----------|--------|----------|
| foobar2000 2.x (64-bit) | Peter Pawlowski | https://www.foobar2000.org/download |
| ESLyric 1.0.7.0 or later | ESLyric | https://github.com/ESLyric/release/releases |
| WebView2 (foo_webview2) 0.3.28 or later | P. Stuer, J. Cassis | https://www.foobar2000.org/components/view/foo_webview2 |
| Playback Statistics (foo_playcount) | Peter Pawlowski | https://www.foobar2000.org/components/view/foo_playcount |
