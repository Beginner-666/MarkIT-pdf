# MarkIT — PDF 智能标注阅读器

> 一个运行在浏览器里的 PDF 阅读 & 批注工具，无需安装，无需服务器，打开即用。

**[🌐 在线体验](https://beginner-666.github.io/MarkIT-pdf/)**

---

## ✨ 功能特性

| 功能 | 说明 |
|------|------|
| 📄 PDF 渲染 | 高清渲染 PDF 每一页，支持缩放 |
| ✍️ 自由标注 | 在 PDF 上任意位置添加文字批注，支持拖拽、旋转、缩放 |
| 🎨 样式自定义 | 自由选择批注文字颜色和字号 |
| 📝 Markdown 支持 | 批注内容支持 Markdown 格式（标题、列表、代码块等） |
| 🧮 LaTeX 公式 | 支持 KaTeX 数学公式渲染 |
| 💾 自动持久化 | 使用 IndexedDB 本地保存工作区，关闭页面不丢失 |
| 📤 导出 PDF | 将批注嵌入 PDF 并导出，或直接覆盖保存源文件 |
| 🤖 AI 助手 | 集成通义千问（QWen），可边阅读边提问 |

---

## 🚀 快速开始

### 方式一：直接使用在线版

点击上方「在线体验」链接，在浏览器中打开即可，无需注册账号。

### 方式二：本地使用

直接下载 `index.html`，用任意现代浏览器（Chrome / Edge / Firefox）打开即可。

```bash
# 或者克隆整个仓库
git clone https://github.com/beginner-666/markit-pdf.git
cd markit-pdf
# 用浏览器打开 index.html
```

---

## 🤖 AI 助手配置

本工具集成了阿里云**通义千问（QWen）** AI 对话功能，需要您自行申请免费 API Key。

### 获取 API Key

1. 访问 [阿里云百炼控制台](https://bailian.console.aliyun.com/)
2. 注册 / 登录阿里云账号
3. 开通 DashScope 服务，获取 API Key

### 在工具中配置

1. 打开 MarkIT，点击右上角 **「AI 助手」** 按钮
2. 点击 **「配置 Key」**
3. 粘贴您的 API Key，点击确定

> 🔒 **隐私安全**：您的 API Key 仅保存在**本地浏览器**（localStorage）中，不会上传到任何服务器。

---

## 📖 使用说明

### 打开 PDF

- 点击中央上传区域上传

### 添加批注

1. 点击顶部工具栏的 **「添加模式」** 按钮，进入批注模式（按钮变为金色状态）
2. 在 PDF 任意位置**单击**，弹出编辑器
3. 输入文字内容（支持 Markdown），选择颜色和字号
4. 点击 **「完成」** 完成批注

### 编辑 / 删除批注

- **双击**已有批注：打开编辑器修改内容
- 编辑器底部点击 **「删除」** 可移除该批注
- 单击批注后可**拖拽**移动位置，拖动顶部绿点可**旋转**，拖动四角可**缩放**

### 保存工作

| 操作 | 说明 |
|------|------|
| 自动保存 | 批注数据实时保存到浏览器本地，关闭页面下次打开自动恢复 |
| 保存 PDF | 将批注渲染进 PDF，直接覆盖源文件 |
| 导出 PDF | 将批注渲染进 PDF，另存为新文件 |
| 退出并保存 | 保存并关闭当前文件，回到初始页面|

---

## 🛠️ 技术栈

- **[PDF.js](https://mozilla.github.io/pdf.js/)** — PDF 渲染
- **[pdf-lib](https://pdf-lib.js.org/)** — PDF 写入与导出
- **[marked.js](https://marked.js.org/)** — Markdown 解析
- **[KaTeX](https://katex.org/)** — 数学公式渲染
- **[html2canvas](https://html2canvas.hertzen.com/)** — 批注截图
- **[idb-keyval](https://github.com/jakearchibald/idb-keyval)** — IndexedDB 持久化
- **通义千问 (QWen)** — AI 对话

---

## 🌍 浏览器兼容性

| 浏览器 | 支持情况 |
|--------|----------|
| Chrome  | ✅ 完全支持（推荐） |
| Edge  | ✅ 完全支持 |


> 建议使用 **Chrome** 或 **Edge** 以获得最佳体验，"直接覆盖保存"功能依赖 [File System Access API](https://developer.mozilla.org/en-US/docs/Web/API/File_System_Access_API)。
> 建议使用同一浏览器打开本网站

---

## 🙋 常见问题

**Q: 我的批注会上传到云端吗？**
A: 不会。所有数据（包括 PDF 内容和批注）均存储在您的本地浏览器中，不会发送到任何服务器。

**Q: 换了浏览器或清除缓存后，批注还在吗？**
A: 不在。批注保存在浏览器的 IndexedDB 中，清除浏览器数据或更换浏览器后会丢失。建议定期使用「保存 PDF」功能备份。

**Q: 支持手写批注吗？**
A: 目前仅支持文字批注（支持 Markdown 格式），暂不支持手绘。

**Q: AI 助手支持分析 PDF 内容吗？**
A: 目前 AI 助手为独立对话框，您可以将感兴趣的段落复制后粘贴给 AI 提问。
