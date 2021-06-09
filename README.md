## laradock-v3リポジトリの位置づけ

- PHPプロジェクトの単体環境構築用に使用するlaradockの設定管理
- v3はdocker-compose.ymlのバージョンに因んで命名
  - galette用のlaradockリポジトリが既にあったが、v2であり一緒に管理することが難しかった

## 使い方

- 【project/プロジェクト名】ブランチをプルし、そのまま下記コマンドを実行する
  - ```docker-compose up -d nginx mysql redis```
  - プロジェクトによりポートを変えていたりするので、.envの設定内容は要確認
- プロジェクトのソースコードの置き場所
  - laradockディレクトリと同階層に置く
  - 例
    ```
    mydir
    ├──laradock
    └──projectdir
        ├─app
        │ ├─Config
        │ ├─Console
        │ (中略)
        ├─lib
    ```
