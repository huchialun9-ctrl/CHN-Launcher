# CHN-Launcher

<p align="center">
  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 667" width="100%" height="auto">
    <rect width="1000" height="667" fill="#000000"/>
    <defs>
      <pattern id="dot-grid" x="0" y="0" width="50" height="50" patternUnits="userSpaceOnUse">
        <circle cx="25" cy="25" r="2.5" fill="#404040"/>
      </pattern>
    </defs>
    <rect x="250" y="83" width="500" height="500" fill="url(#dot-grid)"/>
    <g fill="#ffffff">
      <path d="M 375 200 H 525 V 280 H 450 V 355 H 375 Z"/>
      <polygon points="450,370 540,280 565,305 475,395"/>
      <path d="M 490 320 H 565 V 395 H 640 V 475 H 490 Z"/>
    </g>
    <text x="500" y="565" text-anchor="middle" fill="#ffffff" font-family="'SF Pro Display', 'Inter', -apple-system, sans-serif" font-size="34" font-weight="700" letter-spacing="14">CHN LAUNCHER</text>
  </svg>
</p>

<p align="center">
  <strong>Minimalist, region-aware game launcher for Chinese players.</strong><br>
  <strong>專為中文玩家打造的極簡、跨平台遊戲庫整合啟動器。</strong>
</p>

<p align="center">
  Unified Steam, Epic, GOG, Xbox & WeGame library with Pinyin search and deal tracking. Built with Tauri & Rust.
</p>

---

## 專案定位

CHN Launcher 是一套以地區感知架構為核心的跨平台桌面端遊戲啟動與管理系統。系統透過讀取本機各商城設定檔、註冊表與系統套件清單，將多平台遊戲集中於單一介面，提供海報牆管理、中文多維度搜尋、兩岸譯名映射、導購比價及遊戲喚醒功能。整體視覺遵循高對比黑白幾何、極簡點陣與工程美學設計。

---

## 地區感知系統

使用者於系統初始化階段選定所在地區，系統即時切換對應設定：

* **台灣 / 香港地區**
  * 介面語系：繁體中文
  * 比價幣別：新台幣 (TWD) / 港幣 (HKD)
  * 網路傳輸：直連官方 CDN
  * 平台掃描：Steam、Epic Games、GOG、Xbox、Battle.net、Riot Client
  * 社群串接：巴哈姆特、PTT、Steam 社群
* **中國大陸地區**
  * 介面語系：簡體中文
  * 比價幣別：人民幣 (CNY)
  * 網路傳輸：啟用 Host 與 SNI 代理規則，掛載圖源鏡像
  * 平台掃描：Steam、Epic Games、GOG、Xbox、WeGame、蒸汽平台、米哈遊客戶端
  * 社群串接：小黑盒、著迷 Wiki、Bilibili
* **其他海外地區**
  * 介面語系：繁體中文、簡體中文、英文
  * 比價幣別：美元 (USD) 或本地貨幣
  * 網路傳輸：直連官方 CDN
  * 平台掃描：Steam、Epic Games、GOG、Xbox
  * 社群串接：Steam 原生評測、Reddit

---

## 核心功能模組

* **遊戲庫掃描與平台整合**：自動解析 Steam (vdf/acf)、Epic Games (Manifests JSON)、GOG (Registry)、Xbox (UWP)、WeGame 與米哈遊客戶端，支援自訂本機 `.exe` 綠色遊戲導入。
* **遊戲啟動與進程管理**：採用零侵入原生 URI 喚醒機制（如 `steam://`、`com.epicgames.launcher://`），支援自訂啟動參數、進程存活監控、遊玩時間統計與在地加速器連動。
* **中文檢索與元數據管理**：支援全拼、簡拼（如 `sbpk` 找賽博朋克）、注音符號與原名即時搜尋；內建中港台譯名映射庫；標註中文支援度；串接 Steam CDN 與 SteamGridDB 實現離線海報快取。
* **導購比價與商城跳轉**：整合官方授權商城即時價格與歷史最低折扣，支援幣別自動換算與限免活動推播，點擊一鍵跳轉瀏覽器購買（無內建金流，安全合規）。
* **介面呈現與統計**：提供海報網格與列表檢視，支援多維度排序篩選與詳細遊玩歷程記錄。

---

## 技術架構

* **桌面容器**：Tauri v2
* **系統核心層**：Rust
* **使用者介面**：Vue 3 + TypeScript + Tailwind CSS

---

## 授權條款

本專案採用 GNU General Public License v3.0 (GPL-3.0) 開源授權。

