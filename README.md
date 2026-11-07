# だこちてギミック【ワールド版】説明サイト

GitHub Pages / Jekyll（just-the-docs）で公開する説明ページです。閲覧者向けの内容は「トップ」「ワールドへの導入」「遊び方」の3ページのみです。「遊び方」には各モードのUI画像3枚を掲載しています。

導入・遊び方の各ページにはDiscordの問い合わせ案内を掲載し、トップからも移動できます。案内の共通部分は `docs/_includes/contact.html` で管理します。

## 説明ページに使う画像

- `docs/assets/img/manual-title*.webp` — トップのタイトル画像（ユーザー提供画像）。幅640・960・1280・1672pxのWebPを用意し、画面幅と画面の精細さに合わせて読み分けます。縦横比を保って全体を表示し、読み込み領域をあらかじめ確保します。
- `docs/assets/img/vcc-manage-packages.webp` — VCCでパッケージ名を検索し、右端の「＋」で追加する画面
- `docs/assets/img/discord-contact.webp` — Discordの問い合わせチャンネル（ユーザー提供画像）
- `docs/assets/img/tmp-importer.webp` — TMP Essentialsの導入
- `docs/assets/img/mode-dako.webp` — だこちてモードの遊び方
- `docs/assets/img/mode-gymnastics.webp` — 組体操モードの遊び方
- `docs/assets/img/mode-battle.webp` — 投げ合いモードの遊び方

操作UI画像は現行PrefabをUnityで描画し、可逆圧縮のWebP形式で収録しています。VCCの導入案内とTMP Importerの案内はスクリーンショットです。画像は説明ページから拡大できます。

## 公開方法

1. リポジトリ直下へ `docs/`、`.gitignore`、`README.md` を配置します。
2. GitHubの **Settings → Pages → Deploy from a branch** で、ブランチ `main`・フォルダー `/docs` を選びます。
3. リポジトリ名が `player-carry-and-throw-pages` 以外なら `docs/_config.yml` の `baseurl` を更新します。

## 既存サイトを差し替える場合

次の旧ページは今回の簡略版では使用しません。**既存リポジトリから削除**してください（上書きだけでは残ります）。

`docs/status.md`, `docs/faq.md`, `docs/custom.md`, `docs/modes.md`, `docs/license.md`, `docs/third-party.md`, `docs/troubleshooting.md`

旧サイトの `docs/_site/`、`.git/`、`docs/Gemfile.lock` はZIPに含めていません。`docs/_site/` はビルド時に生成されます。

## ローカルでの確認

`docs/` に移動し、初回のみ `bundle install` を実行します。

```bash
bundle exec jekyll serve --baseurl=""
```

`http://localhost:4000/` で表示できます。

## 仕様の参照元

ユーザー提供のだこちてギミック【ワールド版】プロジェクト内の以下の一次資料を参照しています。

- `Packages/jp.aramaa.player-carry-and-throw/Documentation~/Installation.md`
- `Packages/jp.aramaa.player-carry-and-throw/Documentation~/ProductionSpec.md`

利用規約（ライセンス）は[GitHubのLICENSE.md](https://github.com/aramaa-vr/player-carry-and-throw/blob/master/LICENSE.md)で一元管理します。この説明サイトには規約本文やPDFを置かず、同じページへのリンクのみを掲載します。

バージョン・開発状況は公開ページに記載していません。
