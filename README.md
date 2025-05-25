# ここにCDK環境を作る。
## cdkのインストール
- npm install aws-cdk
- npm install typescript ts-node
- mkdir (プロジェクト名ディレクトリ) & ディレクトリに移動
- npx cdk init app --language typescript

## cfn-lint のインストール
- python -m venv .venv
- . .venv/bin/activate
- pip install cfn-lint

# 出力先ディレクトリの作成
- .clinerules/02-StandardRules.md に出力先ディレクトリを指定する

# 使用ツール
- cdk コマンドを使用するときは、`npx cdk`のように、コマンドの前に`npx`を付ける、ことをprojectBrief.md ファイルに書く
- cfn-lint コマンドは、`.venv/bin/cfn-lint`に保存してある、ことをprojectBrief.md ファイルに書く
  または「cfn-lint は venvを使用した仮想環境内にあります。`. .venv/bin/activate` を実行して仮想環境に入ってから cfn-lint を使用してください」

# cline セットアップ
1. .clinerules/01-memory-bank.mdファイルを作り、[Cline Memory Bank](https://docs.cline.bot/prompting/cline-memory-bank)の「Cline Memory Bank Custom Instructions COPY THIS」をコピペする
   ※cline下部アイコンの「Rules ＞ Workspace Rules」から「01-memory-bank.md」ファイルを作る
2. .clinerules/02-StandardRules.md ファイルを作り、その他規約などを書く（↓にサンプル。いろいろ追記して成長させていく）
3. cline_docsディレクトリを作り、中に「projectBrief.md」ファイルを作る
   →[Our Favorite Tech Stack](https://docs.cline.bot/getting-started/our-favorite-tech-stack)にある「Example Project Brief」をコピペして、プロジェクト要件を書く
4. clineに「initialize memory bank」と伝え、メモリバンクをセットアップしてもらう
5. clineに「follow your custom instructions」と伝える→clineが計画を立て始める
6. セッションを切り替えるときは「update memory bank」と伝えてMemoryBankを更新
7. 新しいセッションで「follow your custom instructions」と伝えてMemoryBankから読み取らせる