# CHN-Launcher

<p align="center">
  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 667" width="100%" height="auto">
    <rect width="1000" height="667" fill="#000000"/>
    <defs>
      <pattern id="dot-grid" x="0" y="0" width="50" height="50" patternUnits="userSpaceOnUse">
        <circle cx="25" cy="25" r="2.5" fill="#404040"/>
      </pattern>
    </defs>
    <rect x="250" y="83" width="500" height="500" fill="url(#dot-grid)"/>
    <g fill="#ffffff">
      <path d="M 375 200 H 525 V 280 H 450 V 355 H 375 Z"/>
      <polygon points="450,370 540,280 565,305 475,395"/>
      <path d="M 490 320 H 565 V 395 H 640 V 475 H 490 Z"/>
    </g>
    <text x="500" y="565" text-anchor="middle" fill="#ffffff" font-family="'SF Pro Display', 'Inter', -apple-system, sans-serif" font-size="34" font-weight="700" letter-spacing="14">CHN LAUNCHER</text>
  </svg>
</p>

<p align="center">
  <strong>Minimalist, region-aware game launcher for Chinese players.</strong><br>
  <strong>專為中文玩家打造的極簡、跨平台遊戲庫整合啟動器。</strong>
</p>

<p align="center">
  Unified Steam, Epic, GOG, Xbox & WeGame library with Pinyin search and deal tracking. Built with Tauri & Rust.
</p>

---

## 專案定位

CHN Launcher 是一套以地區感知架構為核心的跨平台桌面端遊戲啟動與管理系統。系統透過讀取本機各商城設定檔、註冊表與系統套件清單，將多平台遊戲集中於單一介面，提供海報牆管理、中文多維度搜尋、兩岸譯名映射、導購比價及遊戲喚醒功能。整體視覺遵循高對比黑白幾何、極簡點陣與工程美學設計。

---

## 地區感知系統

使用者於系統初始化階段選定所在地區，系統即時切換對應設定：

* **台灣 / 香港地區**
  * 介面語系：繁體中文
  * 比價幣別：新台幣 (TWD) / 港幣 (HKD)
  * 網路傳輸：直連官方 CDN
  * 平台掃描：Steam、Epic Games、GOG、Xbox、Battle.net、Riot Client
  * 社群串接：巴哈姆特、PTT、Steam 社群
* **中國大陸地區**
  * 介面語系：簡體中文
  * 比價幣別：人民幣 (CNY)
  * 網路傳輸：啟用 Host 與 SNI 代理規則，掛載圖源鏡像
  * 平台掃描：Steam、Epic Games、GOG、Xbox、WeGame、蒸汽平台、米哈遊客戶端
  * 社群串接：小黑盒、著迷 Wiki、Bilibili
* **其他海外地區**
  * 介面語系：繁體中文、簡體中文、英文
  * 比價幣別：美元 (USD) 或本地貨幣
  * 網路傳輸：直連官方 CDN
  * 平台掃描：Steam、Epic Games、GOG、Xbox
  * 社群串接：Steam 原生評測、Reddit

---

## 核心功能模組

* **遊戲庫掃描與平台整合**：自動解析 Steam (vdf/acf)、Epic Games (Manifests JSON)、GOG (Registry)、Xbox (UWP)、WeGame 與米哈遊客戶端，支援自訂本機 `.exe` 綠色遊戲導入。
* **遊戲啟動與進程管理**：採用零侵入原生 URI 喚醒機制（如 `steam://`、`com.epicgames.launcher://`），支援自訂啟動參數、進程存活監控、遊玩時間統計與在地加速器連動。
* **中文檢索與元數據管理**：支援全拼、簡拼（如 `sbpk` 找賽博朋克）、注音符號與原名即時搜尋；內建中港台譯名映射庫；標註中文支援度；串接 Steam CDN 與 SteamGridDB 實現離線海報快取。
* **導購比價與商城跳轉**：整合官方授權商城即時價格與歷史最低折扣，支援幣別自動換算與限免活動推播，點擊一鍵跳轉瀏覽器購買（無內建金流，安全合規）。
* **介面呈現與統計**：提供海報網格與列表檢視，支援多維度排序篩選與詳細遊玩歷程記錄。

---

## 技術架構

* **桌面容器**：Tauri v2
* **系統核心層**：Rust
* **使用者介面**：Vue 3 + TypeScript + Tailwind CSS

---

## 授權條款

本專案採用 GNU General Public License v3.0 (GPL-3.0) 開源授權。
