readme_content = r'''# DAISEN UMIHOTARU Official Website

鳥取県大山町御来屋にある一棟貸し宿「DAISEN UMIHOTARU」の公式ウェブサイト。
「波の音を聴きながら、大山で暮らす旅」をコンセプトに、静謐で心地よい滞在体験をWeb上で表現しています。

## 技術スタック

* **HTML5**: セマンティックなマークアップ
* **Tailwind CSS (CDN)**: スタイリングおよびレスポンシブデザイン
* **GSAP (ScrollTrigger)**: スクロール連動アニメーション
* **Lenis**: スムーズスクロール制御
* **Lucide Icons**: アイコンセット

## ディレクトリ構造

デプロイ時は以下の構造を維持してください。画像パスが正しく機能するために必須です。

```text
.
├── index.html          # メインファイル
├── README.md           # 本ファイル
└── assets/
    └── images/         # 画像フォルダ
        ├── fv.jpg      # ファーストビュー（海景など）
        ├── view.jpg    # 窓からの景色
        ├── living.jpg  # リビング
        ├── kitchen.jpg # キッチン
        ├── bath.jpg    # バスルーム
        ├── bedroom.jpg # 寝室
        ├── local-food.jpg  # 釣り体験イメージ
        ├── mikuri-dinner.jpg # mikuri夕食イメージ
        └── ping-pong.jpg # 卓球・遊びイメージ
```

## ローカルでの確認方法

1.  このリポジトリをクローンまたはダウンロードします。
2.  `index.html` をブラウザ（Chrome, Safari, Edge等）で開くだけで動作します。
    * ※ 外部CDNを利用しているため、インターネット接続が必要です。

## デプロイ（GitHub Pages）

1.  GitHubリポジトリの **Settings** タブを開きます。
2.  サイドバーの **Pages** を選択します。
3.  **Build and deployment** > **Source** で `Deploy from a branch` を選択します。
4.  **Branch** で `main` (または `master`) を選択し、`/ (root)` のまま **Save** をクリックします。
5.  数分後、表示されるURL（例: `https://username.github.io/repo-name/`）にて公開されます。

## ライセンス

Copyright © 2025 DAISEN UMIHOTARU. All Rights Reserved.
'''

    # 1. ルートディレクトリの作成
    if not os.path.exists(root_dir):
        os.makedirs(root_dir)
        print(f"ディレクトリを作成しました: {root_dir}")

    # 2. index.htmlの作成
    with open(os.path.join(root_dir, "index.html"), "w", encoding="utf-8") as f:
        f.write(html_content)
    print(f"ファイルを作成しました: {os.path.join(root_dir, 'index.html')}")

    # 3. README.mdの作成
    with open(os.path.join(root_dir, "README.md"), "w", encoding="utf-8") as f:
        f.write(readme_content)
    print(f"ファイルを作成しました: {os.path.join(root_dir, 'README.md')}")

    # 4. 画像用フォルダの作成
    images_dir = os.path.join(root_dir, "assets", "images")
    if not os.path.exists(images_dir):
        os.makedirs(images_dir)
        print(f"ディレクトリを作成しました: {images_dir}")

    # 5. 画像配置の案内用ファイル作成
    with open(os.path.join(images_dir, "PUT_IMAGES_HERE.txt"), "w", encoding="utf-8") as f:
        f.write("このフォルダに fv.jpg, view.jpg, mikuri-dinner.jpg, ping-pong.jpg などの画像ファイルを配置してください。")
    print(f"ファイルを作成しました: {os.path.join(images_dir, 'PUT_IMAGES_HERE.txt')}")

    print("\nプロジェクトの準備が完了しました！")
    print(f"'{root_dir}' フォルダをGitHubにアップロードしてください。")

if __name__ == "__main__":
    create_project()