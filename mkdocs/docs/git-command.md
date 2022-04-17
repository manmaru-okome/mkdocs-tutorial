# gitの基本コマンド

## clone
リポジトリを複製する

```bash
> git clone {リポジトリのURL}
```

## add
ローカルリポジトリに変更を記録するファイルを選択する
```bash
# 特定のファイルをステージング
> git add {ファイル名}

# 変更のあったすべてのファイルをステージング
> git add .
```

## status
ステージングされたファイルの一覧を表示する。
```bash
> git status
```

## commit
変更をローカルリポジトリに記録する
```bash
> git commit -m "コミットメッセージ"
```

## push
ローカルリポジトリの内容をリモートリポジトリに反映させる
```bash
> git push origin {ブランチ名}

# mainからorigin/mainにpushの場合
> git push origin main
```

## fetch
追跡ブランチにリモートの状態を反映させる

```bash
# リモートのすべてのブランチの変更を検知
> git fetch

# 特定のブランチの変更を検知
> git fetch origin {ブランチ名}
```

## pull
```bash
# pullするブランチに移動して取り込み
> git checkout {ブランチ名}
> git pull origin {ブランチ名}
```

## mv
ファイルを移動する。ファイル名を変更するときもこれ。
このコマンドでファイルの操作を行わないと、git上では変更後で新規ファイルとして認識され、これまで記録していた変更履歴がなくなってしまう。
```bash
> git mv {変更前のファイル名} {変更後のファイル名}
```
`test.md`というファイルを`docs`フォルダに移動する場合
```bash
# 
> git mv test.md docs/test.md
```
`test.md`というファイルの名前を`testest.md`に変更する場合
```bash
> git mv test.md testtest.md
```

## remote
リモートリポジトリの情報を確認
```bash
> git remote -v
origin  https://github~~ (fetch)
origin  https://github~~ (push)
```

リモートリポジトリの変更。tokenの有効期限が切れたときなどに使用する。
```bash
> git remote set-url origin {変更後のURL}
```

## checkout
```bash
> git checkout {ブランチ名}
```

## merge
```bash
> git merge {ブランチ名}
```

