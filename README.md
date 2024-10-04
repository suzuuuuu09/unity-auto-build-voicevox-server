# Unity AutoBuildVoicevoxServer

(2024/10/05 更新)  
Unityでゲームの再生をしたときに自動でVoicevoxのサーバーを立ててくれるアセットです。

## 動作環境

- Unity 2022.3.0f1
- Windows (Linux、MacOSでは動作しません)
- [7-zip](https://7-zip.opensource.jp/) と [curl](https://curl.se) がインストール済み (セットアップをするために必要です)

## 導入方法

<details open>
<summary><code>setup.bat</code> を使った導入</summary>

### Ⅰ. 必要なファイルのダウンロード

[Releases](https://github.com/suzuuuuu09/unity-auto-build-voicevox-server/releases) から最新バージョンの `auto-build-voicevox-server<バージョン名>.zip`をダウンロードしてください。 (0.2.0以降)

### Ⅱ. アセットの導入

1. Assets -> Import Package -> Custom Package...
2. 先ほどダウンロードした `auto-build-voicevox-server<バージョン名>.zip` の中にある `unity-auto-build-voicevox-server.unitypackage` を選択します。
3. Importを押し、アセットの導入ができれば完了です。

### Ⅲ. サーバーファイルの設定

1. 先ほどダウンロードした `auto-build-voicevox-server<バージョン名>.zip` の中にある `setup.bat` を実行します。
2. `セットアップが完了しました。` と出たら、何かキーを押して終了してください。
3. 実行後、ディレクトリ構造が次のようになっていることを確認してください。

```
C:/
└ Voicevox
  ├ server
  │ ├ run.exe
  │ └ voicevox_core.dll
  │     ︙
  └ voicevox_server.bat
```

> [!IMPORTANT]
> セットアップに失敗した場合は [7-zip](https://7-zip.opensource.jp/) または [curl](https://curl.se) がインストールしていることを確認してください。

### Ⅳ. 動作確認

Unityでゲームの実行をし、コンソールに `Voicevoxサーバーを起動しました。` とログが出れば成功です。お疲れさまでした。

</details>

<details>
<summary>手動での導入</summary>

### Ⅰ. 必要なファイルのダウンロード

1. [Releases](https://github.com/suzuuuuu09/unity-auto-build-voicevox-server/releases) から最新バージョンの `auto-build-voicevox-server<バージョン名>.zip`をダウンロードしてください。 (0.2.0以降)
2. [こちら](https://github.com/VOICEVOX/voicevox_engine/tags) からビルドアーカイブをダウンロードしてください。

### Ⅱ. アセットの導入

1. Assets -> Import Package -> Custom Package...
2. 先ほどダウンロードした `auto-build-voicevox-server<バージョン名>.zip` の中にある `unity-auto-build-voicevox-server.unitypackage` を選択します。
3. Importを押し、アセットの導入ができれば完了です。

### Ⅲ. サーバーファイルの設定

1. 先ほどダウンロードしたVoicevoxのビルドアーカイブを解凍し、ディレクトリ名を `server` に変更します。
2. Cドライブ直下に `Voicevox` というディレクトリを作ります。
3. 先ほどダウンロードしたVoicevoxのビルドアーカイブと`voicevox_server.bat`を以下のように設置してください。

```
C:/
└ Voicevox
  ├ server
  │ ├ run.exe
  │ └ voicevox_core.dll
  │     ︙
  └ voicevox_server.bat
```

### Ⅳ. 動作確認

Unityでゲームの実行をし、コンソールに `Voicevoxサーバーを起動しました。` とログが出れば成功です。お疲れさまでした。
</details>
