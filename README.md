# Unity AutoBuildVoicevoxServer

Unityでゲームの再生をしたときに自動でVoicevoxのサーバーを立ててくれるアセットです。

## 動作環境

- Unity 2022.3.0f1
- Windows (Linux、MacOSでは動作しません)

## 導入方法

### 必要なファイルのダウンロード

1. [Releases](https://github.com/suzuuuuu09/unity-auto-build-voicevox-server/releases) から2つのファイルをダウンロードしてください。
2. [こちら](https://github.com/VOICEVOX/voicevox_engine/tags) からビルドアーカイブをダウンロードしてください。

### アセットの導入

1. Assets -> Import Package -> Custom Package...
2. 先ほどダウンロードした `unity-auto-build-voicevox-server.unitypackage` を選択します。
3. Importを押し、アセットの導入ができれば完了です。

### サーバーファイルの設定

1. 先ほどダウンロードしたVoicevoxのビルドアーカイブを解凍し、ディレクトリ名を `server` に変更します。
2. Cドライブ直下に `Voicevox` というディレクトリを作ります。
3. 先ほどダウンロードしたVoicevoxのビルドアーカイブと`voicevox_server.bat`を以下のように設置してください。

```
Voicevox
├ server
│ ├ run.exe
│ └ voicevox_core.dll
│   (以下略)
└ voicevox_server.bat
```

### 動作確認

Unityでゲームの実行をし、コンソールに `Voicevoxサーバーを起動しました。` とログが出れば成功です。お疲れさまでした。
