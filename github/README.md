# email

## Keep my email addresses private を有効化

GitHub アカウントに登録されているメールアドレスが非公開になる

## noreplyアドレスの設定方法

1. git config --global --list で確認

2. あればリセット

git config --global --unset user.email

3. noreplyのメールアドレスを設定します。

git config --global --add user.email ID+名前@users.noreply.github.com