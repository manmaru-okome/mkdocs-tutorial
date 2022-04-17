# コンフリクトの対処法

## そもそもコンフリクトとは？

## 想定ケース
`main`ブランチに`feature/conflict-test`ブランチをマージさせようとしている場合

###  1. `feature/conflict-test`に`main`をマージさせる

```bash
> git checkout main
> git pull origin main
> git chckout feature/conflict-test
> git merge main
(コンフリクト発生中)
```

### 2. コンフリクトを解消

TODO: 画像用意する

### 3. `feature/conflict-test`をリモートにpush
```bash
> git push origin feature/conflict-test
```