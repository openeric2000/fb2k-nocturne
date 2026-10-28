# 第三方授權說明

這個主題套件用到下面這些別人的作品。隨包附上的部分，授權全文放在這份文件旁邊的 `licenses\` 資料夾；沒有隨包附上的元件，請照 README 到官方網站下載。下面的檔案位置都是 fb2k 設定資料夾裡的位置。

## 隨包附上

### Columns UI 3.7.1（修改版）

- 檔案：`user-components-x64\foo_ui_columns\foo_ui_columns.dll`
- 版權：Copyright (c) musicmusic and contributors 2003-2025
- 授權：GNU Lesser General Public License v3（`licenses\columns_ui\COPYING.LESSER`，搭配 `licenses\columns_ui\COPYING` 的 GNU GPL v3）
- **這是修改版**：以上游 v3.7.1 為基礎，加上 20 個修改（patch 0001～0020，例如展開頁、底線式分頁、主選單按鈕、暫停時凍結進度條、主題字型命令）後重新編譯。
- 修改版完整原始碼：https://github.com/openeric2000/columns_ui （標籤 `fb2k-nocturne-v1.00`）。每個修改各是一個 commit；用 `git clone --recursive` 會一起抓到修改過的 ui_helpers，編譯方式見該 repo 的 README
- 上游原始碼：https://github.com/reupen/columns_ui （標籤 `v3.7.1`）
- 一起編進這個 DLL 的程式庫：
  - ui_helpers（**有修改**，patch 0019 拿掉深色模式清單欄位標題的分隔線；原始碼 https://github.com/openeric2000/ui_helpers 分支 `fb2k-nocturne`）、mmh、fbh：Copyright (c) Reupen Shah 2003–2017，BSD 3-Clause License（`licenses\columns_ui\ui_helpers-LICENCE`、`mmh-LICENCE`、`fbh-LICENCE`）
  - columns_ui-sdk、svg-services 介面：Reupen Shah，0BSD（`columns_ui-sdk-LICENCE`、`svg-services-LICENCE`）
  - foobar2000 SDK：Copyright (c) Peter Pawlowski，BSD 類授權（`licenses\columns_ui\foobar2000-sdk-license.txt`）
  - pfc：Copyright (C) Peter Pawlowski，zlib 類授權（`licenses\columns_ui\pfc-license.txt`）
  - {fmt}：Copyright (c) 2012 - present, Victor Zverovich and {fmt} contributors，MIT License（`fmt-LICENSE`）
  - GSL：Copyright (c) 2015 Microsoft Corporation，MIT License（`GSL-LICENSE`）
  - WIL：Copyright (c) Microsoft Corporation，MIT License（`WIL-LICENSE`）
  - lexy、range-v3：Boost Software License 1.0（`lexy-LICENSE`、`range-v3-LICENSE`）

### Album list panel 2.2.0

- 檔案：`user-components-x64\foo_uie_albumlist\foo_uie_albumlist.dll`（未修改，取自官方元件包）
- 以 Peter Pawlowski 的 Album List 3.1.0 為基礎，由 reupen 維護
- 授權：GNU Lesser General Public License v3（`licenses\album_list_panel\COPYING.LESSER`、`COPYING`）
- 原始碼：https://github.com/reupen/album_list_panel （標籤 `v2.2.0`）
- 一起編進這個 DLL 的程式庫：ui_helpers、mmh、fbh（BSD 3-Clause）、columns_ui-sdk（0BSD）、foobar2000 SDK、pfc，授權同上

### foo_queue_mirror 1.2.0

- 檔案：`user-components-x64\foo_queue_mirror\foo_queue_mirror.dll`
- 版權：Copyright (c) 2026 openeric2000
- 授權：MIT License（`licenses\foo_queue_mirror\LICENSE`）
- 原始碼：https://github.com/openeric2000/foo_queue_mirror （標籤 `v1.2.0`）

## 沒有隨包附上，請自己下載

以下元件的作者沒有公開允許轉發的授權條款，所以這個套件不附，請到官方網站下載安裝：

| 元件 | 作者 | 下載 |
|------|------|------|
| foobar2000 2.x（64 位元） | Peter Pawlowski | https://www.foobar2000.org/download |
| ESLyric 1.0.7.0 以上 | ESLyric | https://github.com/ESLyric/release/releases |
| WebView2（foo_webview2）0.3.28 以上 | P. Stuer、J. Cassis | https://www.foobar2000.org/components/view/foo_webview2 |
| Playback Statistics（foo_playcount） | Peter Pawlowski | https://www.foobar2000.org/components/view/foo_playcount |
