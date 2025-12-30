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
