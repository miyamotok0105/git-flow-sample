# git-flow-sample

## 環境構築

mac

```
brew install git-flow
```

ubuntu

```
sudo apt-get install git-flow
```

centos


```
yum install git-flow
```


## 初期化

```
git flow init
```


```
* develop
  master
```


```
git push origin develop
```

## 新機能追加:feature

topという名前でブランチを切る。


```
git flow feature start top
```

```
  develop
* feature/top
  master
```

```
git flow feature publish top
```

github側でプルリクを作ってマージしておく。    


```
git checkout develop
git pull origin develop
```

# githubの運用について


ブランチの計画はgit-flowを使用する。    
コミットのメッセージはライト版を使用。    
Pull requestとIssueのフォーマット。    

### コミットのテンプレート

ライト版を使用。

```
fix：バグ修正
add：新規（ファイル）機能追加
update：機能修正（バグではない）
remove：削除（ファイル）
```

例

```
[fix]削除フラグが更新されない不具合の修正
or
[add]削除フラグが更新されない不具合の修正
```


### Pull request テンプレート

```
<!-- あくまでテンプレートなので必ずしもすべての項目を埋めなくてよい -->

# 概要
<!-- 変更の目的 もしくは 関連する Issue 番号 -->

# 変更内容
<!-- ビューの変更がある場合はスクショによる比較などがあるとわかりやすい -->

# 影響範囲
<!-- この関数を変更したのでこの機能にも影響がある、など -->

# 動作要件
<!-- 動作に必要な 環境変数 / 依存関係 / DBの更新 など -->

# 補足
<!-- レビューをする際に見てほしい点、ローカル環境で試す際の注意点、など -->
```


### Issue テンプレート

```
<!-- あくまでテンプレートなので必ずしもすべての項目を埋めなくてよい -->

<!-- 要望のテンプレート -->
# 概要
# 目的
# 提案内容
# タスク
- [ ] 細かいタスクに分解できているなら書き出す

<!-- 不具合のテンプレート -->
# 概要
# 再現手順
# 修正しないとどう困るか
# 原因
# 修正案
```



# 参考


https://blog.hotolab.net/entry/github_template
https://qiita.com/KosukeSone/items/514dd24828b485c69a05

https://qiita.com/azusanakano/items/c5f021497d8f69c00e51
https://qiita.com/KosukeSone/items/514dd24828b485c69a05
