# タイトー様インタビューLP

タイトーらくがキッズ様とサンサンキッズTVのYouTubeタイアップ成功事例を紹介するランディングページです。

## プロジェクト概要

このLPは、デジタルプレイグラウンド施設とYouTubeキャラクターのコラボレーション事例を、インタビュー形式で紹介するページです。オンラインとオフラインを融合したプロモーション施策の成功事例として、親子集客の実績を伝えます。

## ファイル構成

```
/Volumes/aqw_8TB/LPtest/taito/
├── index.html              # メインHTMLファイル
├── styles.css              # スタイルシート
├── images/                 # 画像ディレクトリ
│   ├── README.md          # 画像配置ガイド
│   ├── hero-image.jpg     # ヒーロー画像（1200×600px）
│   ├── profile.jpg        # プロフィール写真（240×240px）
│   ├── facility-interior.jpg        # 施設内の様子（800×450px）
│   ├── character-filming.jpg        # キャラクター撮影風景（800×450px）
│   ├── visitors.jpg                 # 来場者の様子（800×450px）
│   ├── character-interaction.jpg    # キャラクター交流（800×450px）
│   └── service-overview.jpg         # サービス概要（800×400px）
└── README.md              # このファイル
```

## 技術仕様

### HTML
- **DOCTYPE**: HTML5
- **言語**: 日本語（ja）
- **文字セット**: UTF-8
- **セマンティックマークアップ**: header, main, section, article使用

### CSS
- **フォント**: Hiragino Kaku Gothic ProN, Meiryo, sans-serif
- **ベースカラー**: #ffffff
- **アクセントカラー**: #f43500（オレンジレッド）、#f2e100（イエロー）
- **レスポンシブブレイクポイント**:
  - デスクトップ: 993px以上
  - タブレット: 768px〜992px
  - モバイル: 767px以下

### レスポンシブ対応
- ✅ モバイルファースト設計
- ✅ タブレット・デスクトップ対応
- ✅ 画像の最適化表示
- ✅ タッチ操作対応

### アクセシビリティ
- ✅ セマンティックHTML使用
- ✅ 全画像にalt属性設定
- ✅ 適切な見出し階層（h1→h2→h3）
- ✅ カラーコントラスト比WCAG AA準拠
- ✅ キーボードナビゲーション対応

## 使用方法

### 1. 基本的な表示

ブラウザで `index.html` を開くだけで表示されます。

```bash
# ローカルサーバーで起動する場合（Python）
python -m http.server 8000

# ブラウザで開く
open http://localhost:8000
```

### 2. コンテンツのカスタマイズ

#### テキストの変更
`index.html` を開き、以下の箇所を編集してください：

- **施設名**: 「タイトー らくがキッズ」
- **インタビュー対象者名**: 「●●」の部分を実名に変更
- **URL**: aquwa.co.jp関連のリンク先を確認・更新

#### 画像の差し替え
1. `images/` ディレクトリに実際の画像を配置
2. `images/README.md` を参照して適切なサイズで用意
3. ファイル名は既存のものに合わせるか、HTML内のsrc属性を更新

#### カラーの変更
`styles.css` の以下の変数を変更してください：

```css
/* メインアクセントカラー */
#f43500 → お好みの色

/* サブアクセントカラー */
#f2e100 → お好みの色
```

## セクション構成

1. **ヘッダー**: タイトルとサブタイトル
2. **ヒーロー画像**: メインビジュアル
3. **リード文**: 施策の概要紹介
4. **プロフィール**: インタビュー対象者情報
5. **インタビュー**: Q&A形式（6問）
   - Q1: 導入背景・課題
   - Q2: 検討プロセス・選定理由
   - Q3: 実施内容の概要
   - Q4: 成果・効果
   - Q5: 印象的なエピソード
   - Q6: 今後の展望
6. **まとめ**: 施策の総括
7. **CTA**: アクションボタン（お問い合わせ、資料請求）
8. **サービス紹介**: aquwaのサービス概要
9. **コンタクト**: お問い合わせ先情報

## カスタマイズポイント

### ボタンのリンク先を変更する

```html
<!-- index.html内のCTAボタン -->
<a href="https://aquwa.co.jp/contact" class="btn btn-primary">無料相談のお申し込み</a>

<!-- リンク先URLを変更 -->
<a href="YOUR_CONTACT_URL" class="btn btn-primary">無料相談のお申し込み</a>
```

### 動画埋め込みを追加する（オプション）

Q3またはQ4の後に動画を追加する場合：

```html
<div class="video-wrapper" style="position: relative; padding-bottom: 56.25%; height: 0; margin: 40px 0;">
    <iframe
        style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"
        src="https://www.youtube.com/embed/VIDEO_ID"
        frameborder="0"
        allowfullscreen>
    </iframe>
</div>
```

### フォントを変更する

`styles.css` の body セクションを編集：

```css
body {
    font-family: 'Your Preferred Font', 'Hiragino Kaku Gothic ProN', sans-serif;
}
```

## パフォーマンス最適化

### 画像の最適化
- 圧縮率: 70-80%推奨
- フォーマット: WebP形式の使用を推奨
- 遅延読み込み: 必要に応じて `loading="lazy"` 属性を追加

### srcset属性の追加例

```html
<img
    src="images/hero-image.jpg"
    srcset="images/hero-image-600.jpg 600w,
            images/hero-image-1200.jpg 1200w,
            images/hero-image-1800.jpg 1800w"
    sizes="(max-width: 767px) 100vw, 1200px"
    alt="タイトーらくがキッズ施設でのYouTubeキャラクター撮影風景">
```

## ブラウザ対応

- ✅ Chrome（最新版）
- ✅ Firefox（最新版）
- ✅ Safari（最新版）
- ✅ Edge（最新版）
- ✅ iOS Safari（iOS 12以降）
- ✅ Android Chrome（Android 8以降）

## トラブルシューティング

### 画像が表示されない場合
1. 画像ファイルが `images/` ディレクトリに配置されているか確認
2. ファイル名が正しいか確認（大文字小文字の区別に注意）
3. ブラウザのキャッシュをクリア

### レイアウトが崩れる場合
1. `styles.css` が正しく読み込まれているか確認
2. ブラウザの開発者ツールでCSSエラーを確認
3. ブラウザのズーム設定を100%に戻す

### レスポンシブが機能しない場合
1. HTMLの `<meta name="viewport">` タグが正しく記述されているか確認
2. ブラウザの開発者ツールでブレイクポイントを確認

## 更新履歴

- 2025-10-22: 初版作成（完全版レイアウト仕様書に基づく実装）

## ライセンス

© 2025 aquwa. All rights reserved.

## お問い合わせ

制作・技術的な質問については以下までご連絡ください：

- **メール**: info@aquwa.co.jp
- **お問い合わせフォーム**: https://aquwa.co.jp/contact
