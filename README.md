# EORZEA CALENDAR — SS WALLPAPER MAKER Ver1.0

FF14のスクリーンショットをスマホ用壁紙に加工し、月間カレンダーを重ねられる、1ファイル完結の非公式Webツールです。

## 使い方

1. `index.html` をChrome / Safari / Edgeなどのブラウザで開きます。
2. 「SS画像を選択する」からスクリーンショットを指定します。
3. プレビュー内をドラッグしてSS位置を調整します（画像の拡大も可能）。
4. 年月、週の始まり、カレンダーの配置・サイズ・配色を設定します。
5. 必要に応じて `© SQUARE ENIX` の表示位置も左・中央・右から選びます。
6. 出力解像度を選択し、「スマホ用壁紙をPNGで保存」を押します。
7. SSなしで「カレンダーだけ透過PNGで保存」もできます。

## 公開方法

ローカルのフォルダ構成：

```text
Github/
└── SS-WALLPAPER-MAKER/
    ├── index.html
    └── README.md
```

GitHubで `SS-WALLPAPER-MAKER` リポジトリを作成し、そのルートに `index.html` と `README.md` を配置してください。GitHub Pagesの設定で `Deploy from a branch` → `main` → `/(root)` を選択すると、以下のURL形式でアクセスできます。

`https://cyanstella.github.io/SS-WALLPAPER-MAKER/`

サーバー処理やライブラリのインストールは不要です。

## Ver1.0（2026年10月2日）

- 初回正式公開版
- 曜日表示：MON / TUE / WED / THU / FRI / SAT / SUN
- 初期状態は月曜始まり（日曜始まりにも切替可能）
- フォント：モダン / 明朝風 / 丸文字風
- 年表示を拡大
- `© SQUARE ENIX` を左 / 中央 / 右から配置選択可能

## 機能

- 完全クライアント処理（画像をサーバーにアップロードしません）
- 月の実際の日数・曜日に対応したカレンダー（日曜／月曜始まり）
- ブラウザプレビューとPNG書き出しの共通描画ロジック
- マウスやタッチでのスクリーンショット移動と拡大
- カレンダー位置、文字、背景色と透明度、3スタイル
- 高解像度PNG / 透過カレンダーPNG
- 日本語UI・スマホ対応

## Cloudflare Web Analytics

- EORZEA PROFILE STUDIOなどと同じ解析トークンを `index.html` の `</body>` 直前に設置しています。追加でトークンを発行する必要はありません。
- GitHub Pages公開後は、Cloudflare Web Analyticsの管理画面でアクセス状況を確認できます。共通トークンで集計されるため、このツールのみを確認する場合はページURL `/SS-WALLPAPER-MAKER/` で絞り込んでください。
- 画像の読み込み・合成・PNG書き出しは引き続き端末内で行い、FF14のSS画像そのものをCloudflareに送信する機能はありません。Web Analyticsによりページのアクセス情報はCloudflareに送られます。

## ご注意

祝日・個人予定は表示しません。画像の読み込みはブラウザの対応形式に依存します。スマホで壁紙に設定する操作はOS側で行ってください。

FINAL FANTASY XIV © SQUARE ENIX。非公式のファン制作ツールです。
