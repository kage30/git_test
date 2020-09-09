# git_test

### 基本的なコマンド
pwd : どこにいるかパスの確認
cd パス : パスのとこに移動
mkdir : ディレクトリの作成


### 基本のgitコマンド
  git --version : gitのバージョン確認
  git --help : 分からなかったらとりあえずこれ

  #### 設定
  - git config —global user.name "name"
  - git config —global user.email email

  #### 確認
  - git status : ファイルの状態確認。
  <br/>
  - git diff : ワークツリーとインデックスのソースの差分確認
    - --name-onlyをつけるとファイル名のみ ≒ git status
  <br/>
  - git log : コミット履歴の確認
    - git log -数字　直近の数字分のコミット
    - --statをつけると変更ファイルも表示される


  #### ブランチ操作
  - git branch <ブランチ名> : ブランチの作成
    - git branch だけだとローカルブランチの確認
  <br/>

  - git checkout <ブランチ名> : ブランチの移動
    - git checkout -b <ブランチ名> : ブランチの作成と移動が同時にされる
    - git checkout -d <ブランチ名> : マージ済みのブランチを削除
  <br/>

  - git add ファイル名 : ワークツリーのファイルをステージングに登録
    - .だと全部のファイル
  <br/>

  - git commit -m "commit comment" : コメント付けてコミット
    - git commit -m "commit comment" -m "commit comment" : つなげて書くと複数行かける
    - git commit -F- <<EOM : これも複数行。↓みたいに書く(>も含む)
      > 要約
      >
      > 詳細
      > 
      > EOM

  - git push origin <ブランチ名> : リモートのブランチにプッシュ

  - git fetch : リモートの最新をローカルに取ってくる。(ワークツリーは変わらない)
  <br/>

  - git pull : リモートの最新をローカルに取ってくる。(ワークツリーまで)
  <br/>

  - git merge <ブランチ名> : 今いるブランチに指定したブランチを統合する。