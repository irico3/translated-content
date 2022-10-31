---
title: Firefox 106 for developers
slug: Mozilla/Firefox/Releases/106
l10n:
  sourceCommit: f7750c2c7d2d7b494b8ccd550af5b95c8d2a1843
---

{{FirefoxSidebar}}

このページでは、開発者に影響する Firefox 106 の変更点をまとめています。Firefox 106 は、米国時間 2022 年 10 月 18 日にリリースされました。

## ウェブ開発者向けの変更点一覧

### HTML

#### 廃止

### MathML

- MathML の [`<semantics>`](/ja/docs/Web/MathML/Element/semantics) および [`<maction>`](/ja/docs/Web/MathML/Element/maction) 要素が、デフォルトで最初の子要素のみ表示するようになりました ({{bug(1588733)}})。

### CSS

- [@supports](/ja/docs/Web/CSS/@supports) アットルールで `font-tech()` および `font-format()` 関数をサポートしました。
  これらの関数で、指定したフォント技術やフォント形式をブラウザーがサポートしているかを確認できます。また、確認結果に基づいて CSS スタイルを適用できます ({{bug(1786493)}})。

#### 廃止

### JavaScript

#### 廃止

### HTTP

#### 廃止

### セキュリティ

#### 廃止

### API

#### DOM

- [`HTMLMetaElement.media`](/ja/docs/Web/API/HTMLMetaElement/media) プロパティをサポートしました。このプロパティは、`media` の値 (例:  `max-width: 600px`) に応じてさまざまなテーマカラーを設定できます。
  `media` プロパティを持つ meta 要素を使用すると、ブラウザーは指定したメディアクエリー向けのページまたは UI の色を設定するために、`theme-color` と合わせて `content` の値を使用できます ({{bug(1706179)}})。

#### Media、WebRTC、Web Audio

#### 廃止

### WebAssembly

#### 廃止

### WebDriver conformance (WebDriver BiDi, Marionette)

#### WebDriver BiDi

- `script.getRealms` の基本的なサポートを追加しました。現在は、window レルムと sandbox レルムを含む `WindowRealmInfo` 型に限定されています ({{bug("1766240")}})。

- `browsingContext.load` イベントをサポートしました。これは、ブラウジングコンテキストのウィンドウの `load` イベントをきっかけにして発生します ({{bug("1756619")}})。

- シリアライズしたリモートの値向けの強い参照を保持するための、オブジェクト参照ストアを追加しました ({{bug("1770736")}})。

- オブジェクト参照ストアで作成したリモート参照のデシリアライズをサポートしました ({{bug("1788124")}})。

- `script.evaluate`、`script.callFunction`、`script.disown` コマンドを完全サポートしました ({{bug("1778976")}})。

#### Marionette

- [Actions](https://w3c.github.io/webdriver/webdriver-spec.html#actions) 向けに `wheel` 入力ソースをサポートしました。これはホイールタイプの入力デバイスに関連づけられます ({{bug("1746601")}})。

- GeckoView ベースのアプリケーション (例: Android 版 Firefox) のタブを開くおよび閉じる操作をサポートしました ({{bug("1506782")}})。

## アドオン開発者向けの変更点一覧

- [`"background"`](/ja/docs/Mozilla/Add-ons/WebExtensions/manifest.json/background) マニフェストキーの `"persistent"` プロパティを `false` に設定することが、Manifest V2 において (バックグラウンドページを非永続化するため) デフォルトで可能になりました。
- `"content_security_policy"` マニフェストキーの `object-src` ディレクティブが省略可能になりました ({{bug(1766881)}})。詳しくは `"content_security_policy"` のページで [object-src ディレクティブ](/ja/docs/Mozilla/Add-ons/WebExtensions/manifest.json/content_security_policy#object-src_directive) をご覧ください。

### 廃止

### その他

## 過去のバージョン

{{Firefox_for_developers(105)}}