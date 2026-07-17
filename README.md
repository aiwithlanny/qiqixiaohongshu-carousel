
<h1 align="center">qiqixiaohongshu-carousel</h1>

<p align="center"><strong>一句話，生成符合爆款邏輯的精美小紅書圖文。</strong></p>

<p align="center">
  先研究近期高互動筆記，再優化切入角度、標題與封面，最後用 Image2.0 直接交付成品。
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Codex-Skill-111111" alt="Codex Skill">
  <img src="https://img.shields.io/badge/小紅書-Carousel-ff2442" alt="小紅書圖文">
  <img src="https://img.shields.io/badge/爆款調研-AgentReach-f59e0b" alt="AgentReach 爆款調研">
  <img src="https://img.shields.io/badge/成品生圖-Image2.0-2563eb" alt="Image2.0 成品生圖">
</p>

<p align="center">
  <img src="assets/showcase/codex-5-tools-cover.png" width="35%" alt="Codex 五個必裝工具小紅書封面">
  &nbsp;&nbsp;
  <img src="assets/showcase/ai-tools-cover.png" width="35%" alt="2026 職場 AI 工具小紅書封面">
</p>

## 它不是普通排版工具

大多數 AI 圖文工具拿到主題後就直接寫、直接排，所以很容易變成「看起來整齊，但沒有點擊理由」的 PPT 式內容。

`qiqixiaohongshu-carousel` 會先研究近期小紅書高互動筆記，找出值得借鑑的選題角度、標題鉤子和封面規律，再把你的知識包裝成更適合平台傳播的圖文。

| 普通 AI 圖文 | qiqixiaohongshu-carousel |
| --- | --- |
| 拿到主題直接生成 | 先調研近期高互動筆記 |
| 給一個普通標題 | 提供 5 個爆款切入角度 |
| 套模板、像簡報 | 先讀真實封面，再設計視覺 |
| 只交文案或提示詞 | 用 Image2.0 交付完整圖片 |
| 你自己找資料和案例 | 提供對標連結、時間與互動數據 |

目標是把原本分散的調研、選題、拆頁與排版工作集中到一次對話，依內容複雜度不同，每次可望省下約 1–2 小時。

## 快速安裝

### 最簡單：直接把這句話貼給 Codex

```text
請使用 $skill-installer 安裝這個 Skill：
https://github.com/aiwithlanny/qiqixiaohongshu-carousel
```

安裝後重新啟動 Codex，讓它載入新的 Skill。

### 手動安裝

```bash
git clone https://github.com/aiwithlanny/qiqixiaohongshu-carousel.git ~/.codex/skills/qiqixiaohongshu-carousel
```

使用前請確認 Codex 可以調用 `agent-reach` 進行爆款調研，並且可以使用 `imagegen` 的 Image2.0 生圖。

## 一句話開始使用

```text
幫我做小紅書圖文。
主題：2026 年職場人必備的 10 個 AI 工具
圖片頁數：5 張
喜歡的風格：留空，請根據爆款調研決定
```

你也可以直接說：

```text
使用 qiqixiaohongshu-carousel，把這份文案優化成 6 張小紅書圖文。
先研究近期爆款標題與封面，再幫我確認標題、排版和主視覺，最後用 Image2.0 生圖。
```

## 實際效果

以下圖片都是這套工作流實際產出的 Image2.0 成品，不是網頁模板或 PPT 截圖。

<p align="center">
  <img src="assets/showcase/ai-tools-cover.png" width="23%" alt="小紅書圖文封面">
  <img src="assets/showcase/ai-tools-research.png" width="23%" alt="小紅書爆款調研內頁">
  <img src="assets/showcase/ai-tools-map.png" width="23%" alt="小紅書工具清單內頁">
  <img src="assets/showcase/ai-tools-kit.png" width="23%" alt="小紅書行動建議內頁">
</p>

## 它怎麼工作

```text
你給主題或文案
      ↓
AgentReach 調研近期爆款筆記
      ↓
提供 5 個選題角度、原始連結與公開數據
      ↓
你提供想對標的封面截圖
      ↓
一起確認主標題、頁數、排版和主視覺
      ↓
Image2.0 生成成品並做品質檢查
```

封面截圖由你從對標連結中挑選並提供。這能確保 Skill 真正讀過你想參考的封面，而不是憑空猜測平台風格。

## 兩種工作模式

### 模式 A：你只有一個主題

適合還沒有整理文案的人。Skill 會：

1. 調研近期高互動筆記。
2. 提供 5 個值得參考的選題角度。
3. 根據你選的角度補充資料並寫出圖文大綱。
4. 確認標題、頁數、排版和主視覺。
5. 用 Image2.0 生成完整圖片。

### 模式 B：你已經有文案

適合已經有文章、筆記、課程內容或產品資料的人。Skill 會：

1. 保留你的核心知識與觀點。
2. 研究同主題的爆款標題和封面。
3. 優化切入角度、標題與圖文節奏。
4. 確認排版後直接用 Image2.0 生圖。

## 適合哪些場景

- AI 工具、職場效率與科技知識分享
- 個人品牌、顧問、講師與知識型創作者
- 課程、社群、服務或產品的內容行銷
- 把文章、逐字稿、報告或筆記改成小紅書圖文
- 不想每天花大量時間找選題、拆封面和排版的人

## 你只需要提供三項資料

```text
文案或主題：
圖片頁數：預設 5 張
喜歡的風格：可留空
```

風格留空時，Skill 會根據爆款筆記的標題、封面與重要視覺元素提出設計方案。

## 常見問題

### 它能保證爆款嗎？

不能。沒有任何工具可以保證流量。這個 Skill 的價值是用近期真實樣本降低盲猜，讓選題、標題和封面更符合平台上的有效規律。

### 為什麼要我提供封面截圖？

小紅書頁面經常有登入或載入限制。由你挑選並截圖，可以更快、更準確地確認真正想對標的視覺，而不是讓 AI 假裝看過。

### 會直接交付圖片嗎？

會。確認內容與排版後，成品必須使用 `imagegen` 的 Image2.0 生成，不用 HTML、PPT 或 Canva 截圖冒充。

### 我沒有喜歡的風格怎麼辦？

可以留空。Skill 會根據調研到的爆款封面提出主視覺、顏色和排版方向。

### 更新 Skill 後，GitHub 會自動同步嗎？

不會。本機 Skill 和 GitHub 是兩份獨立檔案。每次迭代後，需要重新將最新版同步到 GitHub；安裝 GitHub 發佈工具後，可以把這一步交給 Codex 自動完成。

## 如果它幫你省下時間

如果這套流程幫你少走彎路、少花時間找對標，歡迎點一下右上角的 **Star**。你的支持會讓這個 Skill 持續更新更多小紅書爆款研究與視覺工作流。

> 好內容不該輸在包裝。讓你的知識，更容易被看見。
