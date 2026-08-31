<h1 align="center">P-ban.com R&D Team</h1>

<p align="center">
  <a href="https://www.p-ban.com/">株式会社ピーバンドットコム（p-ban.com Corp.）</a>
</p>

---

## 会社について

プリント基板ネット通販サイト「P板.com（ピーバンドットコム）」の運営を中心に、
設計・製造・部品実装までをインターネット上でワンストップ提供するサービスを展開しています。

https://www.p-ban.com/

## R&D チーム

P板.com の自社サービス向け技術開発を担当するチームです。
回路・基板設計からファームウェア、PC アプリケーション、組み込み AI まで、
ハードウェアとソフトウェアの両面を一貫して開発しています。

この GitHub アカウントでは、開発した成果物の一部を一般公開・配布しています。

## 活動内容

開発しているのは次の 2 つです。

- **gene** — センサー PoC 向けのセミカスタム開発 **サービス**
- **gene + Solist-AI™ 開発キット** — gene をベースにキット化した **製品**

---

### gene（サービス）

<p align="center">
  <a href="https://www.p-ban.com/services/gene/"><img src="https://www.p-ban.com/services/gene/images/logo.png" width="160" alt="gene"></a>
</p>

> そのセンサ、geneが動かす。

<p align="center">
  <img src="https://www.p-ban.com/services/gene/images/hand_gene2.webp" width="230" alt="手のひらの上に浮かぶ gene Core">
</p>

回路図と BOM（部品表）をお預かりし、基板設計・製造からファームウェア・PC アプリまでをワンストップで仕上げる、センサー PoC 特化のセミカスタム開発サービスです。

[センサPoCのセミカスタム開発サービス gene | P板.com](https://www.p-ban.com/services/gene/)

---

### gene + Solist-AI™ 開発キット（製品）

> 箱を開けたら、その日からAIを試せる。
>
> ファームウェア実装もモデル変換も専任エンジニアも不要。必要なのは、データとアイデアだけ。

<p align="center">
  <img src="https://www.p-ban.com/services/gene/images/concept231.webp" width="280" alt="Solist-AI × gene 開発キット">
</p>

gene のハードウェアをベースに、ROHM Solist-AI™ を搭載してキット化した製品です。
コードを書かずに、IC 上で「学習→推論」まで実行可能です。

[Solist-AI™ × gene｜ノーコード組み込みAI開発キット | P板.com](https://www.p-ban.com/services/gene/solist-ai.html)

#### この開発キット向けの公開リポジトリ

キットに搭載されているファームウェアを、以下のリポジトリで公開しています。

| リポジトリ | 内容 | 提供形態 |
| --- | --- | --- |
| [gene_firmware_for_solist_ai_dev_kit](https://github.com/pban-rd-dev/gene_firmware_for_solist_ai_dev_kit) | gene Core（ESP32-S3）側の gene firmware | プリコンパイル済みライブラリ + hook API の SDK |
| [solist_ai_module_firmware](https://github.com/pban-rd-dev/solist_ai_module_firmware) | Solist-AI モジュール（ML63Q2537）ファームウェア | バイナリ（Releases） |
| [solist_ai_iap_firmware](https://github.com/pban-rd-dev/solist_ai_iap_firmware) | Solist-AI モジュール IAP ファームウェア | ソース |
