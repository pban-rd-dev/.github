# P-BAN R&D Team

**P-ban.com（株式会社ピーバンドットコム）** の R&D チームです。東京・千代田区で、
プリント基板の設計・製造・実装をオンラインで扱っています。

ここには、自社のハードウェア開発から出てきたファームウェアとツールを置いています。

## お知らせ

技術者向けの更新情報です。

- **2026-08-27** — [solist_ai_iap_firmware](https://github.com/pban-rd-dev/solist_ai_iap_firmware)
  に J-Link 経由の書き込みを追加しました。Linux / macOS / Windows 対応。ベンダ提供の
  フラッシュアルゴリズムをターゲット RAM 上で走らせるので、OpenOCD 経路よりかなり速く
  書けます。
- **2026-06-05** — solist_ai_iap_firmware を公開しました。
- **近日** — gene + Solist-AI 開発キットのファームウェアを公開します。

## gene — センサ PoC のセミカスタム開発

[**gene**](https://www.p-ban.com/services/gene/) は、評価ボードではなく「動くデモ機」が
必要なときのための開発サービスです。gene Core（40 × 40 × 20 mm、ESP32-S3 または
STM32F446）にセンサモジュールを組み合わせ、回路・基板・実装・ファームウェア・データを
見るための PC アプリまでまとめて用意します。

共通プラットフォーム 7 割 + カスタム 3 割くらいの作りにしてあるので、PoC のために
フルスクラッチの開発案件を立てなくて済みます。

## gene + Solist-AI 開発キット

ROHM のオンデバイス AI ソリューション
[**Solist-AI™**](https://www.rohm.co.jp/support/solist-ai) のエコシステムパートナーとして、
Solist-AI マイコンを載せた gene モジュールを開発しました。推論はデバイス上で完結します。

ノーコードで組込み AI を試せる **gene + Solist-AI 開発キット** を販売中です。ROHM 主催の
エッジ AI 開発コンテスト [ROHM EDGE HACK CHALLENGE 2026](https://rehc.jp/) では、
選考通過者に提供されるキットにもなっています。

## 公開しているもの

### [solist_ai_iap_firmware](https://github.com/pban-rd-dev/solist_ai_iap_firmware)

開発キットの Solist-AI モジュール（ROHM/LAPIS ML63Q2537、Cortex-M0+）にプリインストール
されている IAP（In-Application Programming）ファームウェアです。内蔵フラッシュ上部 32 KB
に書き込まれていて、起動すると UART を立ち上げ、XMODEM-CRC でユーザファームウェアを
受け取り、アプリ領域に書き込んで REMAP + リセットで起動します。

**デバッグプローブなしで、シリアルケーブルだけでファームウェアを差し替えられる**のがこの
仕組みの狙いです。IAP 自体を工場で書き込むための J-Link / OpenOCD ツールも同梱しています。

---

### English

We are the R&D team at **P-ban.com** (株式会社ピーバンドットコム), a PCB design,
fabrication and assembly business in Tokyo. We publish firmware and tooling from our
own hardware work here — currently
[solist_ai_iap_firmware](https://github.com/pban-rd-dev/solist_ai_iap_firmware), the
IAP firmware pre-installed on the Solist-AI module of our **gene + Solist-AI
development kit**, which lets kit owners flash their own application firmware over a
serial cable with no debug probe. The kit's application firmware follows soon.
