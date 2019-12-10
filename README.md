# git-hello-world

gitはバージョン管理ツールですよ😃

## git
- `init`
    - ディレクトリをgitでバージョン管理したいときに一番最初に使う
    - ディレクトリの中に.gitを作る  
    - .gitを使ってバージョン管理をしている
- `clone`
    - リモートリポジトリからとってくる
- `status`
    - modified / untracked / deleted などの状態がわかる
    - staged file / unstaged file がわかる
- `log`
    - ログが見れる
- `add`
    - Staging area に追加する
    - `git add -A, --all`
        - 全部をアドする
- `commit`
    - Staging area にあるのをHistoryにコミットする
    - `git commit -m`
        - コミット際にメッセージを付ける
- `reset`  

| モード | mixed | soft | hard |
| ---- | ---- | ----|---- |
| ワーキングディレクトリ | 変更したまま | 変更したまま | 変更していない状態に戻る |
| ステージングエリア | 捨てる | 捨ててない | 捨てる |

- `branch`
    - `git branch`
        - 自体は、どのブランチにいるかを確認する
    - `git branch ブランチ名`
        - ブランチを作る
    - `git branch -m 古いブランチ名 新ブランチ名`
        - ブランチ名をリネームする
    - `git branch -d ブランチ名`
        - ブランチを削除
            - `-D` にして強制的に削除(マージしていないコミットがあるとき)
- `checkout`
    - `git checkout ファイル名`
        - ファイルの内容を元に戻す
    - `git checkout ブランチ名`
        - ブランチを切り替える
- `merge`
    - 合併する
    - マージの順番が変わる
        - master 1 / 2 / 3 / 4
        - trainer 1 / 2 / 3 / 4 / d / p
        - pokemon 1 / 2 / 3 / 4 / x / y
        - `git checkout trainer; git merge pokemon`
            - trainer 1 / 2 / 3 / 4 / d / p / x / y
        - `git checkout pokemon; git merge trainer`
            - pokemon 1 / 2 / 3 / 4 / x / y / d / p
- `push`
    - プッシュする
    - リモートにuploadする
- `fetch`
    - リモートからダウンロードする
- `pull`
    - `git fetch; git merge`