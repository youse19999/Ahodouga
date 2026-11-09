# Ahodouga Tauri セットアップ（Windows）

## 前提

- Windows x64
- Microsoft C++ Build Tools（MSVC）
- Microsoft Edge WebView2
- Rust stable MSVC toolchain
- Node.jsとpnpm 11.25.0

検証時の構成はTauri 2.12.5、@tauri-apps/cli 2.12.4でした。依存バージョンはCargo.lockとpnpm-lock.yamlに固定しています。

## 起動

```powershell
pnpm install
pnpm dev
```

現在のフロントエンドはweb/の静的HTML/CSSです。別の開発サーバーやportは使いません。

## リリースビルド

```powershell
pnpm build
```

成果物はsrc-tauri/target/release/bundle/以下に出ます。

- bundle/msi/Ahodouga_0.1.0_x64_en-US.msi
- bundle/nsis/Ahodouga_0.1.0_x64-setup.exe

## 作業範囲

このセットアップでは新規のsrc-tauri/とweb/だけを追加しました。既存テンプレートおよびAI関連ファイルは変更対象に含めません。リポジトリの別機能へ統合する場合は、その既存構成を確認してから接続してください。
