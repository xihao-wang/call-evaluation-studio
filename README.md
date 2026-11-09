# CALL Studio · 英语学习与评测工作台

公开网址：https://xihao-wang.github.io/call-evaluation-studio/

保留阅读、口语词汇、产品测试、AES、AWE 与回修对比模块的结果查询、筛选和导出。公开站点为静态浏览版；本机 Python 模型调用和共享写入不在 GitHub Pages 中运行。

## 发布结构

`release/site.zip.*` 是按顺序拆分的公开站点压缩包。GitHub Actions 将其合并、核对 SHA-256、解压并部署。解压后包含 HTML、CSS、JavaScript 及静态结果快照。

本仓库未包含 API 密钥、本机 SQLite、教师答案、个人简历、原始作业附件或原始录屏。公开数据为课程展示与练习用途。

## 本地预览

```sh
cat release/site.zip.* > site.zip
unzip site.zip -d site
python3 -m http.server --directory site 8080
```

## 更新

生成经过检查的公开站点压缩包，按顺序替换 release 分片，并更新工作流中的 SHA-256。推送 main 后自动部署。
