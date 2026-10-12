# Agent 工具探索與修復

[简体中文](README.md) · [繁體中文](README.zh-Hant.md) · [English](README.en.md) · [Français](README.fr.md) · [Deutsch](README.de.md) · [Español](README.es.md)

**分類：** Agent 工具與互通 · **版本：** 1.0.2

## 解決什麼問題？

「明明安裝過，換一個 Agent 卻說找不到。」技能目錄、MCP 設定與登入狀態各自獨立，終端機與桌面程式的 PATH 也可能不同，造成重複安裝和版本不一致。

這個 Skill 會盤點本機 Agent 與工具，優先共用中央技能來源，依實際支援情況使用原生讀取、個別軟連結或受控複製。MCP 依各客戶端格式接入，CLI 檢查路徑與執行環境，最後建立本地工具索引並驗證能否探索與呼叫。

## 下載與安裝

下載[獨立技能 ZIP](https://github.com/xisheng687/open-skills/releases/download/agent-tool-discovery-v1.0.2/agent-tool-discovery.zip)，或從倉庫取出完整的 `skills/agent-tool-discovery/`。保留所有檔案與參考資料；不要只下載 SKILL.md，也不要把整個倉庫 ZIP 當作單一技能包。

支援中央目錄的本地客戶端可使用 `~/.agents/skills/agent-tool-discovery/`；Claude Code 使用 `~/.claude/skills/agent-tool-discovery/`。實際路徑以產品和版本為準；同名技能先比較，不直接覆寫。

附上 ZIP 或解壓目錄，向 Agent 提出：

> 只將這個 Skill 安裝到目前客戶端已確認的使用者技能目錄。保留完整資料及同名衝突版本，在新工作階段確認能否探索。先不要執行檢查或修復流程。

## 使用方式

> 用 agent-tool-discovery 檢查這台電腦的 Agent 與工具共享問題，只回報，不修改。請用繁體中文回答。

> 用 agent-tool-discovery 檢查並修復已安裝 Agent 的工具探索問題。保留原設定，需要登入或解決衝突時再通知我。請用繁體中文回答。

Codex 可以用 `$agent-tool-discovery` 呼叫。也能直接複製完整的[中文提示詞](references/client-prompt.zh-CN.md)或[英文提示詞](references/client-prompt.en.md)，不必先安裝 Skill；提示詞預設允許範圍內的可逆修復，只想檢查時要明確說「僅審計，不修改」。

## 權限、隱私與限制

保留原設定、停用狀態與專案範圍；不安裝依賴、不升級、不刪原檔、不複製 OAuth 憑證或靜默散布內嵌金鑰。單純審計不寫索引、規則、備份或任務。下載或安裝不代表授權執行修復。

索引、備份與報告留在不受版本控制、不公開共享的本機位置。這是指令型 Skill，依賴 Agent 的本機存取能力；沒有常駐服務或上傳腳本。產品清單不是相容認證，無法驗證時必須標示。第三方產品仍有自己的資料處理政策。

## 可選定期檢查

完成後可選擇定期檢查。需要明確同意並確認頻率、排程機制和本機存取能力；預設唯讀，正常且無變化時不打擾。自動修復需要另外授權，登入和衝突不會自動處理。

[MIT 授權條款](LICENSE)。
