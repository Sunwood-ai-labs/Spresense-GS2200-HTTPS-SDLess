<div align="center">

# Spresense-GS2200-HTTPS-SDLess

[![Lab](https://img.shields.io/badge/Lab-Sunwood%20AI%20Labs-orange?style=flat-square)](https://github.com/Sunwood-ai-labs)
![Language](https://img.shields.io/badge/Language-C%2B%2B-00599C?style=flat-square&logo=c%2B%2B)
![Framework](https://img.shields.io/badge/Framework-Arduino-00979D?style=flat-square&logo=arduino)
![Hardware](https://img.shields.io/badge/Hardware-Sony%20Spresense-000000?style=flat-square)
![WiFi](https://img.shields.io/badge/WiFi-GainSpan%20GS2200-blue?style=flat-square)
![Protocol](https://img.shields.io/badge/Protocol-HTTPS%20%2F%20TLS%201.2-green?style=flat-square)
![License](https://img.shields.io/badge/License-LGPL%202.1-blue.svg?style=flat-square)

![header](header.jpg)

</div>

Sony Spresense と GainSpan GS2200 WiFi モジュールを使用した HTTPS クライアントの実装例です。SD カードを使用せずに証明書をロードし、HTTPS (TLS 1.2) 通信を実現します。

## 特徴
- **SD カード不要**: ルート証明書をメモリ (Flash) から直接ロード。
- **TLS 1.2 対応**: GS2200 のハードウェア TLS アクセラレーションを活用。
- **安定した接続管理**: 起動時に既存の証明書をクリーンアップ (`AT+TCERTDEL`) し、重複エラーを回避。

## 動作環境
- [Sony Spresense](https://developer.sony.com/develop/spresense/)
- [GainSpan GS2200-WiFi Shield](https://www.telit.com/products/wifi-and-bluetooth/gs2200m/)

## セットアップ

1. 本リポジトリをクローンします。
2. `config.example.h` を `config.h` にリネームします。
3. `config.h` 内の `AP_SSID` と `PASSPHRASE` をお使いの環境に合わせて書き換えます。
4. Arduino IDE で `HTTPSecureClient_TEST.ino` を開き、Spresense に書き込みます。

## ライブラリ
以下のライブラリが必要です。
- [GS2200-WiFi](https://github.com/sonydevworld/spresense-arduino-compatible/tree/master/examples/GS2200-WiFi)

## ライセンス
LGPL 2.1
