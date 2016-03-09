# 大野が記載
## WinMergeがうまく設定できてないかも

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


=================
1. 講義で習ったcommand集

 - touch .gitconfig			.gitconfigの作成
 - git init					リポジトリの作成（リポジトリを作成するディレクトリで実行）
 - git clone [URL]			リポジトリの複製（リポジトリを作成するディレクトリで実行）
 - git status				ステータスの確認
 
 - git add [ファイル名]		コミットファイルの追加
 - git commit				変更をコミット
 - get fetch				リモートのコピーをローカルにダウンロード
 - git merge [branch]		今いるブランチに別のブランチの内容を結合させる
 							リモートリポジトリにあるブランチや、ローカルの別のブランチをマージするときに使用
 							
 - gitk -all &				ツリーを表示させる
 - git checkout [branch]	ブランチ名を指定してブランチを切替え
 - git rebase [branch]		mergeと同じく今いるブランチに別のブランチの内容を取り込むコマンド

 - git pull					git fetch と git merge を同時に実行するコマンド
 - git pull --rebase		git fetch と git rebase を同時に実行するコマンド
 
 master						ローカルの今いるところ
 origin/master				リモートの今いるところ
 

2. Reference

get pullとget pull -rebaseの違い
http://kray.jp/blog/git-pull-rebase/

 - git checkout [branch元] 	rebase元にチェックアウト
 - git rebase [branch先]	リベースする

=================


# git-svnについて
* SubversionのリポジトリをGitクライアントで操作する
* SVNからGitに移行する場合は、```git-svn```でGitの操作に慣れてもらってからリモートリポジトリを切り替える
## git-svnに関するリンク
* [git-scm.com](https://git-scm.com/book/ja/v1/Git%E3%81%A8%E3%81%9D%E3%81%AE%E4%BB%96%E3%81%AE%E3%82%B7%E3%82%B9%E3%83%86%E3%83%A0%E3%81%AE%E9%80%A3%E6%90%BA-Git-%E3%81%A8-Subversion)
* [Atlassian](https://www.atlassian.com/ja/git/migration)

＝＝＝＝＝＝＝＝＝＝＝＝
マージできるかテストマージ
＝＝＝＝＝＝＝＝＝

#プロキシ環境下での設定について(参考HP)
http://sushichop.blogspot.jp/2013/09/git.html

