# myst-packages
mystのパッケージリポジトリです。
パッケージを追加する際は以下の手順に従ってください。

## 追加手順
1. このリポジトリをクローンする `git clone https://github.com/nekogakure/myst-packages.git`
2. 別のとこで自分の作成したパッケージの名前のディレクトリを作成する。
3. 下記の形式でプロジェクトを作成（`myst init package`で簡単に作ってくれます）
```
json_parser-1.2.3/
├── mystia.lib.toml           # ライブラリ情報
├── src/                      # ソースコード
│   ├── **.ms
│   └── **.ms
├── docs/                     # ドキュメント
│   ├── README.md
│   └── API.md
├── examples/                 # 使用例
│   └── basic_usage.ms
└── tests/                    # テストファイル
    └── test_json_parser.ms
```
4. コードを書く
5. mystia.lib.tomlのあるディレクトリで`myst lib pack`
6. このリポジトリに生成されたtar.gzを配置するディレクトリを追加（~/パッケージ名/バージョン.tar.gz）
7. ~/パッケージ名/にlib.tomlを作成
8. [これ](example_lib.toml)を参考にして書く
9. このリポジトリにPRを送る。（下記の形式で）
   タイトル: [ADD] パッケージ名
   内容:     このパッケージでできることやまぁ、いいかんじにかいてください。
10. 承認されたらマージされます。

## アップデート手順
1. 更新する `git fetch`
2. アップデートしたいパッケージの名前のディレクトリに移動。
3. コードを書いて`myst lib pack`し、このリポジトリの~/パッケージ名/に配置。
4. lib.tomlのlatest_versionを最新のバージョンにし、version_indexに最新バージョンを追加。
5. このリポジトリにPRを送る。（下記の形式で）
   タイトル: [FIX] パッケージ名: バージョン
   内容:     更新したこのパッケージでできることやまぁ、いいかんじにかいてください。
6. 承認されたらマージされます。
