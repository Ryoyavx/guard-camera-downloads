# Guard Camera

Android端末またはWindows PCを監視カメラとして使い、同じLANやTailscale内の登録済み端末から映像を視聴するアプリです。現在の公開版は0.2.0 Previewです。

## ダウンロード

- [Android 0.2.0 Preview APK](https://github.com/Ryoyavx/guard-camera-downloads/releases/download/v0.2.0-preview/GuardCamera-Android-0.2.0.apk)
- [Windows x64 0.2.0 Preview ZIP](https://github.com/Ryoyavx/guard-camera-downloads/releases/download/v0.2.0-preview/GuardCamera-Windows-v0.2.0-win-x64.zip)

Androidは8.0以降、Windowsはx64向けです。Windows版ZIPには自己完結型の実行ファイルとSTART_HERE.txtが入っています。.NETの別途インストールは不要です。

## できること

- Android: カメラ配信、録画、簡易検知、登録したAndroid/Windows端末の映像視聴、配信自己診断
- Windows: ブラウザでPCカメラを取得して配信、登録した複数端末の同時表示、オンライン表示
- 端末登録: 名前、LAN/Tailscale URL、視聴パスワードを手動入力

WindowsのPCカメラ配信には、実行ファイルとローカル管理画面のブラウザタブの両方を開いておく必要があります。

## 初回設定

1. 配信側で視聴パスワードを設定し、配信を開始します。
2. 視聴側で同じLANまたはTailscaleに接続し、配信側のURLとパスワードを登録します。
3. Androidでは「他端末の配信を見る」、Windowsではローカル管理画面を使います。

ルーターのポート開放やインターネットへの直接公開はしないでください。HTTP Basic認証を使うため、信頼できるLANまたはTailscale内だけで利用し、端末ごとに推測しにくいパスワードを設定してください。クラウド中継はありません。

## 既存の開発版との関係

公開Android版のアプリIDは io.github.ryoyavx.guardcamera です。従来のdebug版 com.example.guardcamera とは別アプリとして共存し、設定・認証情報・録画の自動移行はありません。必要な記録がある場合はdebug版をアンインストールしないでください。

## 現在の制限

- QRペアリングと自動探索は未実装です。
- Windows側の音声、録画、動体検知、ブラウザタブを閉じたままのカメラ取込は未実装です。
- PC実カメラの640×480 JPEG配信とAndroidアプリ内での実映像更新を確認しました。Tailscale経由の長時間運用は未検証です。
- Windows実行ファイルに商用コード署名はありません。インストール判断時は下のSHA-256でファイルを確認してください。

## ファイル確認

- Android APK SHA-256: F2B31ABADBA6756522B7DBD7FA5D97242FC0D4D41FFF48F00D86AA536A6AC71D
- Windows ZIP SHA-256: 1B838FC34892CDED50DE16FAA3F2F1D95DB834CB85C4170FC247B8FA826C1BEC
- Android署名証明書 SHA-256: 3C7538FBF9188617750C0BDD37779958240B6315841611F8B1ACB9E94B6AB1C8

この公開リポジトリは配布ファイルと説明だけを置き、ソースコード、署名鍵、視聴パスワード、利用者データは含めません。
