# 大野が記載
## WinMergeがうまく設定できてないかも
-更に追加(大野)
-16:01追加（大野） これを修正するぞ
-16:35追加

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
* git fetch ...リモートから履歴を取得
* git pull ... リモートから履歴取得
* git merge ... マージ
* git fetch ...リモートから履歴を取得（ブランチは変わらない。）
* git pull ... リモートから履歴取得、ブランチ変わる。マージしたりする必要
* git pull --rebase リモートブランチの後ろにローカルの履歴を追加する
* git merge ... マージ。
* git merge --ff-only ... ファストフォワードでマージする
* git merge --abort ... マージを取り消す
* git rebase master .. ローカルブランチの後ろにリモートブランチを追加
* git fsck ... リポジトリの正当性チェックを行う
* git gc ... リポジトリ内の不要なオブジェクトを削除し、最適化を行う
* git diff ... ファイルに加えられた変更点をdiff形式で表示する
* git log ... コミットログを閲覧する
* git reset ... 直前のコミットを取り消す
* git tag ... コミットにタグを付ける


branch
checkout
(変更）

==========================================================
1. 講義で習ったcommand集

 - touch .gitconfig			.gitconfigの作成
 - git init					リポジトリの作成（リポジトリを作成するディレクトリで実行）
 - git clone [URL]			リポジトリの複製（リポジトリを作成するディレクトリで実行）
 - git status				ステータスの確認
 
 - git add [ファイル名]		コミットファイルの追加
 - git commit				変更をコミット
 - git fetch				リモートのコピーをローカルにダウンロード
 - git merge [branch]		今いるブランチに別のブランチの内容を結合させる
 							リモートリポジトリにあるブランチや、ローカルの別のブランチをマージするときに使用
 - git push					リモートににローカルの内容を送信する
 							
 - gitk --all &				ツリーを表示させる
 - git checkout [branch]	ブランチ名を指定してブランチを切替え
 - git rebase [branch]		mergeと同じく今いるブランチに別のブランチの内容を取り込むコマンド

 - git pull					git fetch と git merge を同時に実行するコマンド
 - git pull --rebase		git fetch と git rebase を同時に実行するコマンド
 
 - git checkout [branch元] 	rebase元にチェックアウト
 - git rebase [branch先]	リベースする

 master						ローカルの今いるところ
 origin/master				リモートの今いるところ

2. Reference

 - git pullとgit pull -rebaseの違い
	http://kray.jp/blog/git-pull-rebase/
 - サブコマンド4選
 	http://qiita.com/cushy79/items/248659b5b814f1deceee
 - コマンドまとめ
 	http://qiita.com/tc_minami/items/70958bb1d19e0d1b5a10

==========================================================

* git fsck ... リポジトリの正当性チェックを行う
* git gc ... リポジトリ内の不要なオブジェクトを削除し、最適化を行う
* git diff ... ファイルに加えられた変更点をdiff形式で表示する
* git log ... コミットログを閲覧する


# git-svnについて
* SubversionのリポジトリをGitクライアントで操作する。
* SVNからGitに移行する場合は、```git-svn```でGitの操作に慣れてもらってからリモートリポジトリを切り替える

## Subversionに出来てGitにできない事
* ディレクトリを指定して```git clone```(```svn checkout```)することは出来ない

## git-svnに関するリンク
* [git-svn(1)のman page](https://www.kernel.org/pub/software/scm/git/docs/git-svn.html)
* [git-scm.com](https://git-scm.com/book/ja/v1/Git%E3%81%A8%E3%81%9D%E3%81%AE%E4%BB%96%E3%81%AE%E3%82%B7%E3%82%B9%E3%83%86%E3%83%A0%E3%81%AE%E9%80%A3%E6%90%BA-Git-%E3%81%A8-Subversion)
* [Atlassian](https://www.atlassian.com/ja/git/migration)
* [Git-Subversion比較](http://www.backlog.jp/git-guide/reference/git-svn.html)
* [面倒くさいsvnリポジトリをgit-svnで扱う時に役立ちそうなオプション一覧](http://sinsoku.hatenablog.com/entry/2014/02/26/231918)
* [仕事で使ってる巨大SVNレポジトリをGithubに移管するためにやったことまとめ](http://dqn.sakusakutto.jp/2012/10/svn-git-github-migration.html)
* [git-svnで始めるボッチのためのGit](https://speakerdeck.com/oohira/git-svnteshi-meruhotutifalsetamefalsegit)
* [svn リポジトリをローカルにコピーしてから git リポジトリに変換する](http://chocolapod.sakura.ne.jp/blog/entry/77)

#プロキシ環境下での設定について(参考HP)
* http://sushichop.blogspot.jp/2013/09/git.html
* http://www.backlog.jp/git-guide/reference/config.html

#よくあるシナリオと対処法
* コミット消えちゃった
 - コミットはそうそう消えない
 - 消えているように見えていても、そう見えてるだけで実際は消えていない。
 - reflogというコマンドでコミット見つけられる。headからの履歴を参照できる。
* コミットは細かいほうがよい。
 - stashコマンドはheadが動かないコミットより取り戻すのが面倒。
* いつまでたってもpushできない。コミットグラフがすごいことに
 - pushしたい場合はfetchしてマージコミットを作る（pullしない）
* push失敗時のマージコミットは１回のみなど
 - pull --rebaseの活用

# 変更をコミット
 git commit
 
# ブランチの切り替え
 git checkout
 
# ブランチの派生元を変更
 git rebase

# きょん氏について
* Twitter本人 <<https://twitter.com/kyon_mm?lang=ja>>
* Twitter奥様 <<https://twitter.com/kaori_t_spica>>
* ブログ <<http://kyon-mm.hatenablog.com/>>
* SlideShare <<http://www.slideshare.net/KyonMm/presentations>>

# Gitのコミットグラフをきれいに保つために
* 1つのファイルを同時に編集しないよう、適切に分割する
* ```git push```でrejectされた場合は```git pull --rebase```を使う
	* マージコミットを作らず、ローカルだけにあるコミットを```origin```の先頭に持って行く

#WinMerge関連のConfig設定
<http://ptech.g.hatena.ne.jp/noromanba/20120602/1338633091>
