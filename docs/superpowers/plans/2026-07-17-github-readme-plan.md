# GitHub 首頁優化 Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** 建立一個以成果、爆款調研價值和無腦安裝為核心的 GitHub README 首頁，並將展示素材同步到公開倉庫。

**Architecture:** README 是唯一入口，先用一句話價值和真實成品抓住注意力，再用工作流程、兩種模式、安裝與使用範例降低門檻。展示圖片集中在 `assets/showcase/`，避免 README 依賴本機路徑。

**Tech Stack:** GitHub Markdown、PNG、Codex Agent Skills、Git。

## Global Constraints

- 一律使用繁體中文和通俗說法。
- 不宣稱保證爆款，不捏造成效數據。
- 展示圖必須是本專案實際產出的 Image2.0 成品。
- 新手必須能用一句自然語言完成安裝與開始使用。
- 首頁參考 `mythkiven/rednote-director-skill` 的資訊順序，但不複製文案或圖片。

---

### Task 1: 整理展示圖片

**Files:**
- Create: `assets/showcase/codex-5-tools-cover.png`
- Create: `assets/showcase/ai-tools-cover.png`
- Create: `assets/showcase/ai-tools-research.png`
- Create: `assets/showcase/ai-tools-map.png`
- Create: `assets/showcase/ai-tools-kit.png`

**Interfaces:**
- Consumes: 工作區內已生成的 Image2.0 PNG 成品。
- Produces: README 可用相對路徑引用的五張展示圖。

- [ ] **Step 1: 建立展示素材資料夾**

Run: `mkdir -p assets/showcase`

Expected: `assets/showcase/` 存在。

- [ ] **Step 2: 複製並重新命名五張成品圖**

Run: 從 `Codex五個必裝工具_Image2.0` 與 `2026職場AI工具_Image2.0真實Logo版/output` 複製指定 PNG。

Expected: 五個英文檔名的 PNG 均可讀取。

- [ ] **Step 3: 驗證圖片**

Run: `file assets/showcase/*.png`

Expected: 五張圖皆顯示為 PNG image data。

### Task 2: 建立轉化型 README

**Files:**
- Create: `README.md`

**Interfaces:**
- Consumes: `assets/showcase/*.png`、`SKILL.md` 的實際工作流程。
- Produces: GitHub 首頁的完整介紹、安裝和使用入口。

- [ ] **Step 1: 寫入 README**

README 必須依序包含：

1. `qiqixiaohongshu-carousel` 與主張「一句話，生成符合爆款邏輯的精美小紅書圖文」。
2. 四個短標籤：爆款調研、標題優化、封面對標、Image2.0 成品。
3. 一張主封面和三張同系列內頁。
4. 「不是普通排版工具」對比表。
5. 六步工作流。
6. 只有主題／已有文案兩種使用方式。
7. 對話式安裝與手動安裝方式。
8. 三個可直接複製的使用範例。
9. 適合場景、輸入格式、常見問題、更新方式與 Star 引導。

Expected: README 第一屏先展示價值與圖片，安裝方法在頁面前半部出現。

- [ ] **Step 2: 驗證 README 內所有本地圖片路徑**

Run: 從 README 擷取 `assets/showcase/` 路徑並逐一確認檔案存在。

Expected: 無缺圖。

- [ ] **Step 3: 檢查文字承諾**

Run: 搜尋「保證爆款」「一定爆款」和不存在的使用者數據。

Expected: README 不含誇大保證；1–2 小時以流程目標描述。

### Task 3: 驗證並發佈

**Files:**
- Modify: Git 索引與提交記錄。

**Interfaces:**
- Consumes: 完成的 README 與展示圖。
- Produces: GitHub 公開倉庫首頁。

- [ ] **Step 1: 執行本地檢查**

Run: `git diff --check`，並重新執行 Skill 驗證器。

Expected: 無格式錯誤，Skill is valid。

- [ ] **Step 2: 檢查修改範圍**

Run: `git status -sb`

Expected: 只有 README、展示圖和本次設計文件相關變更。

- [ ] **Step 3: 提交首頁版本**

Run: `git add README.md assets/showcase docs/superpowers && git commit -m '優化 Skill GitHub 首頁'`

Expected: 產生新的本地提交。

- [ ] **Step 4: 同步 GitHub**

優先測試 SSH 推送；若帳號沒有 SSH 憑證，建立乾淨的手動上傳包，只包含 README 與 `assets/showcase/`，交由使用者一次拖曳上傳。

Expected: GitHub 首頁顯示 README 和五張成品圖。

- [ ] **Step 5: 線上驗證**

透過 GitHub 連接器讀取 `README.md` 與一張展示圖路徑。

Expected: 兩者都能從 `aiwithlanny/qiqixiaohongshu-carousel` 的 `main` 分支讀取。
