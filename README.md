# AI 主神資料庫｜遊戲存檔鏡像

這個儲存庫是 **ChatGPT 核對遊戲資料的正式 GitHub 來源**。

主神資料庫網站只提供人類閱讀介面；JSON 存檔與版本歷史統一由本儲存庫保存。

## ChatGPT 讀取順序

1. [存檔索引](./current-state/manifest.json)
2. [最新正式存檔](./current-state/latest.json)
3. 需要核對特定版本時，讀取 `current-state/v版本號.json`
4. [相容入口](./current-state.json) 與 latest 內容相同

目前正式版本：

- [v94 封存](./current-state/v94.json)

## 同步規則

- 資料來源：主神資料庫 Supabase CURRENT STATE
- 自動同步：約每 30 分鐘
- 每個版本以獨立 JSON 封存，不會只留下最新檔案
- ChatGPT 應優先採用索引所指向的最高版本
- GitHub 是核對與版本保存來源，不提供遊戲資料寫入
- 主神資料庫網站仍是玩家查看角色、能力、裝備、物資與副本紀錄的介面

> 若 GitHub 最新檔案與網站畫面短暫不同，通常是定時同步尚未執行；待下一次同步後再以較高版本為準。
