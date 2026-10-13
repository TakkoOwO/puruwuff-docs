# Installation guide

**English** | [日本語](install.ja.md) | [한국어](install.ko.md) | [简体中文](install.zh-CN.md)

## VRChat project

### Core dependencies

[![VRChat Creator Companion](https://img.shields.io/badge/VRChat_Creator_Companion-core_dependency-007ec6?style=flat-square)](https://vcc.docs.vrchat.com/guides/getting-started)
[![Modular Avatar](https://img.shields.io/badge/Modular_Avatar-core_dependency-007ec6?style=flat-square)](https://modular-avatar.nadena.dev/docs/intro)
[![lilToon](https://img.shields.io/badge/lilToon-core_dependency-007ec6?style=flat-square)](https://lilxyzw.github.io/lilToon/)

#### Unity 2022.3.22f1

> The Unity editor version this project depends on

#### VRChat Creator Companion (VCC)

> The official VRChat tool for managing the Unity Editor and the various SDKs involved in VRChat Unity projects in one place — less hassle than doing it manually.

<https://vcc.docs.vrchat.com/guides/getting-started>

#### Modular Avatar

> Used for non-destructive clothing and prop attachment. Many clothing and prop developers use this tool, so when you buy their prefabs you can drag them straight onto the avatar and use them right away.

<https://modular-avatar.nadena.dev/docs/intro> (installing it via VCC is recommended)

> [!WARNING]
> This project's pw_outfit (prefab) and pw_pudding_root (prefab) use Modular Avatar components to automatically merge the relevant animator, parameters, and menu into pw_core (prefab) at upload time. If it is not installed, the upload will not succeed.

Depending on what you need, you can remove pw_outfit (prefab), pw_pudding_root (prefab), or both from the avatar.

> If you enter play mode directly, you will find that the clothing is not attached to the avatar. Please install Gesture Manager via VCC so that Modular Avatar takes effect in play mode.

#### lilToon Shader

> A shader commonly used for VRChat toon materials

<https://lilxyzw.github.io/lilToon/> (installing it via VCC is recommended)

> [!WARNING]
> This project's materials use the lilToon shader. If it is not installed, the materials will display as purple.

### Recommended components (optional)

[![VRCFury](https://img.shields.io/badge/VRCFury-recommended-007ec6?style=flat-square)](https://vrcfury.com/download)
[![GogoLoco](https://img.shields.io/badge/GogoLoco-recommended-007ec6?style=flat-square)](https://gogoloco.net/)
[![VRCFaceTracking](https://img.shields.io/badge/VRCFaceTracking-recommended-007ec6?style=flat-square)](https://docs.vrcft.io/docs/intro/getting-started)

#### GogoLoco

> Gives the avatar some fun locomotion poses and convenient flying features.

GogoLoco depends on VRCFury. VRCFury is an auto-attachment tool similar to Modular Avatar. Add VRCFury and GogoLoco to the project, then add GogoLoco-VRCFury (Prefab) to the avatar.

<https://vrcfury.com/download> (installing it via VCC is recommended)
<https://gogoloco.net/> (installing it via VCC is recommended)

#### VRCFaceTracking-Templates (Jerry's templates)

> If you have a headset that supports face tracking, this component quickly makes the avatar face-tracking ready.

Download VRCFaceTracking-Templates (Jerry's templates) and drag "VF_ARKit_VRCFT" onto the model.
<https://github.com/Adjerry91/VRCFaceTracking-Templates> (installing it via VCC is recommended)

Run VRCFaceTracking on PC to convert the headset's face-tracking data into OSC that drives the avatar in VRChat.
<https://docs.vrcft.io/docs/intro/getting-started>

## VRM project

[![UniVRM](https://img.shields.io/badge/UniVRM-0.x-007ec6?style=flat-square)](https://github.com/vrm-c/UniVRM/releases)

The downloaded files already include a packaged VRM file. To export a new VRM file, you need to add UniVRM 0.x to the project.
<https://github.com/vrm-c/UniVRM/releases>

## FBX export

For the export settings, refer to the settings guide in VRChat's official documentation (Step 3 - Get the model into your project).
<https://creators.vrchat.com/avatars/creating-your-first-avatar/>

![Blender FBX export settings](../images/blender-fbx-export.webp)

- pw_base.fbx: In the Blender file, delete all bones in the outfit bone collection(s) of the armature, then select the armature and body and export.
- pw_outfit.fbx: In the Blender file, rename the armature to armature_outfit, then select armature_outfit and the corresponding clothing mesh objects and export.

## Substance Painter textures

The layer masks in this SP project usually reference texture assets imported into the SP project rather than being painted.

If you want to edit them, right-click the mask and choose Add Paint. It will sit on top of the Fill (the referenced texture asset), and you can then paint and edit on the Paint layer.

![Editing a mask in Substance Painter](../images/sp-mask-paint.webp)
