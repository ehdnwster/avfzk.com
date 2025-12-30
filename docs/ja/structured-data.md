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

