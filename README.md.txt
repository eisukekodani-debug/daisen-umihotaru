DAISEN UMIHOTARU Official Website

鳥取県大山町御来屋にある一棟貸し宿「DAISEN UMIHOTARU」の公式ウェブサイト。
「波の音を聴きながら、大山で暮らす旅」をコンセプトに、静謐で心地よい滞在体験をWeb上で表現しています。
日本語・英語・韓国語の3ヶ国語に対応しています。

技術スタック

HTML5: セマンティックなマークアップ

Tailwind CSS (CDN): スタイリングおよびレスポンシブデザイン

GSAP (ScrollTrigger): スクロール連動アニメーション

Lenis: スムーズスクロール制御

Lucide Icons: アイコンセット

Google Fonts:

日本語: Zen Old Mincho, Zen Kaku Gothic New

英語: Cormorant Garamond

韓国語: Noto Serif KR, Noto Sans KR

ディレクトリ構造

デプロイ時は以下の構造を維持してください。各言語ファイル間のリンクや画像パスが正しく機能するために必須です。

.
├── index.html          # 日本語版（メイン・ランディングページ）
├── index.en.html       # 英語版
├── index.kr.html       # 韓国語版
├── README.md           # 本ファイル
└── assets/
    └── images/         # 画像フォルダ (すべて .webp 形式)
        ├── fv.webp           # ファーストビュー
        ├── view.webp         # 窓からの景色
        ├── living.webp       # リビング
        ├── kitchen.webp      # キッチン
        ├── bath.webp         # バスルーム
        ├── bedroom.webp      # 寝室
        ├── floor-plan.webp   # 間取り図
        ├── local-food.webp   # 釣り体験イメージ
        ├── mikuri-dinner.webp # mikuri夕食イメージ
        └── ping-pong.webp    # 卓球・遊びイメージ


ファイル名の規則について（重要）

GitHub Pagesの仕様上、ファイル名の大文字・小文字は厳密に区別されます。また、言語切り替えリンクを正しく機能させるため、ファイル名は以下の通り統一してください。

推奨: index.en.html (ドット区切り)

非推奨: index_en.html (アンダーバー区切り)

ローカルでの確認方法

このリポジトリをクローンまたはダウンロードします。

index.html をブラウザ（Chrome, Safari, Edge等）で開くだけで動作します。

※ 外部CDN（Tailwind, GSAP等）を利用しているため、インターネット接続が必要です。

デプロイ（GitHub Pages）

GitHubリポジトリの Settings タブを開きます。

サイドバーの Pages を選択します。

Build and deployment > Source で Deploy from a branch を選択します。

Branch で main (または master) を選択し、/ (root) のまま Save をクリックします。

数分後、表示されるURL（例: https://username.github.io/repo-name/）にて公開されます。

更新手順

画像やテキストを修正した際は、以下のコマンド等でGitHubへプッシュしてください。

git add .
git commit -m "Update content"
git push origin main


ライセンス

Copyright © 2025 DAISEN UMIHOTARU. All Rights Reserved.