# [App Name] Application Repository

本リポジトリは、アプリケーションのソースコードおよび詳細仕様書を管理する子リポジトリです。
親リポジトリ (Portal) と連携し、ドキュメントの更新は自動的にポータルサイトへ反映されます。

## 🛠 開発ルール (Docs as Code)

### 1. ブランチ命名規則 [cite: 511]
| Prefix | 用途 | 例 |
| :--- | :--- | :--- |
| `feature/` | 新機能 (Minor Update) | `feature/login` |
| `bugfix/` | バグ修正 (Patch Update) | `bugfix/header` |
| `docs/` | ドキュメントのみ | `docs/manual` |

### 2. 実装・PRルール
* **ドキュメント同期:** コード修正時は、必ず同じPR内で `docs/` 配下も修正してください [cite: 526]。
* **PR記述:** Description に必ず `Closes #Issue番号` を記述してください [cite: 532]。
* **マージ:** **Squash and Merge** が必須です [cite: 543]。

## 📦 リリース
PRが `main` にマージされると、**自動的にタグが付与され**、親リポジトリへ同期・デプロイされます。手動でのタグ作成は禁止です 。