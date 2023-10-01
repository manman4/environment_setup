# email

## Keep my email addresses private を有効化

GitHub アカウントに登録されているメールアドレスが非公開になる

## noreplyアドレスの設定方法

1. git config --global --list で確認

2. あればリセット

　　git config --global --unset user.email

3. noreplyのメールアドレスを設定します。

　　git config --global --add user.email ID+名前@users.noreply.github.com

# masterからmainへ変更

1. ローカルブランチを改名

　　git branch -m master main

2. 改名後のブランチをpush

　　git push -u origin main

3. GitHubで既定のブランチを変更

　　リポジトリのSettings→左メニューBranches→Default branch

　　masterとなっているところをmainに変更して、Updateを押す

4. masterブランチの削除

　　git push origin :master


# リポジトリ名変更

1. GitHub側

　　GitHubの対象リポジトリ > Setting > Renameで変更

2. ローカル側の操作

　　ローカルリポジトリ名もRename
  
　　対象ディレクトリ内の .git > configを変更
  
# publicからprivateへ変更(逆も然り)

https://qiita.com/HyunwookPark/items/1d24972dd71612eb81c9

　1. 「Settings」でページの一番下「Danger Zone」から

# forkリポジトリ削除

1. Settings Options の一番下のDelete this repositoryから削除

# そもそもGithubの興味深い機能

## Clonerの数の確認

Insights -> Traffic -> Git clones





