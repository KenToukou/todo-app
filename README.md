# Todo App

シンプルなTodoアプリです。ReactとViteを使って構築されています。

## 機能

- タスクの追加
- タスクの完了/未完了の切り替え
- タスクの削除

## インストールと実行

1. 依存関係をインストール:
   ```
   npm install
   ```

2. 開発サーバーを起動:
   ```
   npm run dev
   ```

3. ブラウザで http://localhost:5173 にアクセス

## ビルド

```
npm run build
```

## プレビュー

```
npm run preview
```

## GitHub リポジトリの作成とプッシュ

このプロジェクトをGitHubにアップロードするための手順です。

### 一括作成とプッシュ

```bash
gh repo create todo-app --public --source=. --remote=origin --push
```

**目的**: GitHub CLIを使って新しいリポジトリを作成し、ローカルのコードをプッシュします。`--public`で公開リポジトリ、`--source=.`で現在のディレクトリをソース、`--remote=origin`でリモート名、`--push`で自動プッシュ。

### ステップバイステップの手順

1. ファイルをステージング:
   ```bash
   git add .
   ```
   **目的**: すべての変更をステージングエリアに追加して、次のコミットに含める準備をする。

2. コミット:
   ```bash
   git commit -m "Initial commit: Add Todo app with React and Vite"
   ```
   **目的**: ステージングされた変更をローカルリポジトリにコミットし、変更履歴を保存。

3. リモートリポジトリ作成:
   ```bash
   gh repo create todo-app --public
   ```
   **目的**: GitHubに"todo-app"という名前の公開リポジトリを作成。

4. リモートを追加:
   ```bash
   git remote add origin https://github.com/KenToukou/todo-app.git
   ```
   **目的**: ローカルリポジトリにGitHubリポジトリをリモートとして追加し、プッシュ先を設定。

5. プッシュ:
   ```bash
   git push -u origin main
   ```
   **目的**: ローカルコミットをGitHubリポジトリにプッシュし、origin/mainをupstreamブランチとして設定。

## GitHub Pagesへのデプロイ

プロジェクトをGitHub Pagesにデプロイして公開します。

### 注意事項
GitHub Pagesではリポジトリ名をベースパスとして設定する必要があります。`vite.config.js`に`base: '/todo-app/'`が設定されています。これにより、GitHub Pages（https://kentoukou.github.io/todo-app/）で正しく動作します。

### デプロイスクリプト実行

```bash
npm run deploy
```

**目的**: gh-pagesパッケージを使ってdistフォルダの内容をGitHub Pagesにデプロイします。これにより、アプリが https://kentoukou.github.io/todo-app/ で公開されます。

### 手動デプロイ手順

1. ビルド:
   ```bash
   npm run build
   ```
   **目的**: プロジェクトをビルドして静的ファイルを生成。

2. デプロイ:
   ```bash
   npx gh-pages -d dist
   ```
   **目的**: distフォルダをGitHub Pagesにプッシュ。