# Mac

## Windows からMac に変えたら動作が重くなった

## Gitで大量のパーミッション差分が出た時の対応

参考：https://belltree.life/git-file-system/

1. 設定変更

Windows　Git Bash で　Mac はターミナルで

git config core.filemode false

2. 確認

git config --list | grep core.filemode


## GitHub等のパスワードを変更したとき

キーチェーンアクセスを開きSourtreeで検索し対象のアカウントを削除

pushのときにパスワードを入れる

## SSH

2021年○月からパスワードがダメなので

https://qiita.com/ozkknnt/items/054746c687936200a281

を参考にSSH