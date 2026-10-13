# Photoshop VA Tracking Zero｜PS 文字字距一键归零

**一键将当前 Photoshop 文档中的文字图层字距（Tracking）批量设为 0。** 支持遍历图层组，省去逐层选中文字、手动调整“VA”字距的操作。

![Photoshop](https://img.shields.io/badge/Adobe-Photoshop-31A8FF?logo=adobephotoshop&logoColor=white)
![Script](https://img.shields.io/badge/Script-JSX%20%7C%20ExtendScript-555555)
![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20macOS-0078D6)

## ✨ 功能特点

- **批量归零**：尝试将文字图层的 `textItem.tracking` 设置为 `0`。
- **递归处理**：遍历当前文档及所有嵌套图层组。
- **自动跳过**：非文字图层和无法修改的文字图层会被跳过。
- **执行反馈**：弹窗提示成功执行设置的文字图层数量。
- **轻量运行**：单个 `.jsx` 脚本文件，无须单独安装软件。

## 📥 下载脚本

[⬇️ 直接下载 Photoshop_VA_Tracking_Zero.jsx](https://github.com/8820387-byte/Photoshop-VA-Tracking-Zero/raw/refs/heads/main/Photoshop_VA_Tracking_Zero.jsx)

也可以在仓库页面点击 **Code → Download ZIP** 下载项目。

## 🚀 使用方法

1. 下载 `Photoshop_VA_Tracking_Zero.jsx`。
2. 打开 Adobe Photoshop 和要处理的 PSD 文档。
3. **先保存备份**，以免批量更改影响原稿。
4. 在 Photoshop 中依次选择 **文件 → 脚本 → 浏览（File → Scripts → Browse）**。
5. 选择 `.jsx` 文件运行，完成后查看弹窗提示。
6. 检查文字排版，确认效果后保存文档。

## 🗂️ 项目结构

```text
Photoshop-VA-Tracking-Zero/
├── Photoshop_VA_Tracking_Zero.jsx    # 批量归零脚本
└── README.md                         # 使用说明
```

## ⚠️ 使用须知

- 只处理**当前打开且处于活动状态的文档**；不会批量处理磁盘上的多个 PSD 文件。
- 该脚本设置的是 **Tracking（字距）**，不等同于逐字符的 Kerning（字偶间距）重置。
- 部分文字图层可能存在局部字符样式；`textItem.tracking = 0` 的实际效果因 Photoshop 版本和文字属性而异，请执行后人工检查。
- 锁定、受限或异常文字图层可能无法修改，脚本会跳过这类图层。
- 使用前请备份 PSD；脚本不负责自动恢复或创建备份。
- 脚本基于 Photoshop ExtendScript / JSX，兼容性需以实际 Photoshop 版本测试为准。

## 🔧 原理

遍历活动文档中的所有图层及嵌套图层组，对每个 Photoshop 文字图层执行：

```javascript
layer.textItem.tracking = 0;
```

## 🤝 反馈

如遇问题，欢迎通过仓库 Issues 提交 Photoshop 版本、可复现步骤及报错信息（请先隐藏私密内容）。

> 非 Adobe 官方工具。若项目对你有帮助，欢迎点一个 ⭐ Star！
