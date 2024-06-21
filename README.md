<div id="top"></div>
# よくある質問ページプロジェクト

## 概要

このプロジェクトは、大阪府主催の公共職業訓練「Javaプログラマー養成科」の受講中に、Java、データベース、WEBアプリケーションの知識とスキルを活かして制作しました。企業実習として、株式会社ジョブリッジ様のために「よくある質問」ページを作成しました。このページは、訪問者が疑問を解決できるように、質問とその回答を提供することを目的としています。

## デモ

以下のリンクからデモ動画をご覧いただけます：
[![デモ動画](https://img.youtube.com/vi/TuKDqV9sB4I/0.jpg)](https://youtu.be/TuKDqV9sB4I)

## ファイル概要

- **データベースファイル**
  - `jobridge.mv.db`: H2データベースで使用するメインデータベースファイル。
  - `jobridge.trace.db`: H2データベースのトレースファイル。

- **エクスポートファイル**
  - `jobridge.zip`: Eclipseで作成し、エクスポートしたプロジェクトファイルのZIPアーカイブ。

- **遷移図**
  - `遷移図.drawio`: システムの画面遷移を示すドローチャート。最初に作成したもののため、V2が最新です
  - `ジョブリッジQA遷移図V2-詳細.jpg`: ページ間の詳細な遷移図の画像ファイル。
  - `ジョブリッジQA遷移図V2.jpg`: 簡略化された遷移図の画像ファイル。

- **その他**
  - `企業実習企画書兼タイムラインURL.txt`: 制作の経過とタイムラインを記録したテキストファイル。
 
## ディレクトリ構造
```
/Jobridge
├── src/main/java
│   ├── dao
│   │   └── QAListDAO.java
│   ├── model
│   │   ├── Answers.java
│   │   ├── QA.java
│   │   └── QACategory.java
│   └── servlet
│       └── SearchServlet.java
├── src/main/webapp
│   ├── CSS
│   │   └── style.css
│   ├── img
│   │   ├── フッターイメージ画像.png
│   │   └── ヘッダーイメージ画像.png
│   ├── META-INF
│   │   └── MANIFEST.MF
│   ├── WEB-INF
│   │   └── lib
│   │       ├── h2-2.2.224.jar
│   │       ├── jstl-api-1.2.jar
│   │       └── jstl-impl-1.2.jar
│   ├── noResult.jsp
│   └── qaList.jsp
└── build
```


## インストールと使い方

### サーブレットの実行手順

1. **プロジェクトのビルド**

   - Javaで構築されています。まず、Eclipseでプロジェクトを開きます。

2. **依存ライブラリの設定**

   - `src/main/webapp/WEB-INF/lib` ディレクトリに以下の依存ライブラリが必要です：
     - `h2-2.2.224.jar`
     - `jstl-api-1.2.jar`
     - `jstl-impl-1.2.jar`

   - プロジェクトのビルドパスにこれらのJARファイルを追加してください。

3. **サーブレットの設定**

   - `SearchServlet.java` は `src/main/java/servlet` ディレクトリにあります。

4. **サーバーでの実行**

   - サーブレットコンテナ（例：Tomcat）にWARファイルをデプロイし、サーバーを起動します。
   - サーブレットへのアクセスURLは、例えば `http://localhost:8080/Jobridge/SearchServlet` のようになります（ポート番号やパスは環境により異なります）。

5. **動作確認**

   - ブラウザでアクセスして、検索機能が正常に動作することを確認してください。

## その他のファイル

- `noResult.jsp`: 検索結果がない場合に表示するページ。
- `qaList.jsp`: QAリストを表示するページ。

<p align="right">(<a href="#top">トップへ</a>)</p>




