# 图像像素查看工具 (Image Pixel Viewer)

> **声明 / Credits**
> 本项目代码及文档由 deepseek和yuanbao协助生成与维护。

一个功能强大的基于浏览器的图像像素查看工具，支持多种图像格式，可放大至单个像素级别，实时显示像素坐标、RGB值和尺寸信息。(因为个人从事计算机视觉和机器人感知方向，有时需要一个像素查看工具，但现有的发现都不好用，于是参考一些工具，用大模型生成一个算了)

[https://via.placeholder.com/800x400/2c3e50/ffffff?text=Image+Pixel+Viewer+Screenshot](https://via.placeholder.com/800x400/2c3e50/ffffff?text=Image+Pixel+Viewer+Screenshot)

## 🌟 主要特性

* **多格式支持** : 支持BMP、JPG、JPEG、PNG、PGM(P2/P5)、GIF、WEBP、TIFF等主流图像格式
* **像素级放大** : 支持最大1600%的放大比例，清晰查看每个像素
* **实时信息显示** : 鼠标悬停时实时显示坐标、RGB值和像素大小
* **视图控制** : 支持平移、缩放、网格显示、视图重置等功能
* **用户友好** : 直观的界面设计，详细的使用说明
* **零依赖** : 单文件HTML应用，无需安装任何软件

## 📋 功能列表

### 核心功能

* ✅ 图像导入（本地文件上传）
* ✅ 鼠标位置追踪显示
* ✅ 像素坐标与RGB值显示
* ✅ 图像平移和缩放控制
* ✅ 像素网格显示切换
* ✅ 最大放大至单个像素可见

### 高级功能

* ✅ PGM格式完整支持（P2 ASCII + P5 Binary）
* ✅ 实时颜色预览
* ✅ 键盘快捷键支持
* ✅ 响应式设计
* ✅ 错误处理与用户提示
* ✅ 示例图像和PGM文件生成

## 🚀 快速开始

### 在线使用

直接访问：[GitHub Pages链接] 或下载项目后在浏览器中打开 `index.html`

### 本地使用

1. 克隆仓库：

   ```
   git clone https://github.com/sc779733661/Image-Pixel-Viewer.git
   ```

2. 进入项目目录：

   ```
   cd Image-Pixel-Viewer
   ```

3. 在浏览器中打开 `index.html`文件

### 文件上传

* 点击"上传图像"按钮选择本地图片文件
* 支持拖拽文件到浏览器窗口（部分浏览器）
* 使用"使用示例图像"快速体验

## 🎮 使用说明

### 基本操作

| 操作                   | 方法                            |
| ---------------------- | ------------------------------- |
| **查看像素信息** | 在图像上移动鼠标                |
| **平移视图**     | 按住鼠标左键拖动                |
| **缩放视图**     | 使用鼠标滚轮或点击放大/缩小按钮 |
| **切换网格**     | 点击"网格"按钮或按 `G`键      |
| **重置视图**     | 点击"重置视图"按钮或按 `0`键  |

### 快捷键

| 按键  | 功能         |
| ----- | ------------ |
| `+` | 放大         |
| `-` | 缩小         |
| `0` | 重置视图     |
| `G` | 切换网格显示 |

### PGM文件支持

* **P2格式** : ASCII编码的PGM文件
* **P5格式** : 二进制编码的PGM文件
* 支持带注释的PGM文件（以#开头）
* 提供示例PGM文件下载功能

## 🔧 技术实现

### 核心技术栈

* **HTML5 Canvas** : 图像渲染和交互
* **JavaScript ES6+** : 核心逻辑实现
* **CSS3** : 现代UI设计和动画效果
* **File API** : 本地文件读取和处理

### 关键算法

* **PGM解析器** : 支持P2(ASCII)和P5(二进制)格式
* **坐标转换** : 屏幕坐标与图像坐标的精确映射
* **图像缩放** : 双线性插值和像素对齐
* **实时渲染** : 高效的Canvas绘制优化

### 架构设计

```
├── 用户界面层 (UI Layer)
│   ├── 控制面板
│   ├── 画布容器
│   └── 信息显示
├── 业务逻辑层 (Logic Layer)
│   ├── 图像加载器
│   ├── 格式解析器
│   ├── 坐标转换器
│   └── 视图控制器
└── 数据层 (Data Layer)
    ├── 图像数据
    ├── 状态管理
    └── 配置信息
```

## 📁 项目结构

```
Image-Pixel-Viewer/
├── index.html          # 主页面文件
├── README.md           # 项目说明文档
├── LICENSE            # 开源协议
├── examples/          # 示例文件
│   ├── sample.jpg
│   ├── sample.png
│   └── sample.pgm
└── docs/              # 文档目录
    ├── screenshots/
    └── api.md
```

## 🌐 浏览器兼容性

| 浏览器  | 版本要求 | 支持状态      |
| ------- | -------- | ------------- |
| Chrome  | 60+      | ✅ 完全支持   |
| Firefox | 55+      | ✅ 完全支持   |
| Safari  | 12+      | ✅ 完全支持   |
| Edge    | 79+      | ✅ 完全支持   |
| IE      | 11       | ⚠️ 部分支持 |

## 🤝 贡献指南

我们欢迎所有形式的贡献！请阅读以下指南：

### 如何贡献

1. Fork 本项目
2. 创建特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 创建 Pull Request

### 开发环境设置

```
# 克隆项目
git clone https://github.com/sc779733661/Image-Pixel-Viewer.git

# 使用本地服务器运行（可选）
python -m http.server 8000
# 或
npx serve .
```

### 代码规范

* 使用ESLint进行JavaScript代码检查
* 遵循Semantic Versioning版本规范
* 提交信息使用Conventional Commits格式

## 📄 开源协议

本项目采用 MIT License 开源协议。

```
MIT License

Copyright (c) 2023 Your Name

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

## 🙏 致谢

* 感谢所有为项目贡献代码的开发者
* 感谢提供示例图像的 [Unsplash](https://unsplash.com/)
* 感谢开源社区的支持和帮助

## 📞 联系方式

* **项目主页** : [https://github.com/sc779733661/Image-Pixel-Viewer](https://github.com/sc779733661/Image-Pixel-Viewer)
* **问题反馈** : [https://github.com/sc779733661/Image-Pixel-Viewer/issues](https://github.com/sc779733661/Image-Pixel-Viewer/issues)
* **邮箱联系** : <your.email@example.com>
* **讨论群组** : [Discord/Slack链接]

## 🗺️ 路线图

### 即将推出的功能

* [ ] 批量图像处理
* [ ] 颜色选择器工具
* [ ] 直方图显示
* [ ] 图像统计信息
* [ ] 导出像素数据
* [ ] 插件系统支持

### 长期目标

* [ ] WebAssembly加速
* [ ] 3D图像支持
* [ ] 移动端APP版本
* [ ] 云端同步功能

---

如果这个工具对您有帮助，请给我们一个 ⭐ Star！

**Made with ❤️ by the Image Pixel Viewer Team**
