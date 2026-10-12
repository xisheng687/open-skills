# Open Skills · 公開 Agent 技能庫

[简体中文](README.md) · [繁體中文](README.zh-Hant.md) · [English](README.en.md) · [Français](README.fr.md) · [Deutsch](README.de.md) · [Español](README.es.md)

可公開分享、按需使用的實用 Agent Skills 合集。以簡體中文為主要說明，另提供繁體中文、英語、法語、德語和西班牙語。只需選擇需要的技能，不必一次安裝全部內容。

## 分類與技能目錄

| 分類 | 技能 | 解決的問題 | 下載 |
| --- | --- | --- | --- |
| Agent 工具與互通 | [Agent 工具探索與修復](skills/agent-tool-discovery/README.zh-Hant.md) | 解決工具在一個 Agent 能用、換另一個卻找不到的問題；檢查 Skills、MCP 與 CLI 的接入並保留原設定。 | [ZIP](https://github.com/xisheng687/open-skills/releases/download/agent-tool-discovery-v1.0.2/agent-tool-discovery.zip) |

目前公開發布 **1 個 Skill**。完整技能包含執行指令、參考資料、中英文提示詞及六種語言的使用說明，不含維護者電腦的其他技能或私人資料。

## 下載與使用

1. 下載單一技能 ZIP；也可下載整個倉庫，再取出完整的 `skills/<技能名稱>/`。
2. 保留全部檔案、參考資料和授權條款；倉庫 ZIP 並不是單一技能匯入包。
3. 依[繁體中文指南](skills/agent-tool-discovery/README.zh-Hant.md)安裝，或直接使用完整的[中文提示詞](skills/agent-tool-discovery/references/client-prompt.zh-CN.md)／[英文提示詞](skills/agent-tool-discovery/references/client-prompt.en.md)。可以要求 Agent 用繁體中文回答。

不同產品的安裝路徑與呼叫方式不一定相同，必須依版本確認；雲端 Agent 未必能讀取本機檔案。下載或安裝不代表授權執行修復。

## 新增更多技能

維持 `skills/<名稱>/` 的獨立目錄；分類和標籤放在技能中繼資料，避免多層分類目錄影響安裝。新增中文主說明、英文輔助說明及需要的其他翻譯，並更新分類目錄。詳見[貢獻規範](CONTRIBUTING.md)（中英文）。

## 隱私與驗證

只提交通用指令與公開資料，不提交憑證、電腦清單、私人路徑、內部服務網址、備份或客戶資料。靜態檢查和打包通過，不代表已在所有客戶端實際執行。

[MIT 授權條款](LICENSE)。獨立技能包也附有授權條款。
