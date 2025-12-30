# 構造化データ（Structured Data）

このページでは、AVFZK サイトで使用している **JSON-LD による構造化データ** を解説します。

対象サイト  
https://www.avfzk.com/

---

## 1. 個別女優ページの構造化データ

```json
{
  "@context": "https://schema.org",
  "@type": "Person",
  "name": "女優名",
  "alternateName": "読み仮名",
  "image": "https://www.avfzk.com/listimg/romaname/1.webp",
  "url": "https://www.avfzk.com/actress/encodedname"
}

@type は Person

name は女優の本名

alternateName は読み仮名

image はプロフィール画像

url は女優ページ URL

2. 一覧ページ（ItemList）
{
  "@context": "https://schema.org",
  "@type": "ItemList",
  "name": "女優一覧",
  "numberOfItems": 123,
  "itemListElement": [
    {
      "@type": "Person",
      "position": 1,
      "name": "女優A",
      "alternateName": "じょゆうA",
      "image": "https://www.avfzk.com/listimg/a/1.webp",
      "url": "https://www.avfzk.com/actress/encodedA"
    }
  ]
}


ItemList で全女優を列挙

position で並び順を明示

Person タイプで個別情報を明確化

3. SEO効果

Google 検索結果にリッチリザルト表示される可能性

内部リンクと組み合わせてサイト全体の評価を向上

クローラーが情報を正確に理解可能


---

## 3️⃣ `docs/ja/crawl-path.md`

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
