# ✂️ ClipForge / 剪集

**macOS 视频批量裁剪工具 —— 拖入文件夹，标记一次，批量裁剪全部视频**

![Platform](https://img.shields.io/badge/platform-macOS_13.0+-blue.svg)
![Swift](https://img.shields.io/badge/Swift-6.0-orange.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)

---

## 📖 简介

ClipForge（剪集）是一款专为 macOS 设计的视频批量裁剪工具，帮助你快速、无损地处理大量视频文件。无论是批量去除片头片尾、提取精彩片段，还是按关键帧精确切分，剪集都能以专业级效率完成。

**核心工作流：拖入文件夹 → 双击设样本 → 标记片头/片尾 → 一键批量裁剪**

---

## ✨ 功能特性

### 🎬 批量裁剪
- 支持一次性导入整个文件夹（最多 3 级子目录递归扫描）
- 自动识别 MP4、MOV、MKV、AVI、M4V、MPG、MPEG、WEBM、FLV、3GP、WMV 等主流格式
- 拖拽文件夹到窗口即可开始

### ⚡ 无损流复制
- 基于 FFmpeg stream copy 技术（`-c copy`），裁剪过程不重编码
- 速度极快，画质无损，输出文件与原视频完全一致

### 🎯 关键帧检测与吸附
- 自动检测视频所有 I 帧（关键帧）
- 关键帧精确吸附：裁剪点自动对齐到最近关键帧，避免黑屏
- 上一帧/下一帧快速跳转导航

### ✂️ 片头片尾独立控制
- 可单独设置片头时长、片尾时长
- 独立开关：仅去片头、仅去片尾或两者都去
- 批量应用到列表内所有视频

### 📐 精确时间控制
- 时间码输入（HH:MM:SS.ms）
- 步进按钮（0.1s / 1s）
- 键盘快捷键：←/→ 单步 · Shift+←/→ 大步 · ⌥+←/→ 关键帧跳转

### ⚙️ 预设管理
- 保存常用裁剪参数为预设
- 一键应用预设到当前视频

### 🔄 安全替换
- 裁剪后可自动替换原文件（原文件移入废纸篓，可恢复）
- `_cropped` 临时文件夹自动清理
- 输出文件保存在原目录

---

## 📸 截图

| 主界面 | 样本标记 | 裁剪参数 |
|:---:|:---:|:---:|
| ![主界面](screenshots/main.png) | ![标记](screenshots/mark.png) | ![参数](screenshots/params.png) |

---

## 🚀 快速开始

### 系统要求
- macOS 13.0 Ventura 或更高版本
- Apple Silicon 或 Intel 处理器

### 安装方式

#### Mac App Store（推荐）
[![App Store](https://img.shields.io/badge/App_Store-下载-blue.svg)](https://apps.apple.com/your-app-link)

#### 手动下载
1. 前往 [Releases](https://github.com/yourusername/ClipForge/releases) 页面
2. 下载最新版本的 `ClipForge.dmg`
3. 打开 `.dmg` 文件，将 `ClipForge.app` 拖入 `Applications` 文件夹

---

## 📖 使用指南

### 第一步：加载视频
将包含视频的文件夹**拖拽**到软件窗口，左侧列表自动显示所有视频文件。

支持格式：`MP4, MOV, MKV, AVI, M4V, 3GP, FLV, WMV, MPG, MPEG, WEBM`

### 第二步：设定样本
在列表中**双击**任意视频，设为「样本」，右侧预览区自动加载并播放。

### 第三步：标记裁剪点
- **标记片头**：拖动进度条到正片开始位置，点击【标记片头】
- **标记片尾**：拖动进度条到正片结束位置，点击【标记片尾】
- **关键帧提示**：若当前标记偏离关键帧，界面会显示偏离距离，点击【吸附到关键帧】可自动对齐

### 第四步：批量裁剪
点击 **【开始批量裁剪】**，自动将样本参数应用到所有选中视频，输出到原文件夹下的 `_cropped` 子目录。

### 第五步：确认替换（可选）
确认裁剪结果满意后，点击 **【确认替换原文件】**，原文件移入废纸篓，裁剪文件移至原位。

---

## 💰 商业模式

| 模式 | 说明 |
|:---|:---|
| **免费模式** | 每日 3 次免费批量裁剪，配额每日 00:00 重置 |
| **付费解锁** | ¥9.00 一次性买断，永久解锁无限次裁剪 |
| **购买方式** | App Store 内购（Product ID: com.smartcutter.unlimited） |
| **授权范围** | 同一 Apple ID 下所有 Mac 通用 |

---

## 🛠 技术栈

| 组件 | 说明 |
|:---|:---|
| **语言** | Swift 6 |
| **UI 框架** | SwiftUI (macOS 13.0+) |
| **视频处理** | FFmpeg (流复制) + AVFoundation |
| **视频播放** | AVFoundation |
| **最低系统** | macOS 13.0 Ventura |

---

## 🤝 贡献指南

欢迎提交 Issue 和 Pull Request！

1. Fork 本仓库
2. 创建您的特性分支 (`git checkout -b feature/amazing-feature`)
3. 提交您的修改 (`git commit -m 'Add some amazing feature'`)
4. 推送到分支 (`git push origin feature/amazing-feature`)
5. 打开一个 Pull Request

---

## 📄 许可证

本项目采用 **MIT 许可证** 开源。详见 [LICENSE](LICENSE) 文件。

## ⚠️ 第三方声明

本软件使用了以下开源项目：
- **[FFmpeg](https://ffmpeg.org)**：采用 LGPLv2.1 许可，源码可于 [ffmpeg.org](https://ffmpeg.org) 获取。

---

## 📧 联系方式

- 邮箱：[appdev@micrao.com]
- 项目主页：[GitHub 仓库链接]

---

**ClipForge / 剪集 —— 让视频整理更高效。** ✂️
