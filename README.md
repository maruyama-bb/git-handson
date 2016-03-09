# 大野が記載
## WinMergeがうまく設定できてないかも
更に追加(大野)
16:01追加（大野）

edit...
git add home.md
git commit
git fetch
git merge
git push


gitk -all

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

branch
checkout
(変更）


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

# git-svnについて
* SubversionのリポジトリをGitクライアントで操作する
* SVNからGitに移行する場合は、```git-svn```でGitの操作に慣れてもらってからリモートリポジトリを切り替える

## git-svnに関するリンク
* [git-scm.com](https://git-scm.com/book/ja/v1/Git%E3%81%A8%E3%81%9D%E3%81%AE%E4%BB%96%E3%81%AE%E3%82%B7%E3%82%B9%E3%83%86%E3%83%A0%E3%81%AE%E9%80%A3%E6%90%BA-Git-%E3%81%A8-Subversion)
* [Atlassian](https://www.atlassian.com/ja/git/migration)
* [Git-Subversion比較](http://www.backlog.jp/git-guide/reference/git-svn.html)
* [面倒くさいsvnリポジトリをgit-svnで扱う時に役立ちそうなオプション一覧](http://sinsoku.hatenablog.com/entry/2014/02/26/231918)
* [仕事で使ってる巨大SVNレポジトリをGithubに移管するためにやったことまとめ](http://dqn.sakusakutto.jp/2012/10/svn-git-github-migration.html)

#プロキシ環境下での設定について(参考HP)
http://sushichop.blogspot.jp/2013/09/git.html
http://www.backlog.jp/git-guide/reference/config.html


