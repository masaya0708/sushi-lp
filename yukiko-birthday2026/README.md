# 優喜子生誕祭2026 LP デプロイ手順書

このLPをインターネット上に公開するための手順です。GitHubとCloudflare Pagesを連携させることで、無料で安全に公開できます。

## 1. ローカルでのプレビュー方法
1. このフォルダ内の `index.html` を、お使いのブラウザ（Chromeなど）に直接ドラッグ＆ドロップしてください。
2. 動画や画像が正しく表示されるか確認してください。

## 2. GitHubへのアップロード
1. GitHubで新しいリポジトリ（例: `yukiko-birthday-2026`）を作成してください。
2. 以下のコマンドをターミナル（PowerShellなど）で実行し、ファイルをPushします。

```powershell
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin [あなたのGitHubリポジトリのURL]
git push -u origin main
```

## 3. Cloudflare Pagesでの公開
1. [Cloudflare ダッシュボード](https://dash.cloudflare.com/)にログインします。
2. 「Workers & Pages」 > 「Pages」 > 「GitHubに接続」を選択します。
3. 先ほど作成したリポジトリを選択します。
4. 設定はそのままで「保存してデプロイ」をクリックします。
5. 数分後、提供されるURL（https://xxx.pages.dev）でLPが公開されます。

## 注意事項
- **動画ファイルについて**: `yukiko's birthday2025.mp4` はファイルサイズが大きいため、GitHubの制限（通常100MB以下）にご注意ください。もしPushできない場合はご連絡ください。GIFへの変換などの対応を検討します。
- **UTA-GEリンク**: `index.html` の下方にある `<a href="#" class="btn-primary">` の `#` を、後日入手するUTA-GEのリンクに書き換えてからPushしてください。
