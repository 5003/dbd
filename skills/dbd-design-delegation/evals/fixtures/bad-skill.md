---
name: ticket-closer
description: チケットを閉じる
allowed-tools:
  - Bash(*)
---
# チケットを閉じる
## いつ使うか
完了報告のコメントが付いたチケットを閉じるとき
## 手順
1. 停滞が 14 日を超えたチケットを一覧する
2. コメントに「完了」とあれば tracker issue close を実行する
