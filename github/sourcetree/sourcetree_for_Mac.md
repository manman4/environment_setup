# Sourcetree for Mac

## Windows からMac に変えたら動作が重くなった

## Gitで大量のパーミッション差分が出た時の対応

参考：https://belltree.life/git-file-system/

1. 設定変更 (重要　Windows、Mac両方作業必要)

Windows　Git Bash で　Mac はターミナルで

```bash
git config core.filemode false
```

2. 確認

```bash
git config --list | grep core.filemode
```

※ 上記方法よりも、

ソースコードに全てファイルやモデルを上げていて、gitignoreされているものがないなら、

一からgithubを引っ張ってくる方が楽かもしれない

## Githubで'Untracked files'がどうにも消えない時の対応

https://qiita.com/nobucook/items/b83464e50c1b27255317

1. git clean -dfn　→　git clean -dfしたときの未追跡の変更差分（Untracked files）がどうなるかの確認。

2. git clean -df

注意　.gitを含まない場所で行う。また、余分に増えた場合も、誤った削除と認識したときも、消されるので、必ず前者のみのファイルしかないことを確認

## GitHub等のパスワードを変更したとき

キーチェーンアクセスを開きSourtreeで検索し対象のアカウントを削除

pushのときにパスワードを入れる

## gitignoreについて

Global がデフォルトだが、このレポジトリのみの方が無難

もし、間違ってGlobalで無視してしまった場合

```
.gitignore_global
```

を編集する

## SSH

今後を考えると、SourcetreeもパスワードでなくSSHで接続すべき

1. Githubにkeyを登録

2. BitbucketにSSH鍵を登録する　https://qiita.com/YoshiISHIGAMI/items/b7d045710d8319f1a3e4

Terminalを開いて以下のコマンドを叩く

```bash
pbcopy < ~/.ssh/id_rsa.pub
```

セキュリティ > SSH鍵 をクリックしページに移動し、ページにある「SSH 鍵を追加」をクリックし、label とkeyを追加

3. Repogitry　https://tks2.co.jp/2021/01/18/github-ssh/

Sourcetreeの設定の高度な設定のConfigファイルを編集を押下

url がSSHになっていなかったら、githubのRepogitryのSSHに変えておく。

(上記はSourcetree上で行う場合だが、.gitフォルダ内のconfigのurlをかえる方がはやいかも... 同時にpushurlを追加する必要があるかも)

4. その他

Sourcetreeの設定からSSHでないリポジトリをSSHに変更できる。

元々アカウントでSSHがうまくいっていなかったら、上記を行ってもpushできない。

（例えばアカウントで公開キーのアップロードの失敗等続くとき、）最終手段として、Sourcetreeをインストールしなおしてから、リポジトリをSSHに変更してみる。

23/7/12

https://qiita.com/unsoluble_sugar/items/14bea376d8e6fce82eb3
