```markdown
# クロールパス（Crawl Path）

このページでは、AVFZK サイトにおける **クローラーの巡回経路** を解説します。

対象サイト  
https://www.avfzk.com/

---

## 1. サイト全体の階層



/
├─ 🆕 新着情報（/）
├─ 📅 本日出勤 (/today/)
├─ ♀ 女優一覧 (/girllist/)
├─ 📍 エリア (/area/)
├─ 🔠 ジャンル (/genre/)
├─ 🔓 無修正 (/uncensoredlist/)
└─ 🔥 人気 (/popular/)


- すべてのページはトップページから辿れる
- サイト内リンクを必ず設置

---

## 2. 女優ページまでの経路例



/girllist/ → /actress/{encoded-name} → /genre/{genre-name} → /area/{area-name}


- 一覧ページ → 個別ページ → ジャンル / エリア  
- 内部リンクを自動生成で接続

---

## 3. クロールの深さと優先度

- 最大深さ：3  
- 高優先度ページ：トップページ、女優一覧、人気ページ  
- 低優先度ページ：個別女優ページ（大量存在）

---

## 4. 次のステップ

- sitemap.xml との整合性確認
- 内部リンク戦略（internal-link-strategy.md）と連動
- JSON-LD 構造化データをクロール経路に組み込み
