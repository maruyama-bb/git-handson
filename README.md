【基本コマンド】
git init
git clone
git add    …commit準備状態
git commit　…リモート反映
git fetch ...リモートから履歴を取得（ブランチは変わらない。）
git pull ... リモートから履歴取得、ブランチ変わる。マージしたりする必要
git merge ... マージ。。。新しいコミットが可能
git pull -rebase リモートブランチの後ろにローカルの履歴を追加する
git rebase master .. ローカルブランチの後ろにリモートブランチを追加