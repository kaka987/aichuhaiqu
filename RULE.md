## 所有时间参考选取系统当前最新时间
## 文档撰写规范
- AI工具文档撰写前，请先阅读 `rules/ai-tools-doc-template.md` 中的规范和模板
- 原始素材放置在 `assets/docs/` 目录下（已 gitignore，不会提交）
- 新增文档后须同步更新 `docs/zh/_sidebar.md`
## 同步命令
- 全量同步
```powershell
$commitSha = (git rev-parse HEAD).Trim(); $apiKey = (Get-Content "$env:USERPROFILE\.litestartup\credentials" -Raw).Trim(); $body = @{ commit_sha = $commitSha; domain_slug = "domain-9cdc304ab3bd18a98396fd3fba0104f3" } | ConvertTo-Json; $r = Invoke-RestMethod -Uri "https://api.litestartup.com/client/v2/repo-sync/trigger" -Method POST -Headers @{ Authorization = "Bearer $apiKey"; "Content-Type" = "application/json" } -Body ([System.Text.Encoding]::UTF8.GetBytes($body)); "code=$($r.code) msg=$($r.message)"; "inserted=$($r.data.synced.inserted.Count) updated=$($r.data.synced.updated.Count) skipped=$($r.data.synced.skipped_count)"; if ($r.data.synced.inserted.Count -gt 0) { $r.data.synced.inserted }; if ($r.data.synced.updated.Count -gt 0) { $r.data.synced.updated }; if ($r.data.needs_confirm.Count -gt 0) { $r.data.needs_confirm | ConvertTo-Json -Depth 3 }; if ($r.data.conflicts.Count -gt 0) { $r.data.conflicts | ConvertTo-Json -Depth 3 }
```
- 按需同步
```powershell
$commitSha = (git rev-parse HEAD).Trim(); $apiKey = (Get-Content "$env:USERPROFILE\.litestartup\credentials" -Raw).Trim(); $body = @{ commit_sha = $commitSha; domain_slug = "domain-9cdc304ab3bd18a98396fd3fba0104f3";paths = @("website/index.html", "docs/zh/index.md")} | ConvertTo-Json; $r = Invoke-RestMethod -Uri "https://api.litestartup.com/client/v2/repo-sync/trigger" -Method POST -Headers @{ Authorization = "Bearer $apiKey"; "Content-Type" = "application/json" } -Body ([System.Text.Encoding]::UTF8.GetBytes($body)); "code=$($r.code) msg=$($r.message)"; "inserted=$($r.data.synced.inserted.Count) updated=$($r.data.synced.updated.Count) skipped=$($r.data.synced.skipped_count)"; if ($r.data.synced.inserted.Count -gt 0) { $r.data.synced.inserted }; if ($r.data.synced.updated.Count -gt 0) { $r.data.synced.updated }; if ($r.data.needs_confirm.Count -gt 0) { $r.data.needs_confirm | ConvertTo-Json -Depth 3 }; if ($r.data.conflicts.Count -gt 0) { $r.data.conflicts | ConvertTo-Json -Depth 3 }
```
