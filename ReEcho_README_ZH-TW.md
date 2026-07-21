# Re:Echo

> 使用現代 SwiftUI 製作，面向 iOS、iPadOS 與 macOS 的 Galgame／視覺小說遊戲庫與執行工具。

Re:Echo 是我在空閒時間開發的個人興趣專案。它不是商業產品，也不代表我能為所有引擎、所有遊戲格式提供快速且長期的維護。專案最初以 ONS／ONScripter 類遊戲為核心，現在亦在不同平台上加入 RPG Maker、KrKr2 與 PC Windows Galgame 的實驗性支援。

Re:Echo 希望改善的並不只是「把遊戲打開」，而是讓匯入、辨識、分類、搜尋與啟動都更接近 Apple 平台原生 App。使用者不必每次解壓縮封包、翻找多層資料夾，再手動指定啟動檔案。

> Re:Echo 本身不提供任何遊戲、遊戲資源或商業引擎檔案。請只匯入你合法持有並有權使用的內容。

## 平台概覽

| 平台 | 系統要求 | 主要用途 | 目前提供的引擎入口 |
| --- | --- | --- | --- |
| iOS | iOS 26.0 或以上 | 適合手機觸控操作的隨身遊戲庫 | ONS、RPG Maker MV／MZ |
| iPadOS | iPadOS 26.0 或以上 | 多欄遊戲庫、大畫面觸控遊玩 | ONS、RPG Maker MV／MZ |
| macOS | macOS 26.0 或以上，Apple 晶片 | 桌面遊戲管理、獨立遊戲視窗與更多引擎 | ONS、KrKr2、RPG Maker MV／MZ、PC Windows Galgame |

## iPhone：為觸控重新整理的遊戲庫

iPhone 版使用底部分頁介面，將「最近遊玩」、ONS、RPG Maker 與實驗功能分開。遊戲收藏可以直接搜尋，常用作品也會出現在最近遊玩頁面。

<p align="center">
  <img src="https://github.com/user-attachments/assets/f9e0d53f-3552-4d9f-8b26-cfca8a1dbca5" alt="Re:Echo iPhone 最近遊玩與搜尋畫面" width="340" />
  <br />
  <sub style="color: gray;">Re:Echo iPhone 最近遊玩與搜尋畫面</sub>
</p>

手機版重點：

- 從「檔案」App 選取 ZIP 封包或遊戲資料夾。
- 自動整理常見的多層封包結構。
- 依遊戲類型加入相應的遊戲庫。
- 支援遊戲搜尋與最近遊玩記錄。
- 配合直向、橫向畫面與不同尺寸的 iPhone。
- 可選擇開啟 HUD，以及是否拉伸適配全螢幕。

## iPad：充分利用大畫面的多欄介面

iPad 版使用側邊欄、遊戲列表與詳情區構成的多欄佈局。切換引擎、搜尋收藏、選擇遊戲與啟動內容均可在同一畫面完成，不需要套用傳統桌面模擬器的狹小視窗介面。

<p align="center">
  <img src="https://github.com/user-attachments/assets/a45725d2-4523-4b0d-b65d-307fcaaf0551" alt="Re:Echo iPadOS 多欄遊戲庫" width="1000" />
  <br />
  <sub style="color: gray;">Re:Echo iPadOS 多欄遊戲庫</sub>
</p>

### 遊戲 HUD 與全螢幕

iPhone 與 iPad 可在遊戲中呼出輕量 HUD。目前 HUD 僅保留「重新啟動」與「退出」，存檔、讀取、快進與其他遊戲功能由引擎及遊戲內建介面負責，避免額外控制層破壞腳本流程。

拉伸適配可以讓舊解析度作品更充分利用現代螢幕；也可在設定中關閉 HUD 或拉伸功能。由於原始解析度、長寬比與腳本行為各不相同，拉伸顯示不保證適合每一部作品。

<p align="center">
  <img src="https://github.com/user-attachments/assets/f7dd2e08-c282-4f9a-b294-312d22070664" alt="Re:Echo iPadOS 遊戲 HUD" width="1000" />
  <br />
  <sub style="color: gray;">Re:Echo iPadOS 遊戲 HUD</sub>
</p>

## Mac：桌面級收藏管理與獨立遊戲視窗

