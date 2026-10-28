# DockSpark

[English](README.md) · [简体中文](README.zh-CN.md) · [繁體中文](README.zh-TW.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Deutsch](README.de.md) · [Français](README.fr.md) · [Español](README.es.md)

DockSpark 讓你直接從 macOS Dock 切換瀏覽器設定檔。將游標停留在支援的瀏覽器圖像上，即可選擇所需設定檔，無須開啟瀏覽器的設定檔選單。

[下載最新版本](https://github.com/DockSpark/DockSpark/releases/latest)
· [官方網站](https://dockspark.app)
· [更新紀錄（英文）](CHANGELOG.md)
· [回報問題](https://github.com/DockSpark/DockSpark/issues)

## 功能

- 從瀏覽器 Dock 圖像旁的彈出面板切換設定檔
- 使用原生 macOS App 管理瀏覽器設定檔
- 自訂名稱與顏色，快速辨識設定檔
- 選擇在 Dock 懸停選單中顯示哪些具名設定檔
- 使用 DockSpark Free，或透過 Pro 解鎖不限數量的瀏覽器與設定檔
- 顯示或隱藏選單列圖像與 Dock 圖像
- 在 App 內檢查更新
- 從「輔助說明」選單開啟文件或傳送結構化意見回饋
- 支援英文、簡體中文、繁體中文、日文、韓文、德文、法文及西班牙文
- 懸停面板隨 Dock 圖像大小縮放，支援 Dock 放大效果
- 可在「一般」設定中關閉匿名使用情況分析

## 系統需求

- macOS 14.0 或以上版本
- Apple 晶片或 Intel Mac
- 將支援的瀏覽器保留在 Dock 中

### 支援的瀏覽器

| 瀏覽器 | 從 Dock 切換設定檔 |
| --- | --- |
| Safari | 支援 |
| Firefox | 支援 |
| Google Chrome | 支援 |
| Chromium | 支援 |
| Microsoft Edge | 支援 |
| Brave Browser | 支援 |
| Vivaldi | 支援 |
| Opera | 支援 |
| Opera GX | 支援 |
| Arc | 支援 |

已安裝的 Safari、Google Chrome 與 Firefox 預設啟用。Free 方案允許啟用一個瀏覽器，每個瀏覽器最多三個具名設定檔；私密瀏覽與無痕模式項目不計入此限制。Pro 可解除這些限制。你可以從 App 列表加入其他已安裝的瀏覽器。

## 安裝

### Homebrew

```sh
brew trust --cask dockspark/tap/dockspark && \
  brew install --cask dockspark/tap/dockspark
```

### 手動下載

1. 開啟[最新版本頁面](https://github.com/DockSpark/DockSpark/releases/latest)。
2. 下載 `DockSpark-0.5.0.dmg`。請勿下載 GitHub 自動產生的原始碼壓縮檔。
3. 開啟磁碟映像檔，將 `DockSpark.app` 拖入「應用程式」檔案夾。
4. 啟動 DockSpark，並授予所要求的 macOS 權限。

也可以下載 `DockSpark-0.5.0.zip` 手動安裝。

DockSpark 已使用 Developer ID 憑證簽署，並通過 Apple 公證。

## 權限

DockSpark 僅要求切換設定檔所需的系統權限：

- **輔助使用**：偵測游標與 Dock 中支援的瀏覽器圖像之間的互動。
- **自動化**：允許 DockSpark 要求所選瀏覽器切換設定檔。
- **完整磁碟存取權**：選用權限，僅用於尋找 Chromium 與 Firefox 的設定檔中繼資料。

你可以隨時在**系統設定 > 隱私權與安全性**中查看或撤銷這些權限。

## 使用方式

1. 將支援的瀏覽器加入 Dock。
2. 在 DockSpark 中設定瀏覽器及其設定檔。
3. 將游標停留在該瀏覽器的 Dock 圖像上。
4. 從彈出面板選擇設定檔。

## AI 助理技能

[DockSpark 技能](skills/dockspark/SKILL.md)可協助 AI 助理介紹 DockSpark 的用途與適用情境、引導安裝與日常使用、尋找官方文件，以及排解常見問題。技能版本 **0.5.0** 與 App 版本保持一致；隨附指南已對照 DockSpark 0.5.0 檢查。助理會使用你的語言回答。

透過 [Skills CLI](https://github.com/vercel-labs/skills) 安裝（需要 Node.js；目前環境需求請參閱其文件）：

```sh
npx skills add DockSpark/DockSpark --skill dockspark
```

依提示選擇你的 AI 助理。預設安裝至目前專案，加入 `-g` 可全域安裝。上述 GitHub 指令要求技能已發佈至本儲存庫。從本機簽出目錄安裝時，使用：

```sh
npx skills add . --skill dockspark
```

若要[手動安裝至 Codex](https://developers.openai.com/codex/skills/)，請將整個 `skills/dockspark` 目錄（包含 `references/` 與 `agents/`）複製至 `~/.agents/skills/dockspark`，或專案內的 `.agents/skills/dockspark`。其他助理可能使用不同的技能目錄。如果未顯示技能，請重新載入助理的技能或開啟新工作階段。

提示詞範例：

- `使用 $dockspark 介紹 DockSpark 能幫我做什麼。`
- `使用 $dockspark 協助我設定 Chrome 設定檔。`
- `使用 $dockspark 排解為什麼游標停留在 Dock 圖像上沒有反應。`

你也可以使用英文或其他語言提問。技能提供使用指引；若要使用 App，仍需另外安裝 DockSpark。每次發佈新 App 版本時，應檢查技能指南與官方連結，並同步更新技能版本及檢查基準版本。

## 螢幕截圖

![DockSpark 設定檔管理視窗](Assets/img_dockspark.jpg)

> 截圖展示 DockSpark 的介面。0.5.0 版本支援從 Dock 切換 Safari、Firefox、Chrome，以及上表所列其他 Chromium 核心瀏覽器的設定檔。

## 更新

DockSpark 使用 Sparkle 提供 App 內更新。你也可以從[發佈頁面](https://github.com/DockSpark/DockSpark/releases)手動下載版本。

## 發佈檔案完整性

SHA-256 校驗值如下：

```text
DockSpark-0.5.0.dmg  90c0f9369d67eb33e6939b1cac008ec70277f7c176c0f2a1aa0e50fb08e85eff
DockSpark-0.5.0.zip  1d7eb10b9ce7736f2a1e5f1fd790eebb399675fadb95702a6032f329f65db129
```

下載後可執行以下指令驗證：

```sh
shasum -a 256 DockSpark-0.5.0.dmg DockSpark-0.5.0.zip
```

## 意見回饋

請透過 [GitHub Issues](https://github.com/DockSpark/DockSpark/issues) 回報問題或提出改善建議。回報問題時，請附上 macOS 版本、瀏覽器版本與重現步驟。

本儲存庫包含 DockSpark 的公開發佈資料，不包含 App 原始碼。
