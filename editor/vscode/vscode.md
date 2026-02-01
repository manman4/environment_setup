# VSCode

## 便利な拡張機能

- **改行**
  - code-eol

- **プログラミングフォント**
  - Ricty Diminished を設定のFont Familyに指定してやる
  - macの場合のフォントのダウンロードは例えば、以下を参照
    - https://hajipro.com/local-development-environment-mac/ricty-diminished

- **自動補完**
  - GitHub Copilot
  - 自動生成されたコードを選択したいときは Tab
  - pari/gpはサジェストしないので、プレインテキストを有効にしておく。

- **関数やクラスのコメントフォーマット作成**
  - autoDocstring
  - Pythonファイルでwクォーテーション３つでコメントフォーマット自動生成

- **Webサーバー**
  - live server

- **EJS**
  - EJS language support

- **Excel**
  - Excel Viewer

- **全角スペース検出**
  - zenkaku

## 便利な設定

```json
"editor.guides.bracketPairs": true
```

## vscode 立ち上げ

### Windows

おそらく何もしなくても code が使える

```bash
code *
```

### Mac

以下の設定が必要

1. Visual Studio Codeを起動
2. コマンドパレットを開く(cmd+shift+p)
3. "Shell Command: Install 'code' command in PATH"を選択

```bash
% code *
```

## terminal

### Mac

control + shift + `

## jupyter notebookを使う

拡張機能　Python for VSCode をインストール

コマンドパレットでjupyter: cretate new blank notebookで新規作成できる。（ググると、違うコマンドすぐにヒットする）
