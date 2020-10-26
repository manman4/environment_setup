# Mac

## Windows からMac に変えたら動作が重くなった

## Gitで大量のパーミッション差分が出た時の対応

参考：https://belltree.life/git-file-system/

1. 設定変更

Windows　Git Bash で　Mac はターミナルで

git config core.filemode false

2. 確認

git config --list | grep core.filemode