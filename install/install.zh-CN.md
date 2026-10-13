# 导入指南

[English](install.md) | [日本語](install.ja.md) | [한국어](install.ko.md) | **简体中文**

## VRChat 项目

### 核心依赖组件

[![VRChat Creator Companion](https://img.shields.io/badge/VRChat_Creator_Companion-core_dependency-007ec6?style=flat-square)](https://vcc.docs.vrchat.com/guides/getting-started)
[![Modular Avatar](https://img.shields.io/badge/Modular_Avatar-core_dependency-007ec6?style=flat-square)](https://modular-avatar.nadena.dev/docs/intro)
[![lilToon](https://img.shields.io/badge/lilToon-core_dependency-007ec6?style=flat-square)](https://lilxyzw.github.io/lilToon/)

#### Unity 2022.3.22f1

> 本项目依赖的 Unity 编辑器版本

#### VRChat Creator Companion（VCC）

> VRChat 官方工具, 用于统一管理 VRChat Unity 项目的 Editor 和涉及的各种 SDK, 相比手动操作更加省事

<https://vcc.docs.vrchat.com/guides/getting-started>

#### Modular Avatar

> 用于非破坏性服装和道具绑定, 很多服装道具的开发者会使用这个工具, 当你购买了他们的 prefab, 直接拖拽到角色身上直接就能使用.

<https://modular-avatar.nadena.dev/docs/intro>（推荐通过 VCC 安装）

> [!WARNING]
> 本项目的 pw_outfit (prefab) 和 pw_pudding_root (prefab), 是通过 Modular Avatar 组件, 自动在上传时将相关的 animator, parameter, menu 合并到 pw_core (prefab) 中, 如果不安装将无法成功上传.

你可以根据实际需要, 将 pw_outfit (prefab) 或 pw_pudding_root (prefab) 或两者一起, 在角色身上移除

> 如果你直接进入 play mode, 会发现服装没有绑定在角色身上, 请通过 VCC 安装 Gesture Manager, 可以让 Modular Avatar 在 play mode 中生效.

#### lilToon Shader

> VRChat 卡通材质常会用到的 Shader

<https://lilxyzw.github.io/lilToon/>（推荐通过 VCC 安装）

> [!WARNING]
> 本项目的材质球采用 lilToon shader, 如果不安装, 材质球会显示为紫色

### 推荐组件（可选）

[![VRCFury](https://img.shields.io/badge/VRCFury-recommended-007ec6?style=flat-square)](https://vrcfury.com/download)
[![GogoLoco](https://img.shields.io/badge/GogoLoco-recommended-007ec6?style=flat-square)](https://gogoloco.net/)
[![VRCFaceTracking](https://img.shields.io/badge/VRCFaceTracking-recommended-007ec6?style=flat-square)](https://docs.vrcft.io/docs/intro/getting-started)

#### GogoLoco

> 让模型拥有一些有趣的 locomotion pose, 以及便捷的飞行功能等

GogoLoco 依赖 VRCFury, VRCFury 是个类似于 Modular Avatar 的自动绑定工具. 将 VRCFury 和 GogoLoco 添加到项目中，并将 GogoLoco-VRCFury (Prefab) 添加进角色

<https://vrcfury.com/download>（推荐通过 VCC 安装）
<https://gogoloco.net/>（推荐通过 VCC 安装）

#### VRCFaceTracking-Templates（Jerry's templates）

> 如果你拥有支持面部捕捉的头显, 可以通过该组件快速让角色支持面捕

下载 VRCFaceTracking-Templates（Jerry's templates），并将「VF_ARKit_VRCFT」拖入模型
<https://github.com/Adjerry91/VRCFaceTracking-Templates>（推荐通过 VCC 安装）

在 PC 上运行 VRCFaceTracking, 用于将头显的面捕数据转化成 OSC 驱动 VRChat 中的角色
<https://docs.vrcft.io/docs/intro/getting-started>

## VRM 项目

[![UniVRM](https://img.shields.io/badge/UniVRM-0.x-007ec6?style=flat-square)](https://github.com/vrm-c/UniVRM/releases)

下载文件中已包含打包好的 VRM 文件, 若要导出新的 VRM 文件, 需要向项目中添加 UniVRM 0.x
<https://github.com/vrm-c/UniVRM/releases>

## FBX 导出

导出设置参考 VRChat 官方文档中的设置指南（Step 3 - Get the model into your project）
<https://creators.vrchat.com/avatars/creating-your-first-avatar/>

![Blender FBX 导出设置](../images/blender-fbx-export.webp)

- pw_base.fbx：在 Blender 文件中, 将 armature 中 outfit 骨骼集合（bone collections）的骨骼都删除, 然后选中 armature 和 body 导出
- pw_outfit.fbx：在 Blender 文件中, 将 armature 重命名为 armature_outfit, 然后选中 armature_outfit 和相应的服装网格物体导出

## Substance Painter 贴图

本 SP 项目的图层蒙版, 通常是引用导入到 SP 项目中的 texture 资源, 而非绘制得来.

如果你想编辑的话, 右键蒙版, Add Paint, 它会盖在 Fill（即引用的 texture 资源）的上方, 然后就可以在 Paint 层进行绘制编辑了

![Substance Painter 中编辑蒙版](../images/sp-mask-paint.webp)
