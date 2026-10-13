# インポートガイド

[English](install.md) | **日本語** | [한국어](install.ko.md) | [简体中文](install.zh-CN.md)

## VRChat プロジェクト

### 必須の依存コンポーネント

[![VRChat Creator Companion](https://img.shields.io/badge/VRChat_Creator_Companion-core_dependency-007ec6?style=flat-square)](https://vcc.docs.vrchat.com/guides/getting-started)
[![Modular Avatar](https://img.shields.io/badge/Modular_Avatar-core_dependency-007ec6?style=flat-square)](https://modular-avatar.nadena.dev/docs/intro)
[![lilToon](https://img.shields.io/badge/lilToon-core_dependency-007ec6?style=flat-square)](https://lilxyzw.github.io/lilToon/)

#### Unity 2022.3.22f1

> 本プロジェクトが依存する Unity エディターのバージョン

#### VRChat Creator Companion（VCC）

> VRChat 公式ツールです。VRChat Unity プロジェクトの Editor と各種 SDK をまとめて管理でき、手作業で行うより手間がかかりません。

<https://vcc.docs.vrchat.com/guides/getting-started>

#### Modular Avatar

> 非破壊的な衣装・小道具の装着に使われます。多くの衣装・小道具の制作者がこのツールを使っており、購入した prefab をそのままアバターにドラッグするだけで使えます。

<https://modular-avatar.nadena.dev/docs/intro>（VCC からのインストールを推奨）

> [!WARNING]
> 本プロジェクトの pw_outfit（prefab）と pw_pudding_root（prefab）は、Modular Avatar コンポーネントによって、アップロード時に該当する animator・parameter・menu を pw_core（prefab）へ自動的に統合します。インストールしていないとアップロードに成功しません。

必要に応じて、pw_outfit（prefab）または pw_pudding_root（prefab）、あるいはその両方をアバターから削除できます

> そのまま play mode に入ると、衣装がアバターに装着されていないことがわかります。VCC から Gesture Manager をインストールすると、play mode でも Modular Avatar が有効になります。

#### lilToon Shader

> VRChat のトゥーン向けマテリアルでよく使われる Shader です

<https://lilxyzw.github.io/lilToon/>（VCC からのインストールを推奨）

> [!WARNING]
> 本プロジェクトのマテリアルは lilToon shader を使用しています。インストールしていないと、マテリアルが紫色に表示されます。

### 推奨コンポーネント（オプション）

[![VRCFury](https://img.shields.io/badge/VRCFury-recommended-007ec6?style=flat-square)](https://vrcfury.com/download)
[![GogoLoco](https://img.shields.io/badge/GogoLoco-recommended-007ec6?style=flat-square)](https://gogoloco.net/)
[![VRCFaceTracking](https://img.shields.io/badge/VRCFaceTracking-recommended-007ec6?style=flat-square)](https://docs.vrcft.io/docs/intro/getting-started)

#### GogoLoco

> アバターに楽しい locomotion ポーズや便利な飛行機能などを追加します

GogoLoco は VRCFury に依存しています。VRCFury は Modular Avatar に似た自動装着ツールです。VRCFury と GogoLoco をプロジェクトに追加し、GogoLoco-VRCFury（Prefab）をアバターに追加します

<https://vrcfury.com/download>（VCC からのインストールを推奨）
<https://gogoloco.net/>（VCC からのインストールを推奨）

#### VRCFaceTracking-Templates（Jerry's templates）

> フェイストラッキング対応のヘッドセットをお持ちなら、このコンポーネントでアバターを手軽にフェイストラッキング対応にできます

VRCFaceTracking-Templates（Jerry's templates）をダウンロードし、「VF_ARKit_VRCFT」をモデルにドラッグします
<https://github.com/Adjerry91/VRCFaceTracking-Templates>（VCC からのインストールを推奨）

PC 上で VRCFaceTracking を実行し、ヘッドセットのフェイストラッキングデータを OSC に変換して VRChat 内のアバターを動かします
<https://docs.vrcft.io/docs/intro/getting-started>

## VRM プロジェクト

[![UniVRM](https://img.shields.io/badge/UniVRM-0.x-007ec6?style=flat-square)](https://github.com/vrm-c/UniVRM/releases)

ダウンロードファイルにはパッケージ済みの VRM ファイルが含まれています。新しい VRM ファイルを書き出すには、プロジェクトに UniVRM 0.x を追加する必要があります
<https://github.com/vrm-c/UniVRM/releases>

## FBX エクスポート

書き出し設定は VRChat 公式ドキュメントの設定ガイド（Step 3 - Get the model into your project）を参照してください
<https://creators.vrchat.com/avatars/creating-your-first-avatar/>

![Blender の FBX 書き出し設定](../images/blender-fbx-export.webp)

- pw_base.fbx：Blender ファイル内で、armature の outfit ボーンコレクション（bone collections）のボーンをすべて削除し、armature と body を選択して書き出します
- pw_outfit.fbx：Blender ファイル内で、armature を armature_outfit にリネームし、armature_outfit と該当する衣装メッシュオブジェクトを選択して書き出します

## Substance Painter テクスチャ

本 SP プロジェクトのレイヤーマスクは、通常、SP プロジェクトに読み込まれた texture アセットを参照しており、描いて作ったものではありません

編集したい場合は、マスクを右クリックして Add Paint を選ぶと、Fill（参照している texture アセット）の上に重なり、Paint レイヤーで描画・編集できるようになります

![Substance Painter でのマスク編集](../images/sp-mask-paint.webp)
