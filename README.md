# MornSteam

## 概要

Steam APIのUnity統合ラッパー。SteamworksのマネージャーとSteam機能へのアクセスを提供するライブラリ。

## 依存関係

| 種別 | 名前 |
|------|------|
| 外部パッケージ | Steamworks.NET |
| Mornライブラリ | なし |

## 使い方

### 初期化

```csharp
MornSteamManager.Initialize();
```

### 状態確認

```csharp
bool isInitialized = MornSteamManager.Initialized;
string userId = MornSteamManager.UserId;
```

### 入力デバイス取得

```csharp
List<string> inputs = MornSteamManager.GetInputs();
```

### アチーブメント管理

```csharp
MornSteamManager.TryGetAchievement("label", out bool isUnlocked);
MornSteamManager.SetAchievement("label");
```

### ゲーム言語取得

```csharp
string language = MornSteamManager.GetCurrentGameLanguage();
```

### 有効化

`USE_STEAM` プリプロセッサシンボルを定義することで有効化されます。未定義時はスタブ実装を提供します。
