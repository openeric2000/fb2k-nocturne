# 第三方授權說明

這個主題套件用到下面這些別人的作品。隨包附上的部分，授權全文放在這份文件旁邊的 `licenses\` 資料夾；沒有隨包附上的元件，請照 README 到官方網站下載。下面的檔案位置都是 fb2k 設定資料夾裡的位置。

## 隨包附上

### Columns UI 3.7.1（修改版）

- 檔案：`user-components-x64\foo_ui_columns\foo_ui_columns.dll`
- 版權：Copyright (c) musicmusic and contributors 2003-2025
- 授權：GNU Lesser General Public License v3（`licenses\columns_ui\COPYING.LESSER`，搭配 `licenses\columns_ui\COPYING` 的 GNU GPL v3）
- **這是修改版**：以上游 v3.7.1 為基礎，加上修改後重新編譯，例如展開頁、底線式分頁、主選單按鈕、暫停時凍結進度條、主題字型命令、中英兩套介面文字，以及 v1.20 新增的下一首提示、已停止畫面、停止鈕收起展開頁、播放別首歌時保留播放佇列，還有進度條的改進；v1.40 再加上展開頁封面虛化背景、細捲軸、沒封面時自動指到附的唱片圖、設定頁整理；v1.50 再加上展開頁顯示內容切換（VU 表、頻譜）、曲目資訊卡與看大圖的放大鈕、歌詞防誤拖、自己畫的滑鼠提示、提示卡片統一外觀、停止時的展開規則。
- 修改版完整原始碼：https://github.com/openeric2000/columns_ui （標籤 `fb2k-nocturne-v1.50`；v1.40 附的是標籤 `fb2k-nocturne-v1.40`，v1.30 是 `fb2k-nocturne-v1.30`，v1.20 是 `fb2k-nocturne-v1.20`，v1.10 是 `fb2k-nocturne-v1.10`）。修改都在 commit 歷史裡，一個功能一個或數個 commit；用 `git clone --recursive` 會一起抓到修改過的 ui_helpers，編譯方式見該 repo 的 README。中文版照原本的方式編譯；英文版另外定義 `NOCTURNE_LANG_EN`（介面文字在 `foo_ui_columns\nocturne_text.h`）
- 上游原始碼：https://github.com/reupen/columns_ui （標籤 `v3.7.1`）
- 一起編進這個 DLL 的程式庫：
  - ui_helpers（**有修改**：深色模式清單欄位標題之間的分隔線，只在滑鼠停的那一欄顯示；v1.40 加上清單的細捲軸，v1.50 加上清單框選方框；原始碼 https://github.com/openeric2000/ui_helpers 分支 `fb2k-nocturne`，標籤 `fb2k-nocturne-v1.50`）、mmh、fbh：Copyright (c) Reupen Shah 2003–2017，BSD 3-Clause License（`licenses\columns_ui\ui_helpers-LICENCE`、`mmh-LICENCE`、`fbh-LICENCE`）
  - columns_ui-sdk、svg-services 介面：Reupen Shah，0BSD（`columns_ui-sdk-LICENCE`、`svg-services-LICENCE`）
  - foobar2000 SDK：Copyright (c) Peter Pawlowski，BSD 類授權（`licenses\columns_ui\foobar2000-sdk-license.txt`）
  - pfc：Copyright (C) Peter Pawlowski，zlib 類授權（`licenses\columns_ui\pfc-license.txt`）
  - {fmt}：Copyright (c) 2012 - present, Victor Zverovich and {fmt} contributors，MIT License（`fmt-LICENSE`）
  - GSL：Copyright (c) 2015 Microsoft Corporation，MIT License（`GSL-LICENSE`）
  - WIL：Copyright (c) Microsoft Corporation，MIT License（`WIL-LICENSE`）
  - lexy、range-v3：Boost Software License 1.0（`lexy-LICENSE`、`range-v3-LICENSE`）

### Album list panel 2.2.0（修改版，v1.40 起）

- 檔案：`user-components-x64\foo_uie_albumlist\foo_uie_albumlist.dll`
- 以 Peter Pawlowski 的 Album List 3.1.0 為基礎，由 reupen 維護
- 授權：GNU Lesser General Public License v3（`licenses\album_list_panel\COPYING.LESSER`、`COPYING`）
- **這是修改版**：以上游 v2.2.0 為基礎，加上修改後重新編譯：搜尋框外觀（圓角、放大鏡、清除鈕）、新的主選單命令「搜尋專輯清單」、資料夾樹的細捲軸，以及中英兩套搜尋框提示字；v1.50 再加上「目前選取資料夾」隱藏伴奏版、搜尋框位置可選、細捲軸自動隱藏。v1.30 以前附的是未修改的官方版。
- 修改版完整原始碼：https://github.com/openeric2000/album_list_panel （分支 `fb2k-nocturne`，標籤 `fb2k-nocturne-v1.50`）。修改都在 commit 歷史裡；中文版照原本的方式編譯，英文版另外定義 `NOCTURNE_LANG_EN`
- 上游原始碼：https://github.com/reupen/album_list_panel （標籤 `v2.2.0`）
- 一起編進這個 DLL 的程式庫：ui_helpers、mmh、fbh（BSD 3-Clause）、columns_ui-sdk（0BSD）、foobar2000 SDK、pfc，授權同上

### foo_queue_mirror 1.3.2

- 檔案：`user-components-x64\foo_queue_mirror\foo_queue_mirror.dll`
- 版權：Copyright (c) 2026 openeric2000
- 授權：MIT License（`licenses\foo_queue_mirror\LICENSE`）
- 原始碼：https://github.com/openeric2000/foo_queue_mirror （標籤 `v1.3.2`）

### ESLyric 歌詞來源與解析器腳本

- 檔案：`eslyric-data\scripts\searcher\`（kugou.js、lrclib.js、minilyrics.js、musixmatch.js、netease.js、netease_en.js、qqmusic.js）、`eslyric-data\scripts\parser\`（krc.js、qrc.js、srt.js）、`eslyric-data\scripts\lib\`
- 出處：ESLyric 官方腳本庫 https://github.com/ESLyric/scripts （ESLyric 設定裡的「獲取更多…」也是從這裡下載），沒有修改。腳本檔頭標示的作者有 ohyeah、wistaria、anonymous，以及 TT（https://github.com/TT-ReBORN ，lrclib、minilyrics、musixmatch、netease_en 有他的修改或重寫）。腳本裡另外致謝：Binaryify/NeteaseCloudMusicApi、jsososo/QQMusicApi、xmcp/QRCD、olee/minilyrics-proxy。
- **授權：這些腳本與 ESLyric 官方腳本庫都沒有附授權條款，作者沒有明確允許轉發。** 套件把它們附上，只是為了讓使用者不用自己找腳本；原作者若要求移除，會立刻移除。不想用的話，可以刪掉整個 `eslyric-data\scripts` 資料夾，需要時再用 ESLyric 的「獲取更多…」自己下載。
- 腳本引用的程式庫（`lib\`，只附執行需要的檔案）：
  - crypto-es：Copyright (c) 2018-2020 LIN Chen，MIT License（`licenses\eslyric-scripts\crypto-es-LICENSE`）
  - himalaya：Copyright (c) 2017 Chris Andrejewski，ISC License（`licenses\eslyric-scripts\himalaya-LICENSE`）
  - querystring：Copyright (c) 2013 Greg Allen，MIT License（`licenses\eslyric-scripts\querystring-LICENSE`）
  - parser_ext.so：QRC 歌詞解析的擴充模組（`qrc.js` 檔頭標示作者 wistaria），沒有授權說明
- 這些腳本會連到網易雲音樂、酷狗音樂、QQ 音樂、LRCLIB、MiniLyrics、Musixmatch 的伺服器搜尋歌詞，細節見 README。

## 沒有隨包附上，請自己下載

以下元件的作者沒有公開允許轉發的授權條款，所以這個套件不附，請到官方網站下載安裝：

| 元件 | 作者 | 下載 |
|------|------|------|
| foobar2000 2.x（64 位元） | Peter Pawlowski | https://www.foobar2000.org/download |
| ESLyric 1.0.7.0 以上 | ESLyric | https://github.com/ESLyric/release/releases |
| WebView2（foo_webview2）0.3.28 以上 | P. Stuer、J. Cassis | https://www.foobar2000.org/components/view/foo_webview2 |
| Playback Statistics（foo_playcount） | Peter Pawlowski | https://www.foobar2000.org/components/view/foo_playcount |
