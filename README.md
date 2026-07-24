# Obsidian 严谨物理笔记模板 (Rigorous Physics Template)

一套专为 **电动力学**、**量子力学** 等硬核物理/数学教材设计的 Obsidian 笔记规范。

## ✨ 特性

*   **严格的 LaTeX 规范**：杜绝因 `$ |` 导致的渲染失败，统一使用 `\lvert \rvert`；公式 `$` 符号紧贴内容，无空格。
*   **Fast Text Color 深度集成**：通过语义化着色（红=致命错误，蓝=核心结论），实现“一眼定位”，极大提升复习效率。
*   **双区结构 (Dual-Zone)**：
    *   **🎯 速查结论区**：纯公式，无推导，适合考前突击和快速复盘。
    *   **📖 具体讲解区**：过程与结论分明，适合初次学习和深入理解。
*   **AI 自动化友好**：包含专门的 `template-instructions.txt`，直接复制给 AI（如 ChatGPT、Claude、元宝），即可批量生成风格高度统一的笔记。

## 🚀 快速开始

1.  **克隆仓库**：
    将此仓库克隆到你本地的 Obsidian 库根目录：bashgit clone https://github.com/你的用户名/obsidian-rigorous-physics-template.git
2.  **安装插件**：
在 Obsidian 设置 → 第三方插件市场中搜索并安装 **Fast Text Color**。
*   *注意：无需复杂配置，保持默认颜色主题即可，本模板已适配。*
3.  **查看示例**：
打开 `examples/` 文件夹，查看 `2.5.1-conductors.md` 或 `2.4.4-energy-remarks.md`，观察渲染效果。
4.  **开始使用 AI**：
复制 `template-instructions.txt` 的全部内容发送给 AI，然后将你的教材截图或文字发给 AI，它会自动按照本模板的格式生成笔记。

## 📖 核心规范速览

### 1. 颜色语义 (Fast Text Color)
本模板使用颜色编码来区分信息的重要程度，请勿随意更改颜色含义：

| 颜色代码 | 含义 | 典型场景 |
|---|---|---|
| `~={red}` | **🚨 致命错误 / 绝对禁止** | 自相互作用发散、公式误用后果 |
| `~={orange}` | **⚠️ 易错提醒** | 常见混淆点、符号区分（如 $\boldsymbol{r}$ vs $\mathscr{r}$） |
| `~={blue}` | **📌 核心结论 / 公式** | Boxed 公式、最终计算结果 |
| `~={green}` | **✅ 技巧 / 记忆口诀** | 快速判断方法、数值比较（如“壳比体低约17%”） |
| `~={purple}` | **💡 物理直觉** | 为什么要这样想、物理图像 |

### 2. 结构模板
每篇笔记必须包含以下四个部分（AI 会自动遵循）：

1.  **🎯 速查结论**：纯公式卡片，30秒扫完。
2.  **📖 具体讲解**：分小节，使用 **【过程】** / **【结论】** 标注，逻辑清晰。
3.  **📝 复习自检清单**：3-5个闭卷回忆要点。
4.  **⚠️ 易错速记**：2-3条短语级别提醒。

### 3. 公式书写铁律
*   **行内公式**：`$E = mc^2$` ❌（错误：有空格）；`$E=mc^2$` ✅（正确）。
*   **绝对值**：在引用块（`>`）中，严禁使用 `|r|`，必须使用 `$\lvert \boldsymbol{r} \rvert$`。
*   **核心公式**：使用 `\boxed{}` 包裹，例如 `$$\boxed{\nabla \cdot \boldsymbol{E} = \rho/\varepsilon_0}$$`。

### 命名约定
- 示例文件统一放在 `examples/` 下。
- 文件名格式：`{章节号}-{英文/拼音短标题}.md`，如 `2.5.1-conductors.md`。
- 每个文件顶部用 YAML frontmatter 标明 `source`、`section`、`tags`，方便在 Obsidian 里按章节筛选和回溯原文。

## 🤖 AI 指令文件说明
本项目最核心的资产是根目录下的 `template-instructions.txt`。

这是一个“元提示词”（Meta-Prompt），它封装了上述所有排版逻辑、LaTeX 规则和颜色规范。你不需要每次都教 AI 怎么写，只需：
1.  复制 `template-instructions.txt` 的内容。
2.  粘贴到 AI 对话框中。
3.  紧接着发送你的教材内容（截图或文字）。

AI 就会自动产出符合本模板要求的 Markdown 笔记。

## 🛠️ 文件结构说明
text.
├── .gitattributes          # Git 属性配置（优化 Diff 和换行符）
├── .gitignore              # Git 忽略配置（忽略缓存等）
├── LICENSE                 # MIT 开源协议
├── README_EN.md               # 英文说明文档
├── README_cn.md            # 中文说明文档（本文件）
├── template-instructions.txt # 【核心】AI 系统提示词
├── examples/               # 示例笔记文件夹
│   ├── 2.5.1-conductors.md
│   └── 2.4.4-energy-remarks.md
└── assets/                 # 静态资源（截图等）
└── screenshot.png

## 💡 贡献与交流
如果你有更好的结构建议，或者发现了 Bug，欢迎提交 Issue 或 Pull Request。
希望这套模板能助你攻克硬核教材！

---
*Happy Note-taking! 祝学习愉快！*
