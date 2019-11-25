# ドメインを独立させる Isolating the Domain
- Spring Boot
- Spring MVC (direct field access)
- Thymeleaf
- MyBatis SQL Mapper

## 起動方法

```sh
./gradlew bootRun
```
memo
http://localhost:8080 でダッシュボード画面を表示

## 実行可能Jarのビルドと実行

```sh
./gradlew :webapp:clean :webapp:build
java -jar webapp/build/libs/webapp.jar
```

## Jig 設計ドキュメントの自動生成

```sh
./gradlew :webapp:jig
```

`webapp/build/jig` 以下にソースコードから自動生成したクラス一覧やクラスの関連図を出力

[Jig 設計ドキュメント](https://github.com/dddjava/Jig)

## 設計ガイド

[ドメインを独立させる](https://github.com/system-sekkei/isolating-the-domain/wiki)

[ドメイン駆動設計本格入門](https://www.slideshare.net/masuda220/ss-137608652)

[型指向のプログラミング：設計ガイドライン](https://github.com/masuda220/business-logic-patterns/wiki/%E8%A8%AD%E8%A8%88%E3%82%AC%E3%82%A4%E3%83%89%E3%83%A9%E3%82%A4%E3%83%B3)

[書籍：現場で役立つシステム設計の原則](https://gihyo.jp/book/2017/978-4-7741-9087-7)

## アーキテクチャ

![アーキテクチャ](architecture.png)

## 動作検証

```sh
npm install
npm test
```

Cypressのヘッドレスブラウザで疎通を実施
