# videos/ — 实物操作视频放置目录

把最终网页要播放的 `.mp4` 文件直接放进本目录，然后编辑 `../index.html`：

1. 找到 `VIDEO SLOTS` 注释块（1 个 featured 大槽 + 4 个小槽）。
2. 每个槽内已备好注释掉的 `<video>` 标签：取消注释，把 `src` 改成
   `videos/你的文件.mp4`，保存即可 —— 槽内的虚线占位层会自动隐藏
   （页面底部脚本检测到 `video[src]` 就隐藏 `.placeholder`）。
3. 建议提供封面图：把截图放进 `../assets/`，填到 `poster="assets/xxx.jpg"`，
   避免加载前黑屏。
4. 若视频托管在 Bilibili / YouTube，用 `<iframe src="...">` 替换 `<video>`，
   外层容器已按 16:9 自适应，无需改样式。

命名建议（与 index.html 注释一致）：

| 文件名                  | 内容                                              |
| ----------------------- | ------------------------------------------------- |
| `paper_video.mp4`       | 论文成片（配音+BGM 宣传片，featured 大图，已入位） |
| `baseline_negative.mp4` | 初次部署：π₀ 负目标方向失败                        |
| `iter2_repair.mp4`      | Iteration-2 per-sign 修复后                        |
| `iter3_heldout.mp4`     | Iteration-3 self-imitation 修复后 held-out 幅值    |
| `operation_cycle.mp4`   | 一次完整操作循环（turn/hold/release/reset）        |

注意：视频文件较大，若整站走 git 仓库托管，确认 `.gitignore` 策略或改用
外链（B 站/YouTube/CDN）+ iframe 嵌入。
