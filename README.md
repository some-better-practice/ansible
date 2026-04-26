要先 source .venv/bin/activate 才能執行 molecule。

分階段執行（除錯用）
molecule test 會跑完整流程並自動刪容器。除錯時改用分步驟：


# 1. 建立容器
molecule create

# 2. 跑 converge（套用 role）
molecule converge

# 3. 跑 verify（驗證）
molecule verify

# 4. 進容器手動檢查
molecule login

# 5. 完成後刪除容器
molecule destroy