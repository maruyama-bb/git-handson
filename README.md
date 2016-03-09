edit...
git add home.md
git commit
git fetch
git merge
git push


gitk -all
=======
# Gitまめちしき h1

# 基本コマンド
* git init
* git clone
* git add    …commit準備状態
* git commit　…リモート反映
* git fetch ...リモートから履歴を取得（ブランチは変わらない。）
* git pull ... リモートから履歴取得、ブランチ変わる。マージしたりする必要
* git merge ... マージ。
* git pull -rebase リモートブランチの後ろにローカルの履歴を追加する
* git rebase master .. ローカルブランチの後ろにリモートブランチを追加

# 講義で習ったコマンド

# .gitconfigの作成
 touch .gitconfig

# リポジトリの作成
 git init
 ただし、リポジトリを作成するディレクトリで実行する

# リポジトリの複製
 git clone [複製したいリポジトリのURL]
 ただし、リポジトリを作成するディレクトリで実行する

# ステータスの確認
 git status

# コミットファイルの追加
 git add [ファイル名]

# 変更をコミット
 git commit

＝＝＝＝＝＝＝＝＝＝＝＝
マージできるかテストマージ
＝＝＝＝＝＝＝＝＝