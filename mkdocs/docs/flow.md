# 機能開発/修正の基本フロー

```mermaid
flowchart TD
    clone["0. リポジトリを複製（初回のみ）"] --> pull["1. ローカルリポジトリを最新状態にする"]
    pull --> branch["2. ブランチを作成"]
    branch --> src["3. プログラム開発"]
    src --> add["4. ステージング"]
    add --> commit["5. コミット"]
    commit --> push[6. リモートに反映]
    push --> pullrequest[7. プルリクエストを作成]
    pullrequest --> review{"レビュー"}
    review -- "承認" --> merge["8. プルリクエストをマージ"]
    review -- "差戻し"　--> src

```
## 0. リポジトリを複製（初回のみ）
---
```bash
> git clone http://{githubユーザー名}:{token}@github.com/{リポジトリパス}
```
- [tokenの発行方法](token.md)

## 1. ローカルリポジトリを最新状態にする
---
### コマンド
```bash
> git pull origin main
```

### Sourcetree

## 2. ブランチを作成
---

### コマンド
```bash
> git checkout {作成するブランチの元となるブランチ名}
> git branch -c {ブランチ名}
```
`main`ブランチから`feature/test`というブランチを作成
```bash
> git checkout main
> git branch -c feature/test
```

### Sourcetree

## 3. プログラム開発
---
プログラムソースの作成・編集

## 4. ステージング
---
### コマンド
```bash
## 特定のファイルをステージング
> git add {ファイル名}

## 変更のあったすべてのファイルをステージング
> git add .
```

### Sourcetree

## 5. コミット
---

### コマンド
```bash
> git commit -m "コミットメッセージ"
```

### Sourcetree

## 6. リモートに変更を反映
---
### コマンド
```bash
> git push origin {ブランチ名}
```

### Sourcetree

## 7. プルリクエストを作成
[プルリクエストの作り方](index.md)

## 8. プルリクエストのマージ
承認されたのち、変更をマージ（画面から）



| Column1 | Column2         |
| ------- | --------------- |
| Row1    | ```bash<br/>``` |
| Row2    |                 |
