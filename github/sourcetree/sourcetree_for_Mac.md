# Mac

## Windows からMac に変えたら動作が重くなった

## Gitで大量のパーミッション差分が出た時の対応

参考：https://belltree.life/git-file-system/

1. 設定変更 (重要　Windows、Mac両方作業必要)

Windows　Git Bash で　Mac はターミナルで

git config core.filemode false

2. 確認

git config --list | grep core.filemode

※ 上記方法よりも、

ソースコードに全てファイルやモデルを上げていて、gitignoreされているものがないなら、

一からgithubを引っ張ってくる方が楽かもしれない

## GitHub等のパスワードを変更したとき

キーチェーンアクセスを開きSourtreeで検索し対象のアカウントを削除

pushのときにパスワードを入れる

## gitignoreについて

Global がデフォルトだが、このレポジトリのみの方が無難

もし、間違ってGlobalで無視してしまった場合

.gitignore_global

を編集する

## SSH

今後を考えると、SourcetreeもパスワードでなくSSHで接続すべき

1. Githubにkeyを登録

2. BitbucketにSSH鍵を登録する　https://qiita.com/YoshiISHIGAMI/items/b7d045710d8319f1a3e4

Terminalを開いて以下のコマンドを叩く

pbcopy < ~/.ssh/id_rsa.pub

セキュリティ > SSH鍵 をクリックしページに移動し、ページにある「SSH 鍵を追加」をクリックし、label とkeyを追加