macOS 版針對 Apple 晶片與桌面使用方式重新設計。側邊欄將遊戲分為「引擎類型」與使用者建立的 PC Galgame 資料夾；主畫面以單一封面圖示呈現遊戲，並提供搜尋、匯入及重新整理。

<p align="center">
  <img src="https://github.com/user-attachments/assets/233e814b-b55f-48e0-8ac5-fd6c4aba3f71" alt="Re:Echo macOS 主頁與遊戲收藏" width="1100" />
  <br />
  <sub style="color: gray;">Re:Echo macOS 主頁與遊戲收藏</sub>
</p>

Mac 版功能包括：

- ONS、KrKr2、RPG Maker 與 PC Windows Galgame 分類入口。
- 自訂 PC 遊戲資料夾；未建立資料夾時使用預設的「未命名」。
- ZIP 或資料夾直接匯入，並分析封包內容。
- 從遊戲圖片中自動挑選較可能的封面。
- 編輯遊戲名稱、編輯封面、切換 Metal HUD 與刪除遊戲。
- 遊戲在獨立視窗中執行，不佔用遊戲庫主視窗。
- 從選單列控制全螢幕、重新啟動及退出目前遊戲。

<p align="center">
  <img src="https://github.com/user-attachments/assets/16348e21-096f-463a-b614-c57439679ed0" alt="Re:Echo macOS 遊戲庫與獨立 ONS 視窗" width="1100" />
  <br />
  <sub style="color: gray;">Re:Echo macOS 遊戲庫與獨立 ONS 視窗</sub>
</p>

## 直接匯入 ZIP

遊戲封包並沒有統一的目錄規則。有些 ZIP 多包一層資料夾，有些混有說明文件或系統檔案，也可能在深層目錄才出現真正的遊戲入口。Re:Echo 會嘗試減少這些重複操作：

1. 直接選擇 `.zip` 或已解壓縮的遊戲資料夾。
2. 將內容匯入 App 的本機遊戲庫。
3. 掃描常見的引擎特徵與啟動檔案。
4. 整理常見的多層資料夾結構。
5. 將辨識結果加入正確的引擎分類或 PC 遊戲資料夾。
6. 之後直接從 Re:Echo 的遊戲庫啟動。

如果封包缺少必要檔案、使用不受支援的加密方式，或只是更新補丁而不是完整遊戲，App 仍可能無法辨識或執行。

## 運作原理（簡述）

Re:Echo 會根據封包中的特徵檔案選擇對應的執行環境，並把畫面、聲音與輸入整合到 Apple 平台的原生介面。iPhone 與 iPad 著重觸控與螢幕適配；Mac 則使用獨立視窗、鍵盤與滑鼠操作。PC Windows Galgame 會經由 App 內建的相容轉譯環境嘗試執行，不要求使用者另行安裝 CrossOver。

## 相容性

### 相容性等級

| 等級 | 意義 |
| --- | --- |
| 主要支援 | 專案的核心使用情境，會優先修正通用相容性問題 |
| 有限／實驗性 | 已能執行部分作品，但插件、影音或平台差異可能造成問題 |
| 不支援 | 目前沒有對應執行環境，或技術條件不適合在 App 中執行 |

### ONS／ONScripter

**狀態：主要支援。** iOS、iPadOS 與 macOS 均提供 ONS 入口。

通常較容易運行：

- 使用常見 `0.txt`、`00.txt`、`nscript.dat` 等入口的 ONS 封包。
- 資源完整、未損壞，且使用常見圖片與音訊格式的作品。
- 僅有額外頂層資料夾、說明文件或一般封包雜項的 ZIP。

可能無法正常運行：

- 依賴特定 ONS 分支私有命令、外部插件或修改版引擎行為的作品。
- 必須載入 Windows DLL、外部 EXE 或其他原生模組的腳本。
- 使用特殊加密、私有封包格式或未支援影音編碼的內容。
- 僅包含補丁、缺少腳本或資源、檔名大小寫不一致的封包。
- 強依賴特定桌面字型、系統路徑、區域編碼或非標準輸入方式的作品。

### RPG Maker

**狀態：有限／實驗性支援。** 目前目標是 RPG Maker **MV／MZ** 類型。

通常較容易運行：

- 包含完整網頁遊戲內容、資料檔、JavaScript 與資源目錄的 MV／MZ 封包。
- 使用標準引擎 API 和常見網頁影音格式的作品。

可能無法正常運行：

