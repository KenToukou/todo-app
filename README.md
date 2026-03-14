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