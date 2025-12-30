# クロールパス（Crawl Path）

このページでは、AVFZK サイトにおける **クローラーの巡回経路** を解説します。

対象サイト  
[https://www.avfzk.com/](https://www.avfzk.com/)

---

## 1. サイト全体の階層

```text
/
├─ 🆕 新着情報（/）
├─ 📅 本日出勤 (/today/)
├─ ♀ 女優一覧 (/girllist/)
├─ 📍 エリア (/area/)
├─ 🔠 ジャンル (/genre/)
├─ 🔓 無修正 (/uncensoredlist/)
└─ 🔥 人気 (/popular/)
すべてのページはトップページから辿れる

サイト内リンクを必ず設置

2. 女優ページまでの経路例
/girllist/ → /actress/{encoded-name} → /genre/{genre-name} → /area/{area-name}

一覧ページ → 個別ページ → ジャンル / エリア

内部リンクを自動生成で接続