- 依賴 NW.js、Node.js、Electron、桌面檔案系統 API 或外部程式的插件。
- 包含平台限定原生模組、Windows DLL 或安裝器才能建立的資料。
- 使用自訂加密、特殊影片／音訊編碼，或缺少解密金鑰與必要資源。
- 大幅修改渲染、輸入、儲存或網路流程的第三方插件組合。

目前不支援：

- RPG Maker 2000／2003、XP、VX、VX Ace 的原生 Windows 執行格式。
- 需要官方編輯器、RTP 安裝或 Windows 專用執行器才能啟動的封包。

### KrKr2／Kirikiri2（僅 macOS）

**狀態：有限／實驗性支援。** iOS 與 iPadOS 版目前沒有 KrKr2 入口。

通常較容易運行：

- 具有標準啟動腳本與完整資料封包的 Kirikiri2 類作品。
- 主要使用引擎內建腳本、圖片、音訊與基本影片功能的內容。

可能無法正常運行：

- 依賴 Windows DLL、COM、ActiveX、外部 EXE 或廠商自製原生插件。
- 使用特殊 XP3 加密、授權驗證、私有解包方式或受 DRM 保護的內容。
- 需要 Windows 專用影片濾鏡、舊式解碼器或特定字型環境的作品。
- Kirikiri Z 或大幅修改過的衍生引擎作品；KrKr2 入口不代表相容所有 Kirikiri 系列。

### PC Windows Galgame（僅 macOS）

**狀態：高度實驗性。** 這不是完整的 Windows 虛擬機，也不等同於保證相容的商業 Windows 執行環境。

較有機會運行：

- 可攜式、解壓後能直接執行，且依賴較少的傳統 2D 遊戲。
- 不需要額外驅動程式、啟動器、帳號服務或複雜安裝流程的作品。
- 使用常見 Windows API、DirectDraw／較舊圖形介面與一般音訊格式的內容。

通常不能運行或成功率很低：

- 帶有 DRM、反作弊、線上授權、核心驅動或必須登入第三方啟動器的遊戲。
- 必須安裝特定 Windows 系統服務、裝置驅動、專用編解碼器或全域字型的作品。
- 依賴複雜安裝器、登錄檔狀態或多個外部運行庫，且沒有可攜式遊戲目錄的內容。
- 需要 DirectX 12、現代高階 3D、VR、特殊輸入裝置或廠商 GPU 擴充的遊戲。
- 使用未支援的 16 位元程式、驅動級保護、硬體金鑰或其他底層 Windows 元件的作品。
- 啟動器與真正遊戲程式分離，但封包中缺少必要元件的內容。

## 跨平台差異

- iOS／iPadOS 不會直接執行 Windows EXE，也不提供 macOS 的 PC Galgame 相容環境。
- KrKr2 目前只在 macOS 版提供。
- RPG Maker 入口以 MV／MZ 網頁型遊戲為目標，不代表支援所有 RPG Maker 世代。
- 同一遊戲在不同裝置上的字型、影音、觸控、鍵盤或全螢幕表現可能不同。
- 存檔通常由遊戲及引擎管理；更新、刪除或重新匯入前應自行備份重要存檔。

## 簽名與安裝

iOS／iPadOS 版本以個人使用與測試為主。使用免費 Apple ID 簽名時，描述檔會在短時間後到期，屆時可能需要重新簽名及安裝。此專案不計畫提供 P12 簽名或任何代簽服務。

macOS 版目前面向 Apple 晶片與 macOS 26.0 或以上版本。系統安全設定、App 簽名、隔離屬性與第三方遊戲檔案來源，都可能影響首次啟動。

## 專案狀態

Re:Echo 是個人興趣專案，更新速度可能很慢，某些功能也可能長時間停留在實驗階段。專案會優先處理能改善一整類遊戲的通用問題，而不是承諾逐一適配所有作品。

請把它視為以 ONS 為核心、逐步嘗試其他引擎與平台能力的工具，而不是近期內即可涵蓋所有引擎、所有平台、所有格式的萬用模擬器。

## 連結

- 開發者：[GepulsteAtmung on GitHub](https://github.com/GepulsteAtmung)
- Discord：[加入社群](https://discord.gg/MeJkYV6ghj)

---

*本文中的遊戲畫面僅作 Re:Echo 功能展示。遊戲、角色、美術、商標及相關內容之權利均屬原權利人所有。*
